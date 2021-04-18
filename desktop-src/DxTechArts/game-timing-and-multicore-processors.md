---
title: Temporizzazione dei giochi e processori multicore
description: Questo articolo suggerisce una soluzione più accurata e affidabile per ottenere intervalli di CPU ad alta risoluzione usando le API Windows QueryPerformanceCounter e QueryPerformanceFrequency.
ms.assetid: 1512324d-dffa-3681-be3f-f63a3b8f11db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5c511f558b59e94945e63c44db225f34ac2583
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300086"
---
# <a name="game-timing-and-multicore-processors"></a>Temporizzazione dei giochi e processori multicore

Con le tecnologie di risparmio energia che diventano più comuni nei computer odierni, un metodo comunemente usato per ottenere intervalli di CPU ad alta risoluzione, l'istruzione RDTSC, potrebbe non funzionare più come previsto. Questo articolo suggerisce una soluzione più accurata e affidabile per ottenere intervalli di CPU ad alta risoluzione usando le API Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).

-   [Background](#background)
-   [Indicazioni](#recommendations)
-   [Compatibilità delle applicazioni](#application-compatibility)

## <a name="background"></a>Sfondo

Dall'introduzione del set di istruzioni x86 P5, molti sviluppatori di giochi hanno usato il contatore Read Time Stamp, l'istruzione RDTSC, per eseguire tempi di risoluzione elevata. I timer multimediali di Windows sono sufficientemente precisi per l'elaborazione audio e video, ma con tempi di fotogrammi di decine di millisecondi o minori, non hanno una risoluzione sufficiente per fornire informazioni sul tempo delta. Molti giochi usano ancora un timer multimediale all'avvio per stabilire la frequenza della CPU e usano tale valore di frequenza per ridimensionare i risultati da RDTSC per ottenere il tempo esatto. A causa delle limitazioni di RDTSC, l'API Windows espone il modo più corretto per accedere a questa funzionalità tramite le routine di [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).

Questo utilizzo di RDTSC per la tempistica soffre di questi problemi fondamentali:

-   Valori discontinui. L'utilizzo diretto di RDTSC presuppone che il thread sia sempre in esecuzione nello stesso processore. I sistemi multiprocessore e dual core non garantiscono la sincronizzazione dei contatori del ciclo tra i core. Questa funzionalità è esacerbata in combinazione con moderne tecnologie di risparmio energia che inattivano e ripristinano diversi core in momenti diversi, il che comporta che i core non siano sincronizzati. Per un'applicazione, ciò comporta in genere problemi di anomalie o potenziali arresti anomali quando il thread passa tra i processori e ottiene i valori di intervallo che comportano Delta di grandi dimensioni, Delta negativi o intervalli interrotti.
-   Disponibilità di hardware dedicato. RDTSC blocca le informazioni di temporizzazione richieste dall'applicazione al contatore dei cicli del processore. Per molti anni questo è stato il modo migliore per ottenere informazioni sugli intervalli a precisione elevata, ma le schede madri più recenti ora includono dispositivi temporizzati dedicati che forniscono informazioni sui tempi di risoluzione elevata senza gli svantaggi di RDTSC.
-   Variabilità della frequenza della CPU. Il presupposto è spesso il fatto che la frequenza della CPU è fissa per la durata del programma. Tuttavia, con le moderne tecnologie di risparmio energia, si tratta di un presupposto non corretto. Sebbene inizialmente limitato a computer portatili e altri dispositivi mobili, la tecnologia che modifica la frequenza della CPU è in uso in molti PC desktop di fascia alta; la disabilitazione della funzione per mantenere una frequenza coerente non è generalmente accettabile per gli utenti.

## <a name="recommendations"></a>Consigli

Per i giochi sono necessarie informazioni temporali accurate, ma è anche necessario implementare il codice di temporizzazione in modo da evitare i problemi associati all'uso di RDTSC. Quando si implementa la temporizzazione ad alta risoluzione, seguire questa procedura:

1.  Usare [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) anziché RDTSC. Queste API possono usare RDTSC, ma possono invece usare un dispositivo di temporizzazione sulla scheda madre o altri servizi di sistema che forniscono informazioni sui tempi di risoluzione elevata di alta qualità. Mentre RDTSC è molto più veloce di **QueryPerformanceCounter**, poiché quest'ultima è una chiamata API, è un'API che può essere chiamata diverse centinaia di volte per fotogramma senza alcun effetto evidente. Tuttavia, gli sviluppatori devono provare a fare in modo che i loro giochi chiamino **QueryPerformanceCounter** il minor possibile per evitare qualsiasi riduzione delle prestazioni.
2.  Quando si calcolano i Delta, i valori devono essere fissati per garantire che eventuali bug nei valori temporali non causino arresti anomali o calcoli instabili correlati al tempo. L'intervallo del morsetto deve essere compreso tra 0 (per evitare valori Delta negativi) e un valore ragionevole in base al framerate minimo previsto. È probabile che il blocco sia utile per qualsiasi operazione di debug dell'applicazione, ma tenere presente che se si esegue l'analisi delle prestazioni o si esegue il gioco in modalità non ottimizzata.
3.  Calcola tutte le tempistiche in un singolo thread. Calcolo dell'intervallo di tempo su più thread, ad esempio con ogni thread associato a un processore specifico, riduce notevolmente le prestazioni dei sistemi multicore.
4.  Impostare il singolo thread in modo che rimanga in un singolo processore usando l'API Windows [**SetThreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask). In genere, si tratta del thread del gioco principale. Sebbene [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) in genere si modifichino per più processori, i bug nel BIOS o nei driver possono comportare la restituzione di valori diversi quando il thread passa da un processore a un altro. Quindi, è preferibile che il thread venga mantenuto su un singolo processore.

    Tutti gli altri thread dovrebbero funzionare senza raccogliere i propri dati del timer. Non è consigliabile usare un thread di lavoro per calcolare la tempistica, perché questo diventerà un collo di bottiglia di sincronizzazione. Al contrario, i thread di lavoro devono leggere i timestamp dal thread principale e, poiché i thread di lavoro leggono solo i timestamp, non è necessario usare sezioni critiche.

5.  Chiamare [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) solo una volta, perché la frequenza non verrà modificata mentre il sistema è in esecuzione.

## <a name="application-compatibility"></a>Compatibilità delle applicazioni

Molti sviluppatori hanno ipotizzato il comportamento di RDTSC in molti anni, quindi è molto probabile che alcune applicazioni esistenti mostrino problemi quando vengono eseguite in un sistema con più processori o core a causa dell'implementazione temporizzata. Questi problemi si manifesteranno in genere come glitch o movimenti lenti. Non esiste un rimedio facile per le applicazioni che non sono a conoscenza del risparmio energia, ma esiste uno shim esistente per forzare l'esecuzione sempre di un'applicazione su un singolo processore in un sistema multiprocessore.

Per creare questo shim, scaricare Microsoft Application Compatibility Toolkit dalla pagina relativa alla [compatibilità delle applicazioni Windows](/archive/blogs/yongrhee/download-application-compatibility-toolkit-act-for-windows-10).

Utilizzando Compatibility Administrator, parte del Toolkit, creare un database dell'applicazione e le correzioni associate. Creare una nuova modalità di compatibilità per il database e selezionare la correzione per la compatibilità **SingleProcAffinity** per forzare l'esecuzione di tutti i thread dell'applicazione in un singolo processore/Core. Utilizzando lo strumento da riga di comando Fixpack.exe (anche parte del Toolkit), è possibile convertire il database in un pacchetto installabile per l'installazione, il testing e la distribuzione.

Per istruzioni sull'uso di Compatibility Administrator, vedere la documentazione del Toolkit. Per la sintassi per ed esempi sull'uso di Fixpack.exe, vedere la guida della riga di comando.

Per informazioni orientate ai clienti, vedere gli articoli della Knowledge base seguenti di guida e supporto tecnico Microsoft:

-   [Programmi che l'utente può eseguire in Windows Server 2003 e Windows XP](https://support.microsoft.com/kb/895980) (articolo 895980).
-   Le [prestazioni del gioco potrebbero essere insufficienti in un computer basato su Windows XP che usa un processore dual-core](https://support.microsoft.com/kb/909944) (articolo 909944)

 

 