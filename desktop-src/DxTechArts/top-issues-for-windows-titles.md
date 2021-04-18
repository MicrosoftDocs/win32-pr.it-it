---
title: Problemi principali per i titoli di Windows
description: In questo articolo vengono illustrati molti dei problemi comuni riscontrati nei giochi per PC di generazione corrente.
ms.assetid: 89b83473-1aa9-9a2d-8778-15cfb91cdea4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 547c977f7d8e4895ef73ba229a9012854a7c6d27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300162"
---
# <a name="top-issues-for-windows-titles"></a>Problemi principali per i titoli di Windows

Il gruppo Microsoft Windows Gaming and graphics Technologies Developer Relations esegue un'analisi delle prestazioni per molti giochi di Windows ogni anno. Durante queste sessioni, si ottiene un'esperienza pratica per associare il feedback degli sviluppatori e le query ricevute ogni giorno. In alcuni casi è utile tenere traccia di un arresto anomalo o di un altro problema in un titolo, che ci fornisce informazioni approfondite sui problemi riscontrati dagli sviluppatori.

In questo articolo vengono illustrati molti dei problemi comuni riscontrati nei giochi per PC di generazione corrente.

-   [Prestazioni limitate alla CPU](#cpu-limited-performance)
-   [Gestione batch scadente](#poor-batch-management)
-   [Copia eccessiva della memoria](#excessive-memory-copying)
-   [Utilizzo eccessivo dell'invio di disegni dinamici](#excessive-use-of-dynamic-draw-submission)
-   [Sovraccarico elevato nell'elaborazione dei file](#high-overhead-in-file-processing)
-   [Installazione lenta e frustrante](#slow-and-frustrating-installation)
-   [Mancanza di considerazioni sulla memoria fisica](#lack-of-consideration-of-physical-memory)
-   [Conversione di frequenza di campionamento audio Real-Time](#over-reliance-on-real-time-audio-sample-rate-conversion)
-   [Frammentazione della memoria virtuale](#fragmention-of-virtual-memory)
-   [Manipolazione della parola di controllo Floating-Point](#manipulation-of-the-floating-point-control-word)
-   [Installazione facoltativa di DirectX Runtime](#optional-installation-of-the-directx-runtime)
-   [Utilizzo eccessivo della sincronizzazione dei thread](#excessive-use-of-thread-synchronization)
-   [Uso di RDTSC](#use-of-rdtsc)

## <a name="cpu-limited-performance"></a>Prestazioni CPU-Limited

La maggior parte dei giochi è limitata dalle prestazioni della CPU nei sistemi con GPU (Graphics Processing Unit) ad alte prestazioni. Questo problema si verifica a volte a causa di un utilizzo non elevato di batch per gli invii di un progetto, ma in genere è dovuto ad altri sistemi di gioco che utilizzano una parte elevata dei cicli CPU disponibili. Nei pochi casi in cui è stata rilevata la GPU come limitazione, la ragione è una frequenza di riempimento molto elevata o pixel shader richiesta, in impostazioni ad alta risoluzione o prestazioni di vertex shader ridotte da una scheda video.

Poiché la maggior parte dei titoli è limitata alla CPU, i principali risultati delle prestazioni derivano dall'ottimizzazione dei sistemi di gioco con utilizzo intensivo della CPU. In genere, i sistemi di intelligenza artificiale o fisica e la logica di rilevamento collisione associata sono i principali consumer di cicli della CPU in cui sono presenti applicazioni Microsoft Direct3D. Qualsiasi lavoro per migliorare questi sistemi può migliorare le prestazioni complessive del gioco.

## <a name="poor-batch-management"></a>Gestione batch scadente

Per ottenere un buon parallelismo con la GPU, è necessario che i batch di traccia contengano una geometria sufficiente, mentre gli shader hanno la complessità giusta, per garantire la disponibilità della scheda video, senza usare così tanti batch che il buffer dei comandi è invaso. Per l'hardware di generazione corrente, è consigliabile circa 300 o meno invii di batch di estrazione per frame (un minor numero di CPU con prestazioni inferiori) per impedire che l'elaborazione del driver del buffer dei comandi diventi un collo di bottiglia delle prestazioni. Alcune altre chiamate di stato API e combinazioni di driver possono comportare una costosa elaborazione della CPU (ad esempio, la compilazione di driver di shader), quindi si consiglia vivamente di eseguire l'analisi delle prestazioni di routine.

## <a name="excessive-memory-copying"></a>Copia eccessiva della memoria

Durante lo sviluppo della maggior parte dei titoli di PC, gli sviluppatori usano strutture di dati e stringhe utili per la gestione dei contenuti. Il lavoro della CPU necessario per il confronto di stringhe, la copia e altre manipolazioni spesso presenta un sovraccarico misurabile, in particolare quando si considerano i riscontri delle prestazioni associati al sottosistema della cache e della memoria. È necessario pianificare i piani quando si sviluppano questi sistemi per rimuovere o ridurre al minimo la dipendenza dall'elaborazione di stringhe quando il prodotto entra nelle fasi principali di test e rilascio.

## <a name="excessive-use-of-dynamic-draw-submission"></a>Utilizzo eccessivo dell'invio di disegni dinamici

L'hardware video moderno offre prestazioni ottimali quando si gestiscono dati statici. Per gli adapter di fascia alta è spesso presente una quantità molto elevata di memoria video, ma questa memoria non può essere utilizzata in modo efficace da dati dinamici.

Sebbene i modelli di utilizzo ragionevolmente efficienti dei buffer dei vertici dinamici o degli indici possano essere implementati per il contenuto dinamico, molti titoli hanno un utilizzo eccessivo di questo idioma per il contenuto statico altrimenti. Questa operazione è spesso visibile con gli alberi del partizionamento dello spazio binario (BSP) e i sistemi basati su portale che archiviano la geometria in una struttura di dati che non è mappata all'hardware e deve essere elaborata in buffer per ogni frame. L'inserimento di un maggior quantità di contenuto nelle risorse statiche può ridurre notevolmente il sovraccarico della larghezza di banda del trasferimento dei dati alla scheda video, sfruttare al meglio la VRAM in corso e ridurre il sovraccarico della CPU/cache dovuto all'elaborazione del contenuto.

## <a name="high-overhead-in-file-processing"></a>Sovraccarico elevato nell'elaborazione dei file

I giochi per PC hanno ottenuto una reputazione per i tempi di caricamento lunghi, in particolare in caso di confronto con i titoli di console con requisiti di tempo di caricamento rigorosi. L'analisi del modo in cui molti titoli usano il sottosistema di file rivela alcuni problemi comuni.

Il sovraccarico dell'apertura di un file è in genere molto più elevato rispetto a quanto previsto dagli sviluppatori. Con l'uso generalizzato di scanner antivirus su richiesta e la funzionalità aggiuntiva di NTFS, l'apertura di un file è un'operazione piuttosto dispendiosa. Aprire più file contemporaneamente o aprire e chiudere ripetutamente lo stesso file è pertanto un metodo scarso per gestire la gestione dei file. Alcuni giochi hanno tentato di ridurre il costo delle prestazioni testando l'esistenza di un file prima di aprirlo. La realtà è che il test per l'esistenza di un file in NTFS richiede l'apertura del file, quindi il test prima di aprire i risultati pagando il costo due volte.

I giochi che consentono modifiche o mods di componenti aggiuntivi o che ancora includono l'impalcatura di sviluppo per verificare la presenza di file di dati di sostituzione possono causare ritardi significativi nel caricamento del gioco a causa del controllo di questi file, anche quando tali file non sono presenti. Si consiglia ai giochi di controllare solo questi file quando vengono eseguiti con un'opzione speciale della riga di comando o un altro indicatore di modalità, in modo che solo gli utenti che utilizzano questa funzionalità paghino effettivamente il costo delle prestazioni di questi controlli (spesso estesi).

Le prestazioni aggiuntive possono essere ottenute dalla file system da quanto segue:

-   Uso appropriato del flag di FILE hint di file system l' \_ \_ \_ accesso casuale e l' \_ \_ analisi sequenziale del flag file \_
-   Ridimensionamento dei buffer per evitare una grande quantità di chiamate alle API di lettura/scrittura del sistema operativo
-   Accesso asincrono ai file
-   Caricamento di thread in background

Si consiglia anche di convertire i dati offline (in fase di compilazione o di installazione) invece di basarsi sulla conversione quando il gioco viene eseguito per la prima volta, in quanto questa operazione impone una significativa tassazione delle prestazioni per ogni utente.

## <a name="slow-and-frustrating-installation"></a>Installazione lenta e frustrante

Un altro problema comune riscontrato sono tempi di installazione molto lunghi necessari per molti giochi per PC moderni. I programmi di installazione richiedono l'utente più volte, a volte semplicemente per indicare all'utente, ad esempio, che non è necessario che DirectX sia installato. In genere, questi programmi di installazione che danneggiano gli utenti richiedono che l'utente scelga **Avanti** o **OK** molte volte prima che inizi l'installazione del gioco. Una volta iniziato, abbiamo visto che alcuni titoli hanno più di un'ora prima che l'utente abbia la possibilità di riprodurre il gioco. Si è convinti che la prima ora di un'esperienza di gioco non dovrebbe essere l'installazione.

Per la gestione dell'installazione è consigliabile usare diversi approcci. Per prima cosa, è possibile usare le istruzioni semplici e minime. In secondo luogo, progettare i dati del gioco in modo che alcuni o tutti i file di dati possano essere usati direttamente dal disco di distribuzione, laddove possibile, le unità DVD moderne hanno una larghezza di banda molto elevata. In terzo luogo, è consigliabile implementare l'installazione su richiesta nei titoli per ridurre o eliminare il processo di installazione e consentire agli utenti di entrare nel gioco nel minor tempo possibile. Per ulteriori informazioni sull'installazione su richiesta, vedere [Install-on-demand per i giochi](/windows/desktop/DxTechArts/install-on-demand-for-games).

Per altre indicazioni sull'installazione dei giochi, vedere [semplificare l'installazione del gioco](/windows/desktop/DxTechArts/simplifying-game-installation).

## <a name="lack-of-consideration-of-physical-memory"></a>Mancanza di considerazioni sulla memoria fisica

A causa della grande variabilità dell'hardware del PC sul mercato, i titoli usano in genere i test di configurazione ad hoc per selezionare le impostazioni predefinite per il livello di dettaglio grafico. Alcuni dei titoli che abbiamo visto usano le dimensioni della memoria video in questi test, ma non è possibile metterli in correlazione con le dimensioni della memoria fisica. Per gestire le situazioni di dispositivo smarrito, la maggior parte della memoria del video (la VRAM locale sulla scheda e l'apertura della memoria AGP non locale) deve essere supportata dalla memoria fisica, tramite l'uso di risorse gestite o strutture di dati personalizzate. Alcune schede video di fascia alta hanno dimensioni di VRAM che comportano la dimensione delle memorie della CPU di fascia bassa. In situazioni in cui il sistema ha una quantità di memoria fisica limitata rispetto alla scheda video, la maggior parte di tale VRAM non può essere utilizzata in modo efficace e devono essere configurate le impostazioni del dettaglio più basso.

## <a name="over-reliance-on-real-time-audio-sample-rate-conversion"></a>Over-Reliance sulla conversione della frequenza di campionamento audio Real-Time

Un'altra fonte comune di ustione del ciclo della CPU si verifica quando il sistema audio è necessario per convertire la velocità di riproduzione durante la combinazione nel buffer hardware. Con i driver Windows Driver Model (WDM), il formato del buffer hardware non è sotto il controllo dell'applicazione diretta, perché si tratta di una risorsa a livello di kernel. il formato viene invece selezionato in base al formato di qualità superiore di tutte le origini e alle capacità dell'hardware. Per impostazione predefinita, in Windows XP viene utilizzata una conversione della frequenza di campionamento di alta qualità per questo processo. se la maggior parte degli esempi audio richiedono una conversione della frequenza, verrà utilizzata una parte significativa dei cicli della CPU.

È consigliabile creare tutti i buffer DirectSound con la stessa frequenza di campionamento. Se si usano le funzioni di **Wave** di Microsoft Win32, è necessario usare anche una frequenza di campionamento coerente. Con i driver WDM, i buffer verranno tutti combinati dal kernel e se si usa una frequenza di campionamento superiore per alcuni di essi, le frequenze di campionamento di tutte le altre verranno convertite in modo da corrispondere. Si noti che ciò implica l'uso della stessa frequenza di riproduzione per tutti gli esempi audio, inclusi i buffer di decompressione audio di streaming. L'impostazione della frequenza del buffer primario non ha alcun effetto a meno che non si tratti di una destinazione Windows 98 o Windows Millennium Edition.

> [!Note]  
> In Windows Vista e versioni successive del sistema operativo, DirectSound e **Wave** out usano l' [API di sessione audio (WASAPI) di Windows](/windows/desktop/CoreAudio/wasapi) per tutti gli output audio.

 

## <a name="fragmention-of-virtual-memory"></a>Frammentazione della memoria virtuale

Sono stati riscontrati numerosi problemi recenti relativi al limite di 32 bit per lo spazio di memoria del processo. Sebbene i 2 GB di spazio degli indirizzi virtuali per i processi in modalità utente siano stati più che adeguati storicamente, l'utilizzo elevato di file mappati alla memoria di grandi dimensioni, allocatori di memoria personalizzati e dimensioni di VRAM crescenti (che devono essere mappate nello spazio del processo) ha iniziato a causare situazioni in cui le allocazioni dello spazio di memoria virtuale hanno esito negativo. Alcune dll non Microsoft usano posizioni di avvio fisso al centro dello spazio degli indirizzi virtuali, causando la frammentazione che comporta allocazioni non riuscite.

Questi problemi vengono spesso visualizzati quando il gioco usa uno schema di allocazione di memoria personalizzato che tenta di allocare un grande blocco continuo di spazio di memoria virtuale. Si consiglia di scrivere gli allocatori in modo che richiedano parti più ragionevolmente dimensionate dello spazio degli indirizzi virtuali in base alle esigenze. Ad esempio, richiedendo 64 o 256 MB alla volta, ma non 1 GB. È tuttavia necessario prestare attenzione a non causare ulteriori frammenti. L'avvento di sistemi operativi e hardware a 64 bit contribuirà a questi problemi in futuro, ma è necessario prestare attenzione ai sistemi a 32 bit correnti.

## <a name="manipulation-of-the-floating-point-control-word"></a>Manipolazione della parola di controllo Floating-Point

Come supporto per il debug, alcuni sviluppatori hanno attivato le eccezioni sull'unità a virgola mobile (FPU) tramite modifiche della parola di controllo a virgola mobile. Questa operazione è molto problematica e potrebbe causare l'arresto anomalo del processo. Proprio come la convenzione di chiamata richiede che il registro ebx venga mantenuto, la maggior parte del sistema presuppone che la FPU si trovi in uno stato predefinito, restituirà risultati ragionevoli e non genererà eccezioni. I driver e altri componenti di sistema spesso calcolano i risultati in base al presupposto che i valori di errore standard verranno visualizzati nei registri per le condizioni non valide, ma se le eccezioni sono abilitate, queste non verranno gestite e provocheranno arresti anomali.

Direct3D imposterà l'unità a virgola mobile su precisione singola, arrotondata al più vicino come parte dell'inizializzazione per il thread chiamante, a meno che non \_ \_ venga usato il flag D3DCREATE FPU Preserve, nel qual caso la parola di controllo a virgola mobile non viene toccata. Poiché la parola di controllo è un'impostazione per thread, assicurarsi che tutti i thread dell'applicazione siano impostati sulla modalità a precisione singola per ottimizzare le prestazioni. Tenere presente che la chiamata a [**\_ control87**](https://msdn.microsoft.com/library/e9b52ceh(v=VS.71).aspx) non è valida per la codifica x64 nativa, che usa esclusivamente SSE ed è estremamente costosa nell'architettura basata su PowerPC della CPU Xbox 360.

> [!Note]  
> Se si modifica la parola di controllo, usare [**\_ controlfp \_ s**](https://msdn.microsoft.com/library/c9676k6h(v=VS.80).aspx) e tenere presente che per le piattaforme x64 non è possibile modificare la precisione a virgola mobile tramite la parola di controllo.

 

In tutte le librerie in cui è necessario avere regole di arrotondamento diverse o altri comportamenti, ad esempio la gestione di vertex shader o la compilazione di software, viene salvata e ripristinata la parola di controllo. Se un gioco deve usare l'arrotondamento non standard o le eccezioni FPU, deve salvare e ripristinare la parola di controllo a virgola mobile ed è necessario assicurarsi che non chiami codice esterno che non è stato dimostrato di essere sicuro da questi problemi, incluse le API di sistema.

## <a name="optional-installation-of-the-directx-runtime"></a>Installazione facoltativa di DirectX Runtime

Un numero di giochi chiede all'utente se installare DirectX. Questa operazione può causare problemi se l'utente presuppone che il sistema abbia installato la versione più recente di DirectX Redistributable e ne ignori l'installazione e, successivamente, l'installazione continua correttamente. Se il gioco richiede una versione specifica di D3DX o altre funzionalità aggiornate che non sono state installate, il gioco non funzionerà e l'utente sarà molto frustrato.

Si consiglia vivamente al programma di installazione del gioco di installare in modo invisibile all'utente DirectX ridistribuibile su cui è stato compilato il gioco. Il processo di installazione di DirectX è progettato in modo da verificare se è necessario aggiornare qualsiasi elemento e restituisce rapidamente un risultato in caso contrario. Non è quindi necessario richiedere all'utente di installare DirectX.

Un'installazione invisibile all'utente di DirectX può essere eseguita eseguendo questo comando dal pacchetto di installazione: **dxsetup.exe/Silent**

Inoltre, le dimensioni effettive della cartella ridistribuibile possono essere configurate in modo da includere solo i file CAB effettivamente necessari per le piattaforme di destinazione del gioco e l'utilizzo.

> [!Note]  
> Prima di usare **Dxsetup**, leggere [installazione non diretta](https://walbourn.github.io/).

 

## <a name="excessive-use-of-thread-synchronization"></a>Utilizzo eccessivo della sincronizzazione dei thread

Durante la profilatura dei giochi, spesso gli hotspot più frequenti sono correlati all'immissione e all'uscita dalle sezioni critiche. Con la prevalenza delle CPU multicore, l'uso del multithreading nei giochi è aumentato notevolmente e molte implementazioni si basano su un utilizzo intensivo della sincronizzazione dei thread. Il tempo di CPU necessario per eseguire una sezione critica anche senza conflitti è piuttosto significativo e tutte le altre forme di sincronizzazione dei thread sono ancora più onerose. Quindi, è necessario prestare attenzione per ridurre al minimo l'uso di queste primitive.

Un'origine comune di una sincronizzazione eccessiva nei giochi è l'uso di [D3DCREATE \_ multithreading](/windows/desktop/direct3d9/d3dcreate). Questo flag, rendendo thread-safe Direct3D per il rendering da più thread, accetta un approccio molto prudente, ottenendo un sovraccarico di sincronizzazione elevato. I giochi devono evitare questo flag. Progettare invece il motore in modo che tutte le comunicazioni con Direct3D provengano da un singolo thread e che tutte le comunicazioni tra i thread vengano gestite direttamente. Per ulteriori informazioni sulla progettazione di giochi multithread, vedere l'articolo relativo alla [codifica di più core in Xbox 360 e Microsoft Windows](/windows/desktop/DxTechArts/coding-for-multiple-cores).

## <a name="use-of-rdtsc"></a>Uso di RDTSC

Non è consigliabile usare l'istruzione x86 **RDTSC** . **RDTSC** non riesce a calcolare correttamente l'intervallo di tempo in alcuni schemi di risparmio energia che modificano la frequenza della CPU in modo dinamico e in molte CPU multicore per le quali il contatore del ciclo non è sincronizzato tra i core. I giochi devono invece usare l'API [**QueryPerformanceCounter**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter) . Per ulteriori informazioni sui problemi relativi a **RDTSC** e sull'implementazione della temporizzazione ad alta risoluzione con **QueryPerformanceCounter**, vedere l'articolo relativo alla [temporizzazione dei giochi e ai processori multicore](/windows/desktop/DxTechArts/game-timing-and-multicore-processors).

 

 