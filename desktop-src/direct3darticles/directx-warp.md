---
title: Windows Guida a WARP (Advanced Rasterization Platform)
description: Questo articolo descrive Windows advanced rasterization platform (WARP) e gli aspetti seguenti di WARP.
ms.assetid: C40A96EB-64AA-46EB-85A9-7C996ABC8BFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab76fd68985069e6114cd7bbb0901eeba5d911eba574332b1dd2008f0375a5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745991"
---
# <a name="windows-advanced-rasterization-platform-warp-guide"></a>Windows Guida a WARP (Advanced Rasterization Platform)

Questo articolo descrive Windows advanced rasterization platform (WARP) e gli aspetti seguenti di WARP.

-   [Che cos'è WARP?](#what-is-warp)
-   [Vantaggi di WARP](#warp-benefits)
    -   [Rimozione della necessità di rasterizzatori software personalizzati](#removing-the-need-for-custom-software-rasterizers)
    -   [Abilitazione delle prestazioni massime dall'hardware grafico](#enabling-maximum-performance-from-graphics-hardware)
    -   [Abilitazione del rendering quando l'hardware Direct3D non è disponibile](#enabling-rendering-when-direct3d-hardware-is-not-available)
    -   [Sfruttare le risorse esistenti per il rendering software](#leveraging-existing-resources-for-software-rendering)
    -   [Abilitazione di scenari che non richiedono hardware grafico](#enabling-scenarios-that-do-not-require-graphics-hardware)
    -   [Completamento della piattaforma grafica DirectX](#completing-the-directx-graphics-platform)
-   [Funzionalità e requisiti warp](#warp-capabilities-and-requirements)
-   [Come usare WARP](#how-to-use-warp)
-   [Tipi di applicazione consigliati per WARP](#recommended-application-types-for-warp)
    -   [Giochi casuali](#casual-games)
    -   [Applicazioni non di gioco esistenti](#existing-non-gaming-applications)
    -   [Giochi per il rendering avanzato](#advanced-rendering-games)
    -   [Altre applicazioni](#other-applications)
-   [Architettura e prestazioni warp](#warp-architecture-and-performance)
-   [Conformità WARP](#warp-conformance)

## <a name="what-is-warp"></a>Che cos'è WARP?

WARP è un rasterizzatore software completamente conforme ad alta velocità. Si tratta di un componente della tecnologia grafica DirectX introdotta dal runtime direct3D 11. Il runtime Direct3D 11 viene installato in Windows 7, Windows Server 2008 R2 e Windows Vista con l'aggiornamento \[ KB971644. \] Windows 8, Windows 10, Windows Server 2012 & e Windows RT includono il runtime Direct3D 11.1, che ha una versione aggiornata di WARP. Windows 10 Fall Creators Update (1709) include una versione di WARP che supporta sia i runtime Direct3D 11 che Direct3D 12.

## <a name="warp-benefits"></a>Vantaggi di WARP

WARP offre i vantaggi seguenti:

-   [Rimozione della necessità di rasterizzatori software personalizzati](#removing-the-need-for-custom-software-rasterizers)
-   [Abilitazione delle prestazioni massime dall'hardware grafico](#enabling-maximum-performance-from-graphics-hardware)
-   [Abilitazione del rendering quando l'hardware Direct3D non è disponibile](#enabling-rendering-when-direct3d-hardware-is-not-available)
-   [Sfruttare le risorse esistenti per il rendering software](#leveraging-existing-resources-for-software-rendering)
-   [Abilitazione di scenari che non richiedono hardware grafico](#enabling-scenarios-that-do-not-require-graphics-hardware)
-   [Completamento della piattaforma grafica DirectX](#completing-the-directx-graphics-platform)

### <a name="removing-the-need-for-custom-software-rasterizers"></a>Rimozione della necessità di rasterizzatori software personalizzati

WARP semplifica lo sviluppo rimuovendo la necessità di compilare un rasterizzatore software personalizzato e di ottimizzare l'applicazione anziché ottimizzare l'applicazione per l'hardware. Fornendo un singolo rasterizzatore software per utilizzo generico, non è più necessario scrivere algoritmi di rendering delle immagini in diversi modi per l'esecuzione su hardware o software con funzionalità e funzionalità diverse. È comunque possibile implementare gli algoritmi in più modi per ottenere prestazioni o scalabilità migliori. Tuttavia, non è necessario modificare l'api o l'architettura di rendering usata per implementare tali algoritmi. Al contrario, è possibile concentrarsi sulla creazione di un'applicazione Direct3D 10 o successiva che avrà lo stesso aspetto e le prestazioni su hardware o nel software.

### <a name="enabling-maximum-performance-from-graphics-hardware"></a>Abilitazione delle prestazioni massime dall'hardware grafico

Quando un'applicazione viene ottimizzata per l'esecuzione efficiente nell'hardware, verrà eseguita in modo efficiente anche in WARP. Anche il contrario è vero; Qualsiasi applicazione ottimizzata per l'esecuzione in WARP avrà prestazioni molto performa erre sull'hardware. Le applicazioni che usano Direct3D 10 e versioni successive in modo inefficiente potrebbero non essere ridimensionate in modo efficiente su hardware diverso. WARP ha profili di prestazioni simili all'hardware, quindi l'ottimizzazione di un'applicazione per batch di grandi dimensioni, la riduzione al minimo delle modifiche di stato, la rimozione dei punti di sincronizzazione o dei blocchi trarrà vantaggio sia dall'hardware che da WARP.

### <a name="enabling-rendering-when-direct3d-hardware-is-not-available"></a>Abilitazione del rendering quando l'hardware Direct3D non è disponibile

WARP consente il rendering rapido in diverse situazioni in cui le implementazioni hardware non sono desiderabili o non disponibili, tra cui:

-   Quando l'utente non dispone di hardware compatibile con Direct3D
-   Quando un'applicazione viene eseguita come servizio o in un ambiente server
-   Quando un'applicazione vuole riservare le risorse hardware Direct3D per altri usi
-   Quando una scheda video non è installata
-   Quando un driver video non è disponibile o non funziona correttamente
-   Quando la memoria di una scheda video è insufficiente, si blocca o sono necessarie troppe risorse di sistema per l'inizializzazione

### <a name="leveraging-existing-resources-for-software-rendering"></a>Sfruttare le risorse esistenti per il rendering software

Esiste un'enorme community, molti libri, siti Web, SDK, esempi, white paper, mailing list e altre risorse che consentono di sfruttare i vantaggi del rendering delle immagini basato su shader Direct3D 10 e versioni successive. Con WARP come fallback software, è possibile usare le conoscenze esistenti sull'hardware per migliorare le prestazioni dell'applicazione quando viene eseguita con hardware o software. Inoltre, molti strumenti eccellenti dei fornitori di schede grafiche e di DirectX SDK consentono di progettare, compilare, sviluppare, eseguire il debug e analizzare i problemi di prestazioni delle applicazioni grafiche. Questi strumenti e conoscenze possono ora essere utili per lo sviluppo di applicazioni destinato sia all'hardware che al software quando si usa WARP.

### <a name="enabling-scenarios-that-do-not-require-graphics-hardware"></a>Abilitazione di scenari che non richiedono hardware grafico

Vari algoritmi e applicazioni (algoritmi di elaborazione delle immagini, stampa, comunicazione remota, PC virtuali e altri emulatori, rendering dei caratteri di alta qualità, grafici, grafici e così via) sono stati in genere ottimizzati per la CPU perché non dipendono dall'hardware. Con WARP è possibile usare una singola architettura che esegue questi algoritmi e applicazioni e che può essere eseguita completamente nel software. tuttavia, se è disponibile l'accelerazione hardware, è possibile sfruttarla.

### <a name="completing-the-directx-graphics-platform"></a>Completamento della piattaforma grafica DirectX

WARP consente di accedere a tutte le funzionalità grafiche direct3D 10 e successive anche nei computer senza hardware grafico Direct3D 10 e versioni successive. Direct3D 10 ha rimosso i bit di funzionalità (tappi); ciò significa che non è più necessario verificare se le funzionalità grafiche sono disponibili dall'hardware grafico perché Direct3D 10 e versioni successive garantiscono questa disponibilità. È ora possibile usare tutte le funzionalità di un'ampia gamma di schede video sapendo che l'applicazione si comporterà e avrà lo stesso aspetto ovunque. È possibile ridimensionare le prestazioni di queste applicazioni disabilitando semplicemente le costose funzionalità grafiche nelle schede video di fascia bassa o il rendering in destinazioni più piccole.

## <a name="warp-capabilities-and-requirements"></a>Funzionalità e requisiti warp

WARP supporta completamente tutte le funzionalità direct3D 10 e 10.1. Ad esempio, WARP supporta le funzionalità più importanti seguenti:

-   Tutti i requisiti di precisione delle specifiche Direct3D 10 e 10.1
-   Direct3D 11 se usato con i livelli di funzionalità \_ 9 1, 9 \_ 2, 9 \_ 3, 10 \_ 0 e 10 \_ 1 (per [**\_ \_**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)altre informazioni sui livelli di funzionalità, vedere D3D FEATURE LEVEL )
-   Tutti i formati di trama facoltativi, ad esempio destinazioni di rendering multicampionamento e campionamento da superfici float
-   Antialiasing, rendering di alta qualità fino a 8x multisample antialiasing (MSAA)
-   Filtro anisotropo
-   Applicazioni a 32 e 64 bit e applicazioni a 32 bit con informazioni su indirizzi di grandi dimensioni

Quando si installa l'aggiornamento della piattaforma [Windows 7](https://support.microsoft.com/kb/2670838) in Windows 7 SP1 o Windows Server 2008 R2 SP1, tale sistema operativo include quindi il runtime Direct3D 11.1 e [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) una versione di WARP che supporta Direct3D 11.x se usato con i livelli di funzionalità \_ 9 1, 9 \_ 2, 9 \_ 3, 10 \_ 0, 10 \_ 1 e 11 \_ 0.

Windows 8, Windows 10, Windows Server 2012 & e Windows RT includono il runtime Direct3D 11.1 e una nuova versione di WARP. Questa versione supporta Direct3D 11.x [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) se usata con i livelli di funzionalità \_ 9 1, 9 \_ 2, 9 \_ 3, 10 \_ 0, \_ 10 1, 11 0 e \_ 11 \_ 1.

Windows 10 Fall Creators Update (1709) include una nuova versione di WARP che supporta i livelli di funzionalità [Direct3D 12](../direct3d12/direct3d-12-graphics.md) 12 0 e \_ 12 \_ 1. 

I requisiti minimi del computer per WARP sono gli stessi di Windows Vista, in particolare:

-   CPU minima a 800 MHz
-   MMX, SSE o SSE2 non è obbligatorio
-   Almeno 512 MB di RAM

## <a name="how-to-use-warp"></a>Come usare WARP

I componenti Direct3D 10, 10.1, 11 e 12 possono usare un tipo di driver aggiuntivo che è possibile specificare quando si crea il dispositivo, ad esempio quando si chiama la [**funzione D3D11CreateDevice.**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) Questo tipo di driver è [**D3D10 \_ DRIVER \_ TYPE \_ WARP**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type) o [**D3D \_ DRIVER TYPE \_ \_ WARP**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type). Quando si specifica questo tipo di driver, il runtime crea un dispositivo WARP e non inizializza un dispositivo hardware.

Poiché WARP usa la stessa interfaccia software per Direct3D del rasterizzatore di riferimento, qualsiasi applicazione Direct3D in grado di supportare l'esecuzione con il rasterizzatore di riferimento può essere testata usando WARP. Per usare WARP, rinominare D3d10warp.dll in D3d10ref.dll e posizionarlo nella stessa cartella dell'esempio o dell'applicazione. Successivamente, quando si passa a ref, viene visualizzato il rendering WARP.

Se si rinomina WARP in D3d10ref.dll e lo si posiziona in C: Programmi \\ (x86) \\ Microsoft DirectX SDK (giugno 2010) Samples \\ \\ C++ \\ Direct3D \\ Bin \\ x86, è possibile eseguire tutti gli esempi DirectX su WARP, facendo clic sul pulsante "Toggle Ref" nell'esempio o eseguendo l'esempio con /ref specificato nella riga di comando.

## <a name="recommended-application-types-for-warp"></a>Tipi di applicazione consigliati per WARP

Tutte le applicazioni che possono usare Direct3D possono usare WARP. Sono inclusi i tipi di applicazioni seguenti:

-   [Giochi casuali](#casual-games)
-   [Applicazioni non di gioco esistenti](#existing-non-gaming-applications)
-   [Giochi per il rendering avanzato](#advanced-rendering-games)
-   [Altre applicazioni](#other-applications)

### <a name="casual-games"></a>Giochi casuali

I giochi hanno in genere requisiti di rendering semplici. Tuttavia, richiedono anche l'uso di effetti visivi straordinari che potrebbero richiedere l'accelerazione hardware. La maggior parte dei titoli di gioco più venduti Windows sono simulazioni o giochi casuali, nessuno dei quali richiede grafica ad alte prestazioni. Tuttavia, entrambi gli stili di gioco traggono grande vantaggio dalla grafica moderna basata su shader e dalla possibilità di ridimensionare l'hardware.

### <a name="existing-non-gaming-applications"></a>Applicazioni non di gioco esistenti

Una grande quantità di applicazioni grafiche richiede un numero minimo di percorsi di codice nel livello di rendering. WARP consente a queste applicazioni di implementare un singolo percorso di codice Direct3D che può avere come destinazione un numero elevato di configurazioni di computer.

### <a name="advanced-rendering-games"></a>Giochi per il rendering avanzato

Gli sviluppatori di giochi potrebbero voler isolare gli errori di rendering specifici della scheda grafica o del driver. Pertanto, tutti i giochi, anche i giochi estremamente impegnativi dal punti di vista grafico, possono trarre vantaggio dalla possibilità di eseguire il rendering del contenuto usando WARP. È possibile usare WARP per verificare se eventuali elementi visivi rilevati sono errori di rendering o problemi con l'hardware o i driver.

### <a name="other-applications"></a>Altre applicazioni

Le applicazioni di destinazione per WARP includono anche quelle che potrebbero attualmente non usare Direct3D 10 o Direct3D 10.1. Queste applicazioni di destinazione includono applicazioni che devono sempre funzionare in tutti i computer, applicazioni di elaborazione di immagini che non scrivono versioni CPU e GPU di algoritmi di elaborazione delle immagini, algoritmi di elaborazione delle immagini in cui la velocità o l'uso della GPU non è fondamentale, ad esempio la stampa, ed emulatori e ambienti virtuali che visualizzano grafica 3D avanzata.

## <a name="warp-architecture-and-performance"></a>Architettura e prestazioni di WARP

WARP si basa sulla codebase del rasterizzatore di riferimento. Pertanto, WARP usa la stessa interfaccia software sia per Direct3D 10 e versioni successive che per DXGI. WARP è incluso in Windows 7 nel D3d10warp.dll, che si trova nelle Windows di sistema. Nei computer a 64 bit vengono installate due versioni di WARP, una versione x86 e una x64. La versione x64 potrebbe essere eseguita più velocemente in determinate circostanze perché il generatore di codice contenuto in WARP può sfruttare i registri aggiuntivi disponibili quando gli utenti eseguono applicazioni a 64 bit.

WARP contiene i due compilatori ad alta velocità e in tempo reale seguenti:

-   Compilatore di linguaggio intermedio di alto livello che converte il bytecode HLSL e lo stato di rendering corrente in un flusso ottimizzato di comandi vettoriali per le fasi geometry shader (GS), vertex shader (VS) e pixel shader (PS) della pipeline.
-   Generatore just-in-time code ad alte prestazioni che può usare questi comandi e generare codice assembly SSE2, SSE4.1, x86, x64, arm e arm64 ottimizzato.

WARP usa il pool di thread e la gestione complessa delle attività e il rilevamento delle dipendenze introdotto in Windows Vista per consentire la distribuzione efficiente di tutte le parti della pipeline di rendering tra i core CPU disponibili.

WARP usa il rendering posticipato. Ciò significa che WARP può eseguire il rendering in batch dei comandi in modo che la rasterizzazione si verifichi solo quando sono disponibili dati sufficienti per usare in modo efficiente tutte le risorse della CPU. Il lavoro sul thread principale dell'applicazione è ridotto al minimo per consentire all'applicazione di inviare i comandi il più rapidamente possibile. Se anche un'applicazione è multi-thread e usa il pool di thread, il lavoro verrà distribuito uniformemente tra WARP e l'applicazione.

Il generatore di codice WARP è stato ottimizzato per usare al meglio l'architettura della CPU moderna. WARP viene eseguito in tutti i computer che possono eseguire Windows Vista e sistemi operativi successivi, anche se il computer non supporta SSE. Tuttavia, WARP è stato ottimizzato per i computer che supportano SSE2. Contiene anche ottimizzazioni per architetture specifiche di processori AMD e Intel, nonché il supporto per le estensioni SSE 4.1.

WARP non richiede hardware grafico per l'esecuzione. Può essere eseguito anche in situazioni in cui l'hardware non è disponibile o non può essere inizializzato.

È probabile che le applicazioni e gli esempi progettati e creati per l'esecuzione su hardware Direct3D 10 e versioni successive senza alcuna conoscenza di WARP funzionino bene usando WARP. Tuttavia, è consigliabile ridurre il più possibile le impostazioni di qualità e la risoluzione per ottenere frequenze dei fotogrammi utilizzabili. È possibile usare WARP per sviluppare e ottimizzare applicazioni che vengono eseguite in modo ottimizzato su hardware e software.

Poiché WARP usa più core CPU, offre prestazioni ottimali nelle MODERNE CPU quad core. WARP viene inoltre eseguito in modo notevolmente più veloce nei computer in cui sono installate le estensioni SSE4.1. Microsoft ha eseguito test significativi e ottimizzazione delle prestazioni nei computer con otto o più core e SSE4.1 perché questi computer di fascia alta diventeranno più comuni per la durata dei sistemi operativi Windows 7 e versioni successive.

Quando WARP è in esecuzione nella CPU, è limitato rispetto a una scheda grafica in diversi modi. La velocità del bus front-side di una CPU è in genere di circa 10 GB/s o inferiore a 10 GB/s. Al contrario, una scheda grafica ha spesso memoria dedicata che usa da 20 a 100 GB/s o più di larghezza di banda grafica. L'hardware grafico dispone anche di unità a funzione fissa che possono eseguire attività complesse e costose, ad esempio il filtro delle trame, la decompressione del formato o le conversioni, in modo asincrono con un sovraccarico minimo o un costo di alimentazione ridotto. L'esecuzione di queste operazioni su una CPU tipica è dispendiosa sia in termini di consumo di energia che di cicli di prestazioni.

I numeri tipici delle prestazioni per un computer Quad Core Intel Penryn basato su 3,0 GHz mostrano che WARP in alcuni casi può avere prestazioni superiori rispetto alle GPU grafiche direct3D 10 e successive integrate di fascia bassa su una serie di benchmark. L'hardware grafico discreto di fascia bassa è in genere da 4 a 5 volte più veloce rispetto a WARP per l'esecuzione di questi benchmark. Queste GPU integrate o discrete di fascia bassa hanno un uso minimo delle risorse della CPU. Le schede grafiche di fascia media o di fascia alta sono notevolmente più veloci rispetto a WARP per molte applicazioni, in particolare quando un'applicazione può sfruttare il parallelismo e la larghezza di banda della memoria forniti da queste schede grafiche.

WARP non è una sostituzione per l'hardware grafico, in particolare perché le prestazioni ragionevoli di hardware discreto Direct3D 10 e versioni successive sono ora convenienti. L'obiettivo di WARP è consentire alle applicazioni di avere come destinazione hardware di livello Direct3D 10 senza avere percorsi di codice significativamente diversi o requisiti di test indipendentemente dal fatto che siano in esecuzione su hardware o software.

Le due tabelle seguenti mostrano i dati di esempio WARP con varie CPU e schede grafiche.

La prima tabella mostra i dati di esempio WARP con Direct3D 10 Crisis in esecuzione a 800x600 con tutte le impostazioni di qualità ai livelli più bassi:

| CPU                         | Ora   | Ave FPS | FPS minimo | Fotogramma minimo | FPS massimo | Frame massimo |
|-----------------------------|--------|---------|---------|-----------|---------|-----------|
| Core i7 8 core a 3,0 GHz     | 271.57 | 7,36    | 3,46    | 1966      | 15.01   | 995       |
| Penryn 4 core a 3,0 GHz      | 351.35 | 5.69    | 2.49    | 1967      | 10.95   | 980       |
| Penryn 2 Core a 3,0 GHz      | 573.98 | 3.48    | 1.35    | 1964      | 6.61    | 988       |
| Core 2 Duo a 2,6 GHz         | 707.19 | 2.83    | 0.81    | 1959      | 5.18    | 982       |
| Core 2 Duo a 2,4 GHz         | 763.25 | 2.62    | 0.76    | 1964      | 4.70    | 984       |
| Core 2 Duo a 2,1 GHz         | 908.87 | 2,20    | 0.64    | 1965      | 3.72    | 986       |
| Xeon 8 Core a 2,0 GHz        | 424.04 | 4.72    | 1.84    | 1967      | 9.56    | 988       |
| AMD FX74 4 Core a 3,0 GHz    | 583.12 | 3.43    | 1,41    | 1967      | 5.78    | 986       |
| Phenom 9550 4 Core a 2,2 GHz | 664.69 | 3.01    | 0.53    | 1959      | 5.46    | 987       |

La seconda tabella mostra i dati di esempio che eseguono lo stesso test in un'ampia gamma di schede grafiche:

| Scheda grafica         | Ora   | Ave FPS | FPS minimo | Fotogramma minimo | Max FPS | Frame massimo |
|-----------------------|--------|---------|---------|-----------|---------|-----------|
| NVIDIA 8800 GTS       | 23.58  | 84.80   | 60.78   | 1957      | 130.83  | 1022      |
| NVIDIA 8500 GT        | 47.63  | 41.99   | 25.67   | 1986      | 72.57   | 991       |
| NVIDIA Quadro 290     | 67.16  | 29.78   | 18.19   | 1969      | 49.87   | 1017      |
| NVIDIA 8400 GS        | 59.01  | 33.89   | 21.22   | 1962      | 51.82   | 1021      |
| ATI 3400              | 53.79  | 37.18   | 22.97   | 618       | 59.77   | 1021      |
| ATI 3200              | 67.19  | 29.77   | 18.91   | 1963      | 45.74   | 980       |
| ATI 2400 PRO          | 67.04  | 29.83   | 17.97   | 606       | 45.91   | 987       |
| Intel DX10 Integrated | 386.94 | 5.17    | 1.74    | 1974      | 16.22   | 995       |

## <a name="warp-conformance"></a>Conformità WARP

WARP supera tutti i test Windows standard di conformità WHQL (Hardware Quality Labs) per la convalida dei dispositivi hardware Direct3D.

WARP è stato testato su una suite di applicazioni e benchmark Direct3D 10 e Direct3D 10.1 e su esempi sdk di DirectX, NVIDIA e AMD.

WARP ha usato lo strumento di debug e analisi [PIX](https://msdn.microsoft.com/library/ee417062(v=VS.85).aspx) per Windows nei test; Microsoft dispone di un'ampia libreria di acquisizioni a frame singolo di applicazioni usate per confrontare hardware e WARP. La maggior parte delle immagini appare quasi identica tra hardware e WARP; Se a volte si verificano piccole differenze, si trovano all'interno delle tolleranze definite dalla specifica Direct3D 10.