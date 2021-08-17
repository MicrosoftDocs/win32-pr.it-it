---
title: Temporizzazione dei giochi e processori multicore
description: Questo articolo suggerisce una soluzione più accurata e affidabile per ottenere intervalli della CPU ad alta risoluzione usando le API di Windows QueryPerformanceCounter e QueryPerformanceFrequency.
ms.assetid: 1512324d-dffa-3681-be3f-f63a3b8f11db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed5e668e87a2645859838b1fdf9cfb35263381e9ce9c73fbe72232ad3d3a46cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649349"
---
# <a name="game-timing-and-multicore-processors"></a>Temporizzazione dei giochi e processori multicore

Con le tecnologie di risparmio energia sempre più comuni nei computer attuali, un metodo comunemente usato per ottenere intervalli di CPU ad alta risoluzione, l'istruzione RDTSC, potrebbe non funzionare più come previsto. Questo articolo suggerisce una soluzione più accurata e affidabile per ottenere intervalli della CPU ad alta risoluzione usando le API di Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).

-   [Background](#background)
-   [Indicazioni](#recommendations)
-   [Compatibilità delle applicazioni](#application-compatibility)

## <a name="background"></a>Sfondo

Dopo l'introduzione del set di istruzioni X86 P5, molti sviluppatori di giochi hanno fatto uso del contatore dei timestamp di lettura, l'istruzione RDTSC, per eseguire tempi ad alta risoluzione. I timer multimediali Windows sono sufficientemente precisi per l'elaborazione audio e video, ma con tempi di fotogrammi di una decina di millisecondi o meno, non hanno una risoluzione sufficiente per fornire informazioni sul tempo delta. Molti giochi usano ancora un timer multimediale all'avvio per stabilire la frequenza della CPU e usano tale valore di frequenza per ridimensionare i risultati da RDTSC per ottenere l'ora esatta. A causa delle limitazioni di RDTSC, l'API Windows espone il modo più corretto per accedere a questa funzionalità tramite le routine [**di QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e [**QueryPerformanceFrequency.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)

L'uso di RDTSC per la temporizzazione è a causa di questi problemi fondamentali:

-   Valori discontinui. L'uso diretto di RDTSC presuppone che il thread sia sempre in esecuzione nello stesso processore. I sistemi multiprocessore e dual core non garantiscono la sincronizzazione dei contatori del ciclo tra core. Questo problema si verifica in combinazione con tecnologie moderne di risparmio energia che inattive e ripristinano diversi core in momenti diversi, causando in genere la non sincronizzazione dei core. Per un'applicazione, ciò comporta in genere problemi o potenziali arresti anomali quando il thread passa tra i processori e ottiene valori di temporizzazione che comportano delta di grandi dimensioni, delta negativi o tempistiche arrestate.
-   Disponibilità di hardware dedicato. RDTSC blocca le informazioni sugli intervalli richieste dall'applicazione al contatore dei cicli del processore. Per molti anni questo è stato il modo migliore per ottenere informazioni di temporizzazione ad alta precisione, ma le schede madre più aggiornate includono ora dispositivi di temporizzazione dedicati che forniscono informazioni temporali ad alta risoluzione senza gli svantaggi di RDTSC.
-   Variabilità della frequenza della CPU. Si presuppone spesso che la frequenza della CPU sia fissa per la durata del programma. Tuttavia, con le moderne tecnologie di risparmio energia, si tratta di un presupposto errato. Sebbene inizialmente limitata a computer portatili e altri dispositivi mobili, la tecnologia che modifica la frequenza della CPU è in uso in molti PC desktop di fascia alta; la disabilitazione della funzione per mantenere una frequenza coerente non è in genere accettabile per gli utenti.

## <a name="recommendations"></a>Consigli

I giochi necessitano di informazioni di temporizzazione accurate, ma è anche necessario implementare il codice di intervallo in modo da evitare i problemi associati all'uso di RDTSC. Quando si implementa un intervallo ad alta risoluzione, seguire questa procedura:

1.  Usare [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) invece di RDTSC. Queste API possono usare RDTSC, ma potrebbero invece usare dispositivi di temporizzazione sulla scheda madre o altri servizi di sistema che forniscono informazioni di alta qualità sugli intervalli di temporizzazione ad alta risoluzione. Anche se RDTSC è molto più veloce di **QueryPerformanceCounter,** poiché quest'ultima è una chiamata API, è un'API che può essere chiamata diverse centinaia di volte per frame senza alcun impatto evidente. Tuttavia, gli sviluppatori devono provare a fare in modo che i giochi chiamino **QueryPerformanceCounter** il meno possibile per evitare eventuali problemi di prestazioni.
2.  Quando si calcolano i delta, i valori devono essere chiusi per assicurarsi che eventuali bug nei valori temporali non causano arresti anomali o calcoli instabili correlati al tempo. L'intervallo di chiusura deve essere compreso tra 0 (per evitare valori differenziali negativi) e un valore ragionevole in base alla frequenza dei fotogrammi più bassa prevista. È probabile che il controllo sia utile in qualsiasi debug dell'applicazione, ma assicurarsi di ricordarlo se si esegue l'analisi delle prestazioni o si esegue il gioco in una modalità non impostata.
3.  Calcola tutti gli intervalli in un singolo thread. Il calcolo dell'intervallo su più thread, ad esempio con ogni thread associato a un processore specifico, riduce notevolmente le prestazioni dei sistemi multi-core.
4.  Impostare il thread singolo in modo che rimanga in un singolo processore usando l Windows API [**SetThreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask). In genere, si tratta del thread principale del gioco. Anche se [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) vengono in genere regolati per più processori, i bug nel BIOS o nei driver possono causare la restituzione di valori diversi da parte di queste routine quando il thread passa da un processore a un altro. È quindi meglio mantenere il thread in un singolo processore.

    Tutti gli altri thread devono funzionare senza raccogliere i propri dati timer. Non è consigliabile usare un thread di lavoro per calcolare i tempi, perché questo diventerà un collo di bottiglia per la sincronizzazione. I thread di lavoro devono invece leggere i timestamp dal thread principale e poiché i thread di lavoro leggono solo i timestamp, non è necessario usare sezioni critiche.

5.  Chiamare [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) una sola volta, perché la frequenza non cambierà mentre il sistema è in esecuzione.

## <a name="application-compatibility"></a>Compatibilità delle applicazioni

Molti sviluppatori hanno fatto ipotesi sul comportamento di RDTSC nel corso di molti anni, pertanto è molto probabile che alcune applicazioni esistenti presentino problemi quando vengono eseguite in un sistema con più processori o core a causa dell'implementazione temporale. Questi problemi si manifestano in genere come anomalie o movimenti lenti. Non esiste un rimedio semplice per le applicazioni che non sono a conoscenza del risparmio energia, ma esiste uno shim esistente che forza l'esecuzione di un'applicazione sempre in un singolo processore in un sistema multiprocessore.

Per creare questo shim, scaricare microsoft Application Compatibility Toolkit da [Windows Application Compatibility](/archive/blogs/yongrhee/download-application-compatibility-toolkit-act-for-windows-10).

Usando l'amministratore della compatibilità, parte del toolkit, creare un database dell'applicazione e le correzioni associate. Creare una nuova modalità di compatibilità per questo database e selezionare la correzione di compatibilità **SingleProcAffinity** per forzare l'esecuzione di tutti i thread dell'applicazione in un singolo processore/core. Usando lo strumento da riga di comando Fixpack.exe (anche parte del toolkit), è possibile convertire questo database in un pacchetto installabile per l'installazione, il test e la distribuzione.

Per istruzioni sull'uso di Compatibility Administrator, vedere la documentazione del toolkit. Per la sintassi ed esempi di utilizzo Fixpack.exe, vedere la guida della riga di comando.

Per informazioni orientate ai clienti, vedere gli articoli seguenti knowledge base di Guida e supporto tecnico Microsoft:

-   I programmi che usano la [funzione QueryPerformanceCounter](https://support.microsoft.com/kb/895980) possono avere prestazioni scarse in Windows Server 2003 e in Windows XP (articolo 895980)
-   [Le prestazioni del gioco potrebbero risultare scarse in Windows computer](https://support.microsoft.com/kb/909944) basato su XP che usa un processore dual-core (articolo 909944)

 

 
