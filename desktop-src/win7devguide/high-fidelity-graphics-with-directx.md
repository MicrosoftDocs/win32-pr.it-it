---
title: Grafica a fedeltà elevata con DirectX
description: Gli sviluppatori di applicazioni Windows hanno usato a lungo Microsoft DirectX per offrire grafica 3D di alta qualità e con accelerazione hardware.
ms.assetid: db555657-90b9-4db2-a0c2-bfaa526a8dd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda45f911293b9d31b9ae28d89c25ed93ce33696
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729858"
---
# <a name="high-fidelity-graphics-with-directx"></a>Grafica a fedeltà elevata con DirectX

Gli sviluppatori di applicazioni Windows hanno usato a lungo Microsoft DirectX per offrire grafica 3D di alta qualità e con accelerazione hardware. Al debutto della tecnologia nel 1995, gli sviluppatori potevano fornire grafica 3D di alta qualità per giochi e applicazioni di progettazione per giocatori e professionisti disposti a pagare una lavagna grafica 3D. A questo punto, anche i PC più convenienti includono hardware grafica 3D.

Per sfruttare i vantaggi di queste funzionalità grafiche, in Windows Vista è stata introdotta l'infrastruttura WDDM (Windows Display Driver Model) per DirectX che ha consentito a più applicazioni e servizi di condividere le risorse dell'unità di elaborazione grafica (GPU). Il Gestione finestre desktop (DWM) utilizza questa tecnologia per animare il cambio di attività in 3D, fornire immagini di anteprime dinamiche delle finestre delle applicazioni e fornire effetti vetro Windows Aero per le applicazioni desktop.

Windows 7 mette a disposizione degli sviluppatori di applicazioni anche altre funzionalità grafiche. Grazie a un nuovo set di DirectXAPIs, gli sviluppatori Microsoft Win32 possono sfruttare le innovazioni più recenti nelle GPU per aggiungere grafica, testo e immagini 2D e 3D veloci, scalabili e di alta qualità alle proprie applicazioni. Negli schermi *LCD* più recenti DirectXAPIs è in grado di visualizzare il contenuto del desktop e della finestra usando una profondità di colore maggiore di 8 bit per ogni componente colore.

Con DirectX, gli sviluppatori Win32 possono anche usare il parallelismo della GPU per calcoli generici, ad esempio l'elaborazione di immagini, ed è possibile eseguire il rendering in hardware DirectX 10, hardware DirectX 9, CPU o in un computer Windows remoto. Queste tecnologie sono state progettate per interagire con Windows Graphics Device Interface (GDI) e Windows GDI+, garantendo agli sviluppatori la possibilità di mantenere facilmente gli investimenti esistenti nel codice Win32. (Vedere [le novità di DirectX SDK di marzo 2009](/previous-versions//bb173043(v=vs.85))).

Queste funzionalità grafiche avanzate sono fornite dalle API basate su *com* seguenti:

