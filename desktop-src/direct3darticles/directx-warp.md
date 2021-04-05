---
title: Guida di Windows Advanced Rasterizzation Platform (WARP)
description: Questo articolo descrive la piattaforma di rasterizzazione avanzata di Windows (WARP) e i seguenti aspetti di WARP.
ms.assetid: C40A96EB-64AA-46EB-85A9-7C996ABC8BFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c09c29dd7b935542f0238cde0a71cbc97fce23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729242"
---
# <a name="windows-advanced-rasterization-platform-warp-guide"></a>Guida di Windows Advanced Rasterizzation Platform (WARP)

Questo articolo descrive la piattaforma di rasterizzazione avanzata di Windows (WARP) e i seguenti aspetti di WARP.

-   [Che cos'è WARP?](#what-is-warp)
-   [Vantaggi di DISTORSIONe](#warp-benefits)
    -   [Eliminazione della necessità di rasterizzatori software personalizzati](#removing-the-need-for-custom-software-rasterizers)
    -   [Abilitazione delle prestazioni massime dall'hardware grafico](#enabling-maximum-performance-from-graphics-hardware)
    -   [Abilitazione del rendering quando l'hardware Direct3D non è disponibile](#enabling-rendering-when-direct3d-hardware-is-not-available)
    -   [Uso delle risorse esistenti per il rendering del software](#leveraging-existing-resources-for-software-rendering)
    -   [Abilitazione di scenari che non richiedono hardware grafico](#enabling-scenarios-that-do-not-require-graphics-hardware)
    -   [Completamento della piattaforma grafica DirectX](#completing-the-directx-graphics-platform)
-   [Funzionalità e requisiti di DISTORSIONe](#warp-capabilities-and-requirements)
-   [Come usare WARP](#how-to-use-warp)
-   [Tipi di applicazione consigliati per WARP](#recommended-application-types-for-warp)
    -   [Giochi casuali](#casual-games)
    -   [Applicazioni non di gioco esistenti](#existing-non-gaming-applications)
    -   [Giochi di rendering avanzati](#advanced-rendering-games)
    -   [Altre applicazioni](#other-applications)
-   [Architettura e prestazioni di WARP](#warp-architecture-and-performance)
-   [Conformità a WARP](#warp-conformance)

## <a name="what-is-warp"></a>Che cos'è WARP?

WARP è un rasterizzatore software completamente conforme e ad alta velocità. Si tratta di un componente della tecnologia grafica DirectX introdotta dal runtime di Direct3D 11. Il runtime di Direct3D 11 è installato in Windows 7, Windows Server 2008 R2 e Windows Vista con l' \[ aggiornamento di KB971644 \] . Windows 8, Windows 10, Windows Server 2012 & precedente e Windows RT includono il runtime Direct3D 11,1, che ha una versione aggiornata di WARP. Windows 10 Fall Creators Update (1709) include una versione di WARP che supporta runtime Direct3D 11 e Direct3D 12.

## <a name="warp-benefits"></a>Vantaggi di DISTORSIONe

WARP offre i vantaggi seguenti:

-   [Eliminazione della necessità di rasterizzatori software personalizzati](#removing-the-need-for-custom-software-rasterizers)
-   [Abilitazione delle prestazioni massime dall'hardware grafico](#enabling-maximum-performance-from-graphics-hardware)
-   [Abilitazione del rendering quando l'hardware Direct3D non è disponibile](#enabling-rendering-when-direct3d-hardware-is-not-available)
-   [Uso delle risorse esistenti per il rendering del software](#leveraging-existing-resources-for-software-rendering)
-   [Abilitazione di scenari che non richiedono hardware grafico](#enabling-scenarios-that-do-not-require-graphics-hardware)
-   [Completamento della piattaforma grafica DirectX](#completing-the-directx-graphics-platform)

### <a name="removing-the-need-for-custom-software-rasterizers"></a>Eliminazione della necessità di rasterizzatori software personalizzati

WARP semplifica lo sviluppo eliminando la necessità di creare un rasterizzatore software personalizzato e di ottimizzare l'applicazione per l'applicazione, anziché ottimizzare l'applicazione per l'hardware. Grazie a un singolo rasterizzatore software generico, non è più necessario scrivere algoritmi di rendering delle immagini in diversi modi per l'esecuzione su hardware o software con caratteristiche e funzionalità diverse. È comunque possibile implementare gli algoritmi in diversi modi per ottenere prestazioni o scalabilità migliori. Tuttavia, non è necessario modificare l'architettura dell'API o del rendering utilizzata per implementare tali algoritmi. Al contrario, è possibile concentrarsi sulla creazione di un'applicazione Direct3D 10 o versione successiva che apparirà lo stesso aspetto ed eseguirà correttamente l'hardware o il software.

### <a name="enabling-maximum-performance-from-graphics-hardware"></a>Abilitazione delle prestazioni massime dall'hardware grafico

Quando un'applicazione viene ottimizzata per essere eseguita in modo efficiente nell'hardware, viene eseguita in modo efficiente anche su WARP. È vero anche il contrario. tutte le applicazioni ottimizzate per essere eseguite correttamente in WARP si adatteranno correttamente all'hardware. Le applicazioni che utilizzano Direct3D 10 e versioni successive non possono essere ridimensionate in modo efficiente su hardware diverso. WARP presenta un profilo di prestazioni simile a quello dell'hardware, quindi l'ottimizzazione di un'applicazione per batch di grandi dimensioni, riducendo al minimo le modifiche di stato, rimuovendo i punti di sincronizzazione o i blocchi può trarre vantaggio sia dall'hardware

### <a name="enabling-rendering-when-direct3d-hardware-is-not-available"></a>Abilitazione del rendering quando l'hardware Direct3D non è disponibile

WARP consente il rendering rapido in diverse situazioni in cui le implementazioni hardware sono indesiderate o non disponibili, tra cui:

-   Quando l'utente non dispone di hardware idoneo per Direct3D
-   Quando un'applicazione viene eseguita come servizio o in un ambiente server
-   Quando un'applicazione vuole riservare le risorse hardware Direct3D per altri usi
-   Quando una scheda video non è installata
-   Quando un driver video non è disponibile o non funziona correttamente
-   Quando una scheda video ha esaurito la memoria, si blocca o richiede un numero eccessivo di risorse di sistema da inizializzare

### <a name="leveraging-existing-resources-for-software-rendering"></a>Uso delle risorse esistenti per il rendering del software

Sono disponibili una grande community, molti libri, siti Web, SDK, esempi, white paper, liste di distribuzione e altre risorse che consentono di sfruttare i vantaggi offerti da Direct3D 10 e versioni successive per il rendering delle immagini basate su shader. Con WARP come fallback software, è possibile usare le informazioni esistenti sull'hardware per migliorare le prestazioni dell'applicazione quando viene eseguita con hardware o software. Inoltre, molti strumenti eccellenti dei fornitori di schede grafiche e di DirectX SDK consentono di progettare, compilare, sviluppare, eseguire il debug e analizzare i problemi di prestazioni delle applicazioni grafiche. Questi strumenti e conoscenze ora possono trarre vantaggio dallo sviluppo di applicazioni destinate a hardware e software quando si usa la DISTORSIONe.

### <a name="enabling-scenarios-that-do-not-require-graphics-hardware"></a>Abilitazione di scenari che non richiedono hardware grafico

Diversi algoritmi e applicazioni (algoritmi di elaborazione delle immagini, stampa, comunicazione remota, PC virtuali e altri emulatori, rendering di tipi di carattere di qualità elevata, grafici, grafici e così via) sono in genere ottimizzati per la CPU, perché non dipendono dall'hardware. Con WARP è possibile usare una singola architettura che esegue questi algoritmi e applicazioni e che può essere eseguita completamente nel software; Tuttavia, se è disponibile l'accelerazione hardware, è possibile sfruttarla.

### <a name="completing-the-directx-graphics-platform"></a>Completamento della piattaforma grafica DirectX

WARP consente di accedere a tutte le funzionalità grafiche Direct3D 10 e successive anche nei computer senza l'hardware grafico Direct3D 10 e versioni successive. Direct3D 10 ha rimosso le funzionalità bits (CAPS); ovvero, non è più necessario verificare se le funzionalità grafiche sono disponibili dall'hardware grafico perché Direct3D 10 e versioni successive garantiscono questa disponibilità. È ora possibile usare tutte le funzionalità di una vasta gamma di schede video, sapendo che la loro applicazione si comporterà e sarà sempre in tutto il mondo. È possibile ridimensionare le prestazioni di queste applicazioni semplicemente disabilitando le costose funzionalità grafiche sulle schede video di fascia bassa o il rendering a destinazioni più piccole.

## <a name="warp-capabilities-and-requirements"></a>Funzionalità e requisiti di DISTORSIONe

WARP supporta completamente tutte le funzionalità Direct3D 10 e 10,1. Ad esempio, WARP supporta le seguenti funzionalità più importanti:

-   Tutti i requisiti di precisione della specifica Direct3D 10 e 10,1
-   Direct3D 11 se usato con i livelli di funzionalità 9 \_ 1, 9 \_ 2, 9 \_ 3, 10 \_ 0 e 10 \_ 1 (per altre informazioni sui livelli di funzionalità, vedere [**\_ \_ livello di funzionalità D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level))
-   Tutti i formati di trama facoltativi, ad esempio le destinazioni di rendering multicampionamento e il campionamento da superfici float
-   Anti-aliasing, elevata qualità di rendering fino a 8 anti-aliasing di multicampionamento (MSAA)
-   Filtro anisotropico
-   applicazioni a 32 bit e a 64 bit e applicazioni a 32 bit compatibili con indirizzi di grandi dimensioni

Quando si installa l' [aggiornamento della piattaforma per Windows 7](https://support.microsoft.com/kb/2670838) in Windows 7 SP1 o windows Server 2008 R2 SP1, il sistema operativo include quindi il runtime Direct3D 11,1 e una versione di Warp che supporta Direct3D 11. x quando viene usato con i [livelli di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ 1, 9 \_ 2, 9 \_ 3, 10 \_ 0, 10 \_ 1 e 11 \_ 0.

Windows 8, Windows 10, Windows Server 2012 & versioni precedenti e Windows RT includono il runtime Direct3D 11,1 e una nuova versione di WARP. Questa versione supporta Direct3D 11. x quando viene usata con i [livelli di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ 1, 9 \_ 2, 9 \_ 3, 10 \_ 0, 10 \_ 1, 11 \_ 0 e 11 \_ 1.

Windows 10 Fall Creators Update (1709) include una nuova versione di WARP che supporta i livelli di funzionalità di [Direct3D 12](../direct3d12/direct3d-12-graphics.md) 12 \_ 0 e 12 \_ 1. 

I requisiti minimi del computer per WARP sono identici a quelli di Windows Vista, in particolare:

-   CPU minima 800 MHz
-   MMX, SSE o SSE2 non è obbligatorio
-   Minimo 512 MB di RAM

## <a name="how-to-use-warp"></a>Come usare WARP

I componenti Direct3D 10, 10,1, 11 e 12 possono usare un tipo di driver aggiuntivo che è possibile specificare quando si crea il dispositivo, ad esempio quando si chiama la funzione [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) . Questo tipo di driver è il tipo di driver [**D3D10 \_ \_ \_ Warp**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type) o il [**tipo di \_ driver D3D \_ \_ Warp**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type). Quando si specifica questo tipo di driver, il runtime crea un dispositivo WARP e non Inizializza un dispositivo hardware.

Poiché WARP usa la stessa interfaccia software per Direct3D come avviene per l'rasterizzazione dei riferimenti, qualsiasi applicazione Direct3D che può supportare l'esecuzione con l'rasterizzazione dei riferimenti può essere testata usando WARP. Per usare WARP, rinominare D3d10warp.dll in D3d10ref.dll e inserirlo nella stessa cartella dell'esempio o dell'applicazione. Quindi, quando si passa a ref, viene visualizzato il rendering WARP.

Se si rinomina WARP in D3d10ref.dll e lo si inserisce in C: \\ Program Files (x86) \\ Microsoft DirectX SDK (giugno 2010) \\ Samples \\ C++ \\ Direct3D \\ bin \\ x86, è possibile eseguire tutti gli esempi di DirectX su Warp, facendo clic sul pulsante "attiva/Rimuovi Ref" nell'esempio oppure eseguendo l'esempio con/ref specificato nella riga di comando.

## <a name="recommended-application-types-for-warp"></a>Tipi di applicazione consigliati per WARP

Tutte le applicazioni che possono usare Direct3D possono usare la DISTORSIONe. Sono inclusi i tipi di applicazioni seguenti:

-   [Giochi casuali](#casual-games)
-   [Applicazioni non di gioco esistenti](#existing-non-gaming-applications)
-   [Giochi di rendering avanzati](#advanced-rendering-games)
-   [Altre applicazioni](#other-applications)

### <a name="casual-games"></a>Giochi casuali

I giochi in genere hanno requisiti di rendering semplici. Tuttavia, richiedono anche l'utilizzo di effetti visivi impressionanti che potrebbero richiedere l'accelerazione hardware. La maggior parte dei migliori titoli dei giochi per Windows è costituita da simulazioni o giochi occasionali, nessuno dei quali richiede una grafica a prestazioni elevate. Tuttavia, entrambi gli stili dei giochi traggono molti vantaggi dai moderni elementi grafici basati su shader e dalla possibilità di ridimensionare l'hardware.

### <a name="existing-non-gaming-applications"></a>Applicazioni non di gioco esistenti

Una grande quantità di applicazioni grafiche richiede un numero minimo di percorsi di codice nel livello di rendering. WARP consente a queste applicazioni di implementare un singolo percorso di codice Direct3D che può essere destinato a un numero elevato di configurazioni di computer.

### <a name="advanced-rendering-games"></a>Giochi di rendering avanzati

Gli sviluppatori di giochi potrebbero voler isolare gli errori di rendering specifici del driver o della scheda grafica. Pertanto, tutti i giochi, anche i giochi estremamente complessi, possono trarre vantaggio dalla possibilità di eseguire il rendering del contenuto tramite WARP. È possibile utilizzare WARP per verificare se eventuali artefatti visivi individuati rilevano errori o problemi con l'hardware o i driver.

### <a name="other-applications"></a>Altre applicazioni

Le applicazioni di destinazione per WARP includono anche quelle che potrebbero non usare attualmente Direct3D 10 o Direct3D 10,1. Queste applicazioni di destinazione includono applicazioni che devono sempre funzionare su tutti i computer, le applicazioni di elaborazione di immagini che non scrivono versioni CPU e GPU degli algoritmi di elaborazione delle immagini, gli algoritmi di elaborazione delle immagini in cui la velocità o l'utilizzo della GPU non è fondamentale, ad esempio la stampa e gli emulatori e gli ambienti virtuali che visualizzano grafica 3D avanzata.

## <a name="warp-architecture-and-performance"></a>Architettura e prestazioni di WARP

WARP è basato sulla codebase di rasterizzazione dei riferimenti. WARP usa quindi la stessa interfaccia software per Direct3D 10 e versioni successive e DXGI. WARP è incluso in Windows 7 nella D3d10warp.dll, disponibile in cartelle di sistemi Windows. Due versioni di WARP sono installate in computer a 64 bit, una versione x86 e x64. La versione x64 potrebbe essere eseguita più velocemente in determinate circostanze perché il generatore di codice contenuto in WARP può sfruttare i registri aggiuntivi disponibili quando gli utenti eseguono applicazioni a 64 bit.

WARP contiene i seguenti due compilatori in tempo reale ad alta velocità:

-   Compilatore di linguaggio intermedio di alto livello che converte il bytecode HLSL e lo stato di rendering corrente in un flusso ottimizzato di comandi Vector per le fasi di geometria shader (GS), vertex shader (VS) e pixel shader (PS) della pipeline.
-   Il generatore di codice JIT a prestazioni elevate che può eseguire questi comandi e generare codice di assembly SSE2, SSE 4.1, x86, x64, ARM e arm64 ottimizzato.

WARP usa il pool di thread e la gestione delle attività complesse e il rilevamento delle dipendenze introdotti in Windows Vista per consentire la distribuzione efficiente di tutte le parti della pipeline di rendering tra i core CPU disponibili.

WARP usa il rendering posticipato. In altri casi, WARP può eseguire il rendering in batch dei comandi in modo che la rasterizzazione avvenga solo quando sono disponibili dati sufficienti per l'uso efficiente di tutte le risorse della CPU. Lavorare sul thread principale dell'applicazione è ridotto al minimo per consentire all'applicazione di inviare i comandi nel minor tempo possibile. Se un'applicazione è anche multithread e usa il pool di thread, il lavoro verrà distribuito uniformemente tra WARP e l'applicazione.

Il generatore di codice WARP è stato ottimizzato per sfruttare al meglio l'architettura della CPU moderna. WARP viene eseguito in tutti i computer in cui è possibile eseguire Windows Vista e sistemi operativi successivi, anche se il computer non supporta SSE. Tuttavia, WARP è stato ottimizzato per i computer che supportano SSE2. Contiene anche le ottimizzazioni per architetture specifiche di processori AMD e Intel, oltre al supporto per le estensioni SSE 4,1.

WARP non richiede l'esecuzione di hardware grafico. Può essere eseguito anche in situazioni in cui l'hardware non è disponibile o non può essere inizializzato.

Le applicazioni e gli esempi progettati e creati per l'esecuzione su hardware Direct3D 10 e versioni successive senza alcuna conoscenza di DISTORSIONe probabilmente vengono eseguiti correttamente usando WARP. Tuttavia, è consigliabile ridurre il più possibile le impostazioni di qualità e la risoluzione per ottenere frequenze dei fotogrammi utilizzabili. È possibile utilizzare WARP per sviluppare e ottimizzare le applicazioni che vengono eseguite correttamente nell'hardware e nel software.

Poiché WARP usa più core CPU, offre prestazioni ottimali sulle CPU quad core moderne. WARP viene inoltre eseguito in modo molto più veloce nei computer in cui sono installate le estensioni SSE 4.1. Microsoft ha eseguito un'ottimizzazione significativa dei test e delle prestazioni nei computer con otto o più core e SSE 4.1, perché questi computer di fascia alta diventeranno più comuni durante la durata di Windows 7 e sistemi operativi successivi.

Quando WARP viene eseguito sulla CPU, è limitato rispetto a una scheda grafica in diversi modi. La velocità del bus front-end di una CPU è in genere di circa 10 GB/s. Al contrario, una scheda grafica spesso ha una memoria dedicata che usa da 20 a 100 GB/s o più di larghezza di banda grafica. L'hardware grafico dispone anche di unità a funzione fissa che possono eseguire attività complesse e costose, ad esempio il filtro della trama, la decompressione del formato o le conversioni, in modo asincrono con scarso sovraccarico o costi energetici. L'esecuzione di queste operazioni su una CPU tipica è dispendiosa in termini di consumo di energia e di cicli delle prestazioni.

I numeri di prestazioni tipici per un computer quad core a 3,0 GHz basato su Intel Penryn mostrano che la DISTORSIONe può in alcuni casi superare le GPU della grafica Direct3D 10 e successive integrate di fascia bassa su diversi benchmark. L'hardware grafico discreto di fascia bassa è in genere da 4 a 5 volte più veloce rispetto alla DISTORSIONe per l'esecuzione di questi benchmark. Queste GPU integrate o discrete di fascia bassa hanno un utilizzo minimo delle risorse della CPU. Le schede grafiche a metà o a fascia alta sono molto più veloci rispetto alla DISTORSIONe per molte applicazioni, in particolare quando un'applicazione può sfruttare il parallelismo e la larghezza di banda della memoria fornita da queste schede grafiche.

WARP non è un sostituto per l'hardware grafico, in particolare per l'esecuzione ragionevolmente dell'hardware discreto e di fascia bassa di Direct3D 10 e versioni successive, ora è poco costoso. L'obiettivo di WARP è quello di consentire alle applicazioni di usare hardware a livello Direct3D 10 senza avere percorsi di codice significativamente diversi o requisiti di test, indipendentemente dal fatto che vengano eseguiti su hardware o software.

Nelle due tabelle seguenti sono illustrati i dati di esempio WARP con varie CPU e schede grafiche.

La prima tabella mostra i dati di esempio WARP con Direct3D 10 Crysis in esecuzione a 800x600 con tutte le impostazioni di qualità ai livelli più bassi:

| CPU                         | Tempo   | FPS Ave | Min FPS | Fotogramma minimo | Numero massimo di FPS | Massimo frame |
|-----------------------------|--------|---------|---------|-----------|---------|-----------|
| Core i7 8 core a 3,0 GHz     | 271,57 | 7,36    | 3,46    | 1966      | 15,01   | 995       |
| Penryn 4 core a 3,0 GHz      | 351,35 | 5,69    | 2.49    | 1967      | 10,95   | 980       |
| Penryn 2 core a 3,0 GHz      | 573,98 | 3.48    | 1.35    | 1964      | 6,61    | 988       |
| Core 2 Duo a 2,6 GHz         | 707,19 | 2.83    | 0.81    | 1959      | 5.18    | 982       |
| Core 2 Duo a 2,4 GHz         | 763,25 | 2.62    | 0.76    | 1964      | 4,70    | 984       |
| Core 2 Duo a 2.1 GHz         | 908,87 | 2,20    | 0,64    | 1965      | 3.72    | 986       |
| Xeon 8 core a 2,0 GHz        | 424,04 | 4,72    | 1,84    | 1967      | 9,56    | 988       |
| AMD FX74 4 core @ 3.0 GHz    | 583,12 | 3.43    | 1,41    | 1967      | 5,78    | 986       |
| Phenom 9550 4 Core @ 2.2 GHz | 664,69 | 3,01    | 0,53    | 1959      | 5,46    | 987       |

La seconda tabella mostra i dati di esempio che eseguono lo stesso test in un'ampia gamma di schede grafiche:

| Scheda grafica         | Tempo   | FPS Ave | Min FPS | Fotogramma minimo | Numero massimo di FPS | Massimo frame |
|-----------------------|--------|---------|---------|-----------|---------|-----------|
| NVIDIA 8800 GTS       | 23,58  | 84,80   | 60,78   | 1957      | 130,83  | 1022      |
| NVIDIA 8500 GT        | 47,63  | 41,99   | 25,67   | 1986      | 72,57   | 991       |
| NVIDIA Quadro 290     | 67,16  | 29,78   | 18,19   | 1969      | 49,87   | 1017      |
| NVIDIA 8400 GS        | 59,01  | 33,89   | 21.22   | 1962      | 51,82   | 1021      |
| ATI 3400              | 53,79  | 37,18   | 22.97   | 618       | 59,77   | 1021      |
| ATI 3200              | 67,19  | 29,77   | 18,91   | 1963      | 45,74   | 980       |
| ATI 2400 PRO          | 67,04  | 29,83   | 17,97   | 606       | 45,91   | 987       |
| Intel DX10 integrato | 386,94 | 5.17    | 1,74    | 1974      | 16,22   | 995       |

## <a name="warp-conformance"></a>Conformità a WARP

WARP passa tutti i test standard di conformità di Windows Hardware Quality Labs (WHQL) per la convalida dei dispositivi hardware Direct3D.

WARP è stato testato su una suite di applicazioni e benchmark Direct3D 10 e Direct3D 10,1 e su esempi di SDK da DirectX, NVIDIA e AMD.

WARP ha usato lo strumento di analisi e debug di [pix](https://msdn.microsoft.com/library/ee417062(v=VS.85).aspx) per Windows nei test. Microsoft dispone di un'ampia libreria di acquisizioni a frame singolo di applicazioni utilizzate per il confronto tra hardware e WARP. La maggior parte delle immagini sembra quasi identica tra l'hardware e la DISTORSIONe; Se talvolta si verificano differenze minime, vengono rilevate all'interno delle tolleranze definite dalla specifica Direct3D 10.