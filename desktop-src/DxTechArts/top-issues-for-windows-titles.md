---
title: Problemi principali per i titoli Windows
description: Questo articolo evidenzia molti dei problemi comuni che abbiamo visto nei giochi per PC di ultima generazione.
ms.assetid: 89b83473-1aa9-9a2d-8778-15cfb91cdea4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89be8ad7a68c247d589f304ea77fa9b3e63e105739264e39f71794c705b66cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118396506"
---
# <a name="top-issues-for-windows-titles"></a>Problemi principali per i titoli Windows

Il gruppo Microsoft Windows Gaming and Graphics Technologies Developer Relations esegue l'analisi delle prestazioni per molti giochi Windows ogni anno. Durante queste sessioni si ottiene un'esperienza pratica per associare il feedback degli sviluppatori e le query ricevute ogni giorno. Occasionalmente si aiuta a rilevare un arresto anomalo del sistema o un altro problema in un titolo, che offre informazioni dettagliate sui problemi riscontrati dagli sviluppatori.

Questo articolo evidenzia molti dei problemi comuni che abbiamo visto nei giochi per PC di ultima generazione.

-   [Prestazioni limitate della CPU](#cpu-limited-performance)
-   [Gestione di batch non scadente](#poor-batch-management)
-   [Copia eccessiva della memoria](#excessive-memory-copying)
-   [Uso eccessivo dell'invio di disegni dinamici](#excessive-use-of-dynamic-draw-submission)
-   [Sovraccarico elevato nell'elaborazione dei file](#high-overhead-in-file-processing)
-   [Installazione lenta e frustrante](#slow-and-frustrating-installation)
-   [Mancanza di considerazione della memoria fisica](#lack-of-consideration-of-physical-memory)
-   [Over-Reliance on Real-Time Audio Sample Rate Conversion](#over-reliance-on-real-time-audio-sample-rate-conversion)
-   [Frammentazione della memoria virtuale](#fragmention-of-virtual-memory)
-   [Manipolazione della parola Floating-Point controllo](#manipulation-of-the-floating-point-control-word)
-   [Installazione facoltativa del runtime DirectX](#optional-installation-of-the-directx-runtime)
-   [Uso eccessivo della sincronizzazione dei thread](#excessive-use-of-thread-synchronization)
-   [Uso di RDTSC](#use-of-rdtsc)

## <a name="cpu-limited-performance"></a>CPU-Limited prestazioni

La maggior parte dei giochi è limitata dalle prestazioni della CPU nei sistemi con GPU (High Performance Graphics Processing Unit). Ciò è talvolta dovuto a un uso non elevato dell'invio in batch per gli invii di estrazione, ma più in genere ciò è dovuto ad altri sistemi di gioco che usano gran parte dei cicli di CPU disponibili. Nei pochi casi in cui la GPU è stata considerata la limitazione, la causa è una frequenza di riempimento molto elevata o una domanda pixel shader, in impostazioni ad alta risoluzione o prestazioni basse dello shader di vertice da parte di una scheda video.

Dato che la maggior parte dei titoli è limitata alla CPU, le prestazioni più elevate vengono dall'ottimizzazione dei sistemi di gioco a elevato utilizzo di CPU. In genere, i sistemi di intelligenza artificiale o fisica e la logica di rilevamento delle collisioni associata sono i principali consumer dei cicli cpu nelle applicazioni Microsoft Direct3D ben gestite. Qualsiasi lavoro per migliorare questi sistemi può migliorare le prestazioni complessive del gioco.

## <a name="poor-batch-management"></a>Gestione di batch non scadente

Per ottenere un buon parallelismo con la GPU, è necessario che i batch di disegno contengano una geometria sufficiente e gli shader hanno la giusta complessità per mantenere occupata la scheda video, senza usare così tanti batch che il buffer dei comandi viene inondato. Nell'hardware di generazione corrente, è consigliabile inviare circa 300 o meno invii di draw-batch per frame (meno cpu con prestazioni inferiori) per evitare che l'elaborazione del buffer dei comandi del driver diventi un collo di bottiglia delle prestazioni. Alcune altre chiamate di stato dell'API e combinazioni di driver possono comportare un'elaborazione della CPU disaserta (ad esempio, la compilazione di driver di shader), pertanto è consigliabile eseguire un'analisi delle prestazioni di routine.

## <a name="excessive-memory-copying"></a>Copia eccessiva della memoria

Durante lo sviluppo della maggior parte dei titoli di PC, gli sviluppatori usano strutture di dati e stringhe utili per la gestione dei contenuti. Il lavoro della CPU necessario per il confronto di stringhe, la copia e altre modifiche spesso presenta un sovraccarico misurabile, in particolare quando si prendono in considerazione i riscontri delle prestazioni associati al sottosistema di cache e memoria. È consigliabile creare piani quando si sviluppano questi sistemi per rimuovere o ridurre al minimo l'affidamento sull'elaborazione delle stringhe quando il prodotto entra nelle fasi di test e rilascio principali.

## <a name="excessive-use-of-dynamic-draw-submission"></a>Uso eccessivo dell'invio di disegni dinamici

L'hardware video moderno funziona bene quando si gestiscono dati statici. Le schede di fascia alta hanno spesso una quantità molto elevata di memoria video, ma questa memoria non può essere utilizzata in modo efficace dai dati dinamici.

Sebbene i modelli di utilizzo ragionevolmente efficienti di buffer di vertici dinamici/buffer di indice possano essere implementati per il contenuto dinamico, molti titoli esulano da questo idioma per il contenuto altrimenti statico. Questo si può spesso verificare con alberi di partizionamento dello spazio binario (BSP) e sistemi basati su portale che archiviano la geometria in una struttura di dati che non esegue il mapping all'hardware e deve essere elaborata in buffer per ogni frame. L'inserimento del maggior numero possibile di contenuti nelle risorse statiche può ridurre notevolmente il sovraccarico di larghezza di banda dovuto al trasferimento dei dati nella scheda video, usare meglio la VRAM di bordo e ridurre il sovraccarico cpu/cache necessario per l'elaborazione di questo contenuto.

## <a name="high-overhead-in-file-processing"></a>Sovraccarico elevato nell'elaborazione dei file

I giochi per PC hanno ottenuto una reputazione per lunghi tempi di caricamento, in particolare se confrontati con i titoli della console con requisiti rigorosi in fase di caricamento. L'analisi del modo in cui molti titoli usano il sottosistema di file rivela alcuni problemi comuni.

L'overhead di apertura di un file è in genere molto superiore a quello previsto dagli sviluppatori. Con gli scanner di virus su richiesta in uso diffuso e le funzionalità aggiuntive di NTFS, l'apertura di un file è un'operazione piuttosto costosa. L'apertura di molti file contemporaneamente o l'apertura e la chiusura ripetute dello stesso file sono quindi un metodo non appropriato per gestire la gestione dei file. Alcuni giochi hanno provato a ridurre questo costo delle prestazioni verificando l'esistenza di un file prima di aprirlo. La realtà è che il test dell'esistenza di un file in NTFS richiede l'apertura del file, quindi il test prima dell'apertura comporta il pagamento del costo due volte.

I giochi che consentono modifiche ai componenti aggiuntivi o mod o che includono ancora lo scaffolding di sviluppo per verificare la presenza di file di dati di override possono avere ritardi significativi nel caricamento del gioco a causa del controllo di questi file, anche quando tali file non sono presenti. È consigliabile che i giochi controllino questi file solo quando vengono eseguiti con un'opzione della riga di comando speciale o un altro indicatore di modalità, in modo che solo gli utenti che usano questa funzionalità pagano effettivamente il costo delle prestazioni di questi controlli (spesso estesi).

Le prestazioni aggiuntive possono essere ottenute dal file system nel modo seguente:

-   Uso appropriato degli hint file system FILE \_ FLAG RANDOM ACCESS e FILE FLAG \_ \_ \_ \_ SEQUENTIAL \_ SCAN
-   Ridimensionamento dei buffer per evitare una grande quantità di chiamate alle API di lettura/scrittura del sistema operativo
-   Accesso ai file in modo asincrono
-   Caricamento di thread in background

È anche consigliabile convertire i dati offline (in fase di compilazione o di installazione) invece di basarsi sulla conversione alla prima esecuzione del gioco, poiché in questo modo si impone un'imposta significativa sulle prestazioni per ogni utente.

## <a name="slow-and-frustrating-installation"></a>Installazione lenta e frustrante

Un altro problema comune che si è visto è che sono necessari tempi di installazione molto lunghi per molti giochi moderni per PC. I programmi di installazione richiede all'utente più volte, a volte semplicemente per indicare all'utente, ad esempio, "Non è necessario Installare DirectX". In genere, questi programmi di installazione offensivi richiedono all'utente di selezionare Più volte **Avanti** o **OK** prima dell'inizio dell'installazione del gioco. Dopo l'inizio, alcuni titoli hanno bisogno di un'ora o più prima che l'utente abbia la possibilità di eseguire il gioco. La prima ora di esperienza di gioco non deve essere l'installazione.

È consigliabile usare diversi approcci per gestire l'installazione. Per prima cosa, mantenere le richieste semplici e al minimo. In secondo luogo, è necessario creare i dati del gioco in modo che alcuni o tutti i file di dati possano essere usati direttamente dal disco di distribuzione, laddove possibile. Le unità DVD moderne hanno larghezza di banda molto elevata. In terzo piano, è consigliabile implementare install-on-demand nei titoli per ridurre o eliminare il processo di installazione e consentire agli utenti di entrare nel gioco il più rapidamente possibile. Per altre informazioni sull'installazione su richiesta, vedere [Install-on-Demand for Games](/windows/desktop/DxTechArts/install-on-demand-for-games).

Per altre raccomandazioni sull'installazione del gioco, vedere [Semplificazione dell'installazione del gioco.](/windows/desktop/DxTechArts/simplifying-game-installation)

## <a name="lack-of-consideration-of-physical-memory"></a>Mancanza di considerazione della memoria fisica

A causa dell'ampia variabilità dell'hardware del PC sul mercato, i titoli usano in genere test di configurazione ad hoc per selezionare le impostazioni predefinite per il livello di dettaglio grafico. Alcuni dei titoli che abbiamo visto usano le dimensioni della memoria video in questi test, ma non riescono a correlare questo problema con le dimensioni della memoria fisica. Per gestire le situazioni di dispositivo perso, la maggior parte della memoria video (sia la VRAM locale nella scheda che l'apertura della memoria AGP non locale) deve essere supportata dalla memoria fisica, tramite l'uso di risorse gestite o strutture di dati personalizzate. Alcune schede video di fascia alta hanno dimensioni di VRAM che rivaleggiano con le dimensioni delle memorie CPU di fascia bassa. Nelle situazioni in cui il sistema ha memoria fisica limitata rispetto alla scheda video, la maggior parte di tale VRAM non può essere utilizzata in modo efficace e devono essere configurate impostazioni di dettaglio inferiori.

## <a name="over-reliance-on-real-time-audio-sample-rate-conversion"></a>Over-Reliance conversione Real-Time frequenza di campionamento audio

Un'altra origine comune di masterizzazione del ciclo cpu si verifica quando il sistema audio è necessario per convertire la velocità di riproduzione durante la combinazione nel buffer hardware. Con Windows driver WDM (Driver Model), il formato del buffer hardware non è sotto controllo diretto dell'applicazione, perché è una risorsa a livello di kernel. al contrario, il formato viene selezionato in base al formato di massima qualità di tutte le origini e alle funzionalità dell'hardware. Per impostazione predefinita, Windows XP usa una conversione della frequenza di campionamento di alta qualità per questo processo e, se la maggior parte dei campioni audio richiede una conversione della frequenza, verrà utilizzata una parte significativa dei cicli della CPU.

È consigliabile creare tutti i buffer DirectSound con la stessa frequenza di campionamento. Se si usano le funzioni **waveOut** di Microsoft Win32, è consigliabile usare anche una frequenza di campionamento coerente con queste funzioni. Con i driver WDM, i buffer verranno tutti misti dal kernel e se si usa una frequenza di campionamento più elevata in alcuni di essi, le frequenze di campionamento di tutte le altre verranno convertite in corrispondenza. Si noti che ciò implica l'uso della stessa velocità di riproduzione per tutti i campioni audio, inclusi i buffer di decompressione audio in streaming. L'impostazione della frequenza del buffer primario non ha alcun effetto a meno che non si abbia come destinazione Windows 98 o Windows Millennium Edition.

> [!Note]  
> In Windows Vista e versioni successive del sistema operativo, DirectSound e **waveOut** usano l'API di sessione audio [Windows (WASAPI)](/windows/desktop/CoreAudio/wasapi) per tutto l'output audio.

 

## <a name="fragmention-of-virtual-memory"></a>Frammentazione della memoria virtuale

Sono stati osservati alcuni problemi recenti relativi al limite a 32 bit per lo spazio di memoria del processo. Anche se 2 GB di spazio degli indirizzi virtuali per i processi in modalità utente sono stati più che adeguati cronologicamente, l'aumento dell'uso di file mappati alla memoria di grandi dimensioni, allocatori di memoria personalizzati e dimensioni di VRAM sempre maggiori (che devono essere mappate nello spazio del processo) ha iniziato a causare situazioni in cui le allocazioni dello spazio di memoria virtuale hanno esito negativo. Alcune DLL non Microsoft usano percorsi di avvio fisso al centro dello spazio degli indirizzi virtuali, causando una frammentazione che causa allocazioni non riuscite.

Questi problemi si verificano più spesso quando il gioco usa uno schema di allocazione di memoria personalizzato che tenta di allocare un blocco continuo di grandi dimensioni di spazio di memoria virtuale. È consigliabile scrivere allocatori in modo da richiedere parti più ragionevoli dello spazio degli indirizzi virtuali in base alle esigenze. Ad esempio, richiedere 64 o 256 MB alla volta, ma non 1 GB. È tuttavia necessario fare attenzione a non causare ulteriori frammentazioni. L'avvento dei sistemi operativi a 64 bit e dell'hardware sarà molto utile per questi problemi in futuro, ma è necessario fare attenzione ai sistemi a 32 bit di generazione corrente.

## <a name="manipulation-of-the-floating-point-control-word"></a>Manipolazione della parola Floating-Point controllo

Come supporto per il debug, alcuni sviluppatori hanno abilitato le eccezioni sull'unità a virgola mobile (FPU) tramite modifiche della parola di controllo a virgola mobile. Questa operazione è estremamente problematica e probabilmente causerà l'arresto anomalo del processo. Proprio come la convenzione di chiamata richiede che il registro ebx sia mantenuto, la maggior parte del sistema presuppone che l'FPU sia in uno stato predefinito, offrirà risultati ragionevoli e non genererà eccezioni. I driver e altri componenti di sistema spesso calcolano i risultati in base al presupposto che i valori di errore standard vengano visualizzati nei registri per le condizioni non ottimali, ma se le eccezioni sono abilitate, questi verranno gestiti e si verificano arresti anomali.

Direct3D imposta l'unità a virgola mobile su precisione singola, round-to-nearest come parte dell'inizializzazione per il thread chiamante, a meno che non venga usato il flag D3DCREATE FPU PRESERVE, nel qual caso la parola di controllo a virgola mobile non viene \_ \_ toccata. Poiché la parola di controllo è un'impostazione per thread, assicurarsi che tutti i thread dell'applicazione siano impostati sulla modalità a precisione singola può ottimizzare le prestazioni. Tenere presente che la chiamata di [**\_ control87**](https://msdn.microsoft.com/library/e9b52ceh(v=VS.71).aspx) non è valida per la codifica nativa x64, che usa esclusivamente la funzionalità SSE, ed è estremamente costosa per l'architettura basata su PowerPC della CPU Xbox 360.

> [!Note]  
> Se si modifica la parola di controllo, usare [**\_ controlfp \_ s**](https://msdn.microsoft.com/library/c9676k6h(v=VS.80).aspx) e tenere presente che per le piattaforme x64 non è possibile modificare la precisione a virgola mobile tramite la parola di controllo.

 

In tutte le librerie in cui è necessario avere regole di arrotondamento diverse o altri comportamenti, ad esempio la gestione di vertex shader software o la compilazione, si salva e si ripristina la parola di controllo. Se un gioco deve usare un arrotondamento non standard o eccezioni FPU, deve salvare e ripristinare la parola di controllo a virgola mobile e assicurarsi che non chiami codice esterno che non si è dimostrato sicuro da questi problemi, incluse le API di sistema.

## <a name="optional-installation-of-the-directx-runtime"></a>Installazione facoltativa del runtime DirectX

Diversi giochi chiedono all'utente se installare DirectX. Ciò può causare problemi se l'utente presuppone che nel sistema sia installata la versione più recente di DirectX Redistributable e ignora l'installazione e successivamente l'installazione continua correttamente. Se il gioco richiede una versione specifica di D3DX o altre funzionalità aggiornate non installate, il gioco non funzionerà e l'utente sarà molto frustrante.

È consigliabile che il programma di installazione del gioco installi automaticamente il ridistribuibile DirectX su cui è stato compilato il gioco. Il processo di installazione di DirectX è progettato in modo da verificare se è necessario aggiornare qualsiasi elemento e restituisce rapidamente se non lo è. Non è quindi necessario chiedere all'utente di installare DirectX.

È possibile eseguire un'installazione invisibile all'utente di DirectX eseguendo questo comando dal pacchetto di installazione: **dxsetup.exe /silent**

Inoltre, le dimensioni effettive della cartella ridistribuibile possono essere configurate in modo da includere solo i file CAB (.cab) effettivamente necessari per l'uso e le piattaforme di destinazione del gioco.

> [!Note]  
> Prima di usare **dxsetup**, leggere [Not So Direct Setup](https://walbourn.github.io/).

 

## <a name="excessive-use-of-thread-synchronization"></a>Uso eccessivo della sincronizzazione dei thread

Durante la profilatura dei giochi, gli hotspot principali sono spesso correlati all'immissione e all'uscita di sezioni critiche. Con la diffusione di CPU multi-core, l'uso del multithreading nei giochi è aumentato notevolmente e molte implementazioni si basano su un uso intenso della sincronizzazione dei thread. Il tempo di CPU necessario per prendere una sezione critica anche senza conflitti è piuttosto significativo e tutte le altre forme di sincronizzazione dei thread sono ancora più costose. È quindi necessario fare attenzione a ridurre al minimo l'uso di queste primitive.

Un'origine comune di una sincronizzazione eccessiva nei giochi è l'uso di [D3DCREATE \_ MULTITHREADED.](/windows/desktop/direct3d9/d3dcreate) Questo flag, pur rendendo Direct3D thread-safe per il rendering da più thread, adotta un approccio molto conservativo, determinando un sovraccarico di sincronizzazione elevato. I giochi devono evitare questo flag. Al contrario, è necessario architetta il motore in modo che tutte le comunicazioni con Direct3D da un singolo thread e qualsiasi comunicazione tra thread sia gestita direttamente. Per altre informazioni sulla progettazione di giochi multi-thread, vedere l'articolo Scrittura di codice per [più core Xbox 360 e Microsoft Windows](/windows/desktop/DxTechArts/coding-for-multiple-cores).

## <a name="use-of-rdtsc"></a>Uso di RDTSC

Non è consigliabile usare **l'istruzione x86 RDTSC.** **RDTSC** non riesce a calcolare correttamente i tempi in alcuni schemi di risparmio energia che modificano la frequenza della CPU in modo dinamico e in molte CPU multi-core per cui il contatore del ciclo non è sincronizzato tra core. I giochi devono invece usare [**l'API QueryPerformanceCounter.**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter) Per altre informazioni sui problemi relativi a **RDTSC** e sull'implementazione di tempistiche ad alta risoluzione **con QueryPerformanceCounter,** vedere l'articolo Temporizzazione del gioco e [processori multicore.](/windows/desktop/DxTechArts/game-timing-and-multicore-processors)

 

 