-   [Direct2D](../direct2d/direct2d-portal.md) per il disegno di immagini 2D.
-   [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) per la disposizione e il rendering del testo.
-   [Componente di Windows Imaging](/windows/desktop/wic/-wic-lh) per l'elaborazione e la visualizzazione di immagini.
-   [Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics) per il disegno di immagini 3D.
-   [Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) per il disegno di immagini 3D e l'accesso alle tecnologie GPU di nuova generazione, come la suddivisione a mosaico, il supporto limitato per lo streaming di trame e l'elaborazione generale.
-   [Infrastruttura grafica DirectX (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) per la gestione di dispositivi di visualizzazione locali e remoti e risorse GPU e per garantire l'interoperabilità tra DirectX e GDI.

## <a name="direct2d"></a>Direct2D

Basato su Microsoft Direct3D 10, [Direct2D](../direct2d/direct2d-portal.md) offre agli sviluppatori Win32 la modalità immediata, le API 2D indipendenti dalla risoluzione, che sfruttano la potenza di hardware grafico di nuova generazione, ma interagiscono bene con le applicazioni GDI/GDI+ attuali e le applicazioni Direct3D 10. Direct2D fornisce un rendering 2D di alta qualità con prestazioni superiori a GDI e GDI+. Fornisce agli sviluppatori Win32 un controllo più preciso sulle risorse e sulla relativa gestione. Vedere [Direct2D](../direct2d/direct2d-portal.md).

## <a name="directwrite"></a>DirectWrite

Molte applicazioni attuali devono supportare il rendering di testo di alta qualità, i tipi di carattere di struttura indipendenti dalla risoluzione e il testo Unicode completo e il supporto del layout. [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), un nuovo componente DirectX, fornisce queste funzionalità e altro ancora:

-   Sistema di layout del testo indipendente dal dispositivo che migliora la leggibilità del testo nei documenti e nell'interfaccia utente.
-   Rendering di testo di alta qualità, sottopixel, *ClearType* che può utilizzare la tecnologia di rendering GDI, [Direct2D](../direct2d/direct2d-portal.md)o specifica dell'applicazione.
-   Testo con accelerazione hardware, se usato con [Direct2D](../direct2d/direct2d-portal.md).
-   Supporto per il testo in più formati.
-   Supporto per le funzionalità tipografiche avanzate dei tipi di carattere *OpenType* .
-   Supporto per il layout e il rendering del testo in tutte le lingue supportate.
-   Layout e rendering compatibili con GDI.

Il sistema dei tipi di carattere [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) consente l'utilizzo dei tipi di carattere in qualsiasi posizione, in cui gli utenti non devono eseguire un passaggio di installazione separato solo per usare un tipo di carattere e una gerarchia strutturale migliorata del raggruppamento di tipi di carattere per semplificare l'individuazione del tipo di carattere manuale o a livello di codice. Le API supportano la misurazione, il disegno e l'hit testing del testo in più formati. DirectWrite gestisce il testo in tutte le lingue supportate per le applicazioni globali e localizzate, basandosi sull'infrastruttura di linguaggio chiave disponibile in Windows 7. DirectWrite fornisce anche API di rendering del glifo di basso livello per gli sviluppatori che desiderano eseguire il proprio layout e l'elaborazione da Unicode a glifo. Vedere [DirectWrite](../directwrite/direct-write-portal.md).

## <a name="windows-imaging-component"></a>Componente Windows Imaging

In Windows Vista, il [componente Windows Imaging](/windows/desktop/wic/-wic-lh) introduce un framework estensibile per l'utilizzo di immagini e metadati di immagini. I formati di immagine supportati dal componente Windows Imaging includono *JPEG*, *png* e *TIFF* e i formati di metadati supportati includono *XMP* e *EXIF*. Con Windows 7, Windows Imaging Component amplia la conformità agli standard fornendo supporto per la decodifica progressiva delle immagini, le funzionalità *png* espanse, i metadati *gif* e i metadati che si estendono sui segmenti *APPn* . Vedere Novità di [WIC in Windows 7](/previous-versions//ee720061(v=vs.85)).

## <a name="direct3d-11"></a>Direct3D 11

Microsoft Direct3D 11 amplia la funzionalità della pipeline Direct3D 10 e fornisce giochi di Windows 7 e applicazioni 3D di fascia alta con accesso efficiente, affidabile e scalabile alla prossima generazione di GPU e CPU multicore. Oltre alle funzionalità disponibili in Direct3D 10, Direct3D 11 introduce alcune nuove funzionalità.

Le superfici Geometry e high order possono ora essere tassellati per supportare contenuto scalabile e dinamico nelle rappresentazioni di superficie di patch e di suddivisione.

Per sfruttare al meglio la potenza di elaborazione parallela disponibile da più core CPU, il multithreading aumenta il numero di potenziali chiamate di rendering per frame distribuendo l'applicazione, il runtime e le chiamate ai driver tra più core. Inoltre, la creazione e la gestione delle risorse sono state ottimizzate per l'uso multithreading, consentendo una gestione della trama dinamica più efficiente per lo streaming.

Per Direct3D 11 sono stati creati nuovi shader di calcolo per utilizzo generico. A differenza degli shader esistenti, si tratta di estensioni della pipeline programmabile che consentono all'applicazione di eseguire completamente più lavoro sulla GPU, indipendentemente dalla CPU. [**DrawAuto**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto), introdotto in Direct3D 10, è stato esteso per interagire con un compute shader.

Sono stati apportati numerosi miglioramenti al linguaggio di[HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)(High-Level Shading Language), ad esempio una forma limitata di collegamento dinamico negli shader, per migliorare la complessità della specializzazione e i costrutti di programmazione orientata a oggetti, come classi e interfacce. (Vedere [le novità di DirectX SDK di marzo 2009](/previous-versions//bb173043(v=vs.85))).

## <a name="direct3d-10-improvements"></a>Miglioramenti di Direct3D 10

Direct3D 10 include una pipeline grafica riprogettata con fasi dello shader programmabili e oggetti di stato non modificabili per inizializzare le fasi della funzione fissa. Gli oggetti stato semplificano la pipeline e migliorano le prestazioni riducendo al minimo il numero di modifiche di stato necessarie. La programmabilità delle fasi dello shader offre ora estensioni di linguaggio ombreggiatura di alto livello per supportare istruzioni shader illimitate, risorse shader generalizzate, calcoli Integer e bit per bit.

La pipeline introduce anche la fase geometry shader, che consente di eseguire il lavoro interamente dalla CPU alla GPU. Questa nuova fase consente di creare la geometria, trasmettere i dati alla memoria ed eseguire il rendering della geometria senza interazione della CPU.

Diversi altri miglioramenti sono progettati in modo specifico per ottenere prestazioni più veloci. Il rendering predicato esegue l'abbattimento dell'occlusione per ridurre la quantità di geometria di cui viene eseguito il rendering. Le API di creazione di istanze possono ridurre in modo significativo la quantità di geometria che deve essere trasferita alla GPU creando più istanze di oggetti simili. Le matrici di trame consentono alla GPU di eseguire lo swapping delle trame senza l'intervento della CPU.

Sono state apportate diverse aggiunte a Direct3D 10 e Direct3D 11 per estendere la gamma di configurazioni che possono essere destinate a queste API. La [piattaforma di rasterizzazione avanzata di Windows](/windows/desktop/direct3darticles/directx-warp) implementa un rapido rendering della CPU scalabile a più core per Direct3D 10, che consente il rendering completo della grafica nei sistemi senza hardware grafico. L'aggiunta di nuovi "livelli di funzionalità", specificamente denominata [Direct3D 10 Level 9](/windows/desktop/direct3d11/d3d11-graphics-reference-10level9), consente a Direct3D 10 e Direct3D 11APIs di guidare l'hardware Microsoft Direct3D 9-Class, espandendo il numero di configurazioni che un'applicazione Direct3D 10 o Direct3D 11 può essere destinata a quasi tutti i computer del mercato. (Vedere la pagina relativa alla [grafica Direct3D 10](../direct3d10/d3d10-graphics.md)).

## <a name="directxgdi-interoperability"></a>Interoperabilità di DirectX/GDI

In Windows Vista, il comportamento di un'applicazione che utilizza sia DirectX sia GDI per eseguire il rendering in una superficie condivisa è diverso a seconda che DWM sia attivo o disattivato. Inoltre, quando DWM è acceso, le applicazioni che utilizzano DirectX e GDI si comportano in modo diverso in Windows Vista rispetto a Windows XP. In questo modo, molti ISV potevano disabilitare DWM durante l'esecuzione delle applicazioni in Windows Vista per garantire un comportamento coerente. Grazie ai miglioramenti apportati a DirectX in Windows 7, un'applicazione può ora combinare liberamente DirectX e GDI senza disabilitare DWM. Windows 7 offre anche un miglioramento delle prestazioni per gli scenari che richiedono l'interoperabilità tra DirectX e GDI usando le API Direct3D 10 più efficienti. Vedere [Cenni preliminari sull'interoperatività Direct2D e GDI](../direct2d/direct2d-and-gdi-interoperation-overview.md).

 

 