---
title: High Fidelity Graphics with DirectX
description: Windows sviluppatori di applicazioni hanno usato da tempo Microsoft DirectX per fornire grafica 3D di alta qualità, con accelerazione hardware.
ms.assetid: db555657-90b9-4db2-a0c2-bfaa526a8dd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9ecb5d6403745162f19b16eea15c22ef7f9676b14bd291226af2f8321483b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086644"
---
# <a name="high-fidelity-graphics-with-directx"></a>High Fidelity Graphics with DirectX

Windows sviluppatori di applicazioni hanno usato da tempo Microsoft DirectX per fornire grafica 3D di alta qualità, con accelerazione hardware. Quando la tecnologia è stata integrata nel 1995, gli sviluppatori potevano fornire grafica 3D di alta qualità per giochi e applicazioni di progettazione per giocatori e professionisti disposti a pagare un extra per una scheda grafica 3D. Ora, anche i PC più economici includono hardware grafico 3D idoneo.

Per sfruttare queste funzionalità grafiche, Windows Vista ha introdotto l'infrastruttura di Windows Display Driver Model (WDDM) per DirectX che consente a più applicazioni e servizi di condividere le risorse dell'unità di elaborazione grafica (GPU). Il Gestione finestre desktop (DWM) usa questa tecnologia per animare il cambio di attività in 3D, fornire immagini di anteprima dinamiche delle finestre dell'applicazione e per fornire Windows effetto cristallo per applicazioni desktop.

Windows 7 mette ancora più funzionalità grafiche nelle mani degli sviluppatori di applicazioni. Grazie a un nuovo set di DirectXAPI, gli sviluppatori Microsoft Win32 possono sfruttare le innovazioni più recenti nelle GPU per aggiungere grafica, testo e immagini veloci, scalabili, di alta qualità, 2D e 3D alle applicazioni. Nei display *LCD* più recenti, le applicazioni DirectXAPI possono visualizzare il contenuto del desktop e della finestra usando una profondità di colore maggiore di 8 bit per componente colore.

Con DirectX, gli sviluppatori Win32 possono anche usare il parallelismo della GPU per calcoli generici, ad esempio l'elaborazione di immagini, ed eseguire il rendering su hardware DirectX 10, hardware DirectX 9, CPU o in un computer Windows remoto. Queste tecnologie sono state progettate per interagire con Windows Graphics Device Interface (GDI) e Windows GDI+, assicurando che gli sviluppatori possano mantenere facilmente gli investimenti esistenti nel codice Win32. Vedere Novità di DirectX SDK di marzo [2009.](/previous-versions//bb173043(v=vs.85))

Queste funzionalità grafiche avanzate sono fornite dalle *API basate* su COM seguenti:

-   [Direct2D per](../direct2d/direct2d-portal.md) disegnare grafica 2D.
-   [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) per la disposizione e il rendering del testo.
-   [Windows imaging per l'elaborazione](/windows/desktop/wic/-wic-lh) e la visualizzazione di immagini.
-   [Direct3D 10 per](/windows/desktop/direct3d10/d3d10-graphics) disegnare grafica 3D.
-   [Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) per disegnare grafica 3D e fornire l'accesso a tecnologie GPU di prossima generazione, ad esempio la struttura a schema, il supporto limitato per lo streaming delle trame e l'elaborazione per utilizzo generico.
-   [DirectX Graphic Infrastructure (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) per la gestione di dispositivi di visualizzazione locali e remoti e risorse GPU e per garantire l'interoperabilità tra DirectX e GDI.

## <a name="direct2d"></a>Direct2D

Basato su Microsoft Direct3D 10, [Direct2D](../direct2d/direct2d-portal.md) offre agli sviluppatori Win32 API in modalità immediata, indipendenti dalla risoluzione e 2D che usano la potenza dell'hardware grafico di nuova generazione, ma interagisce bene con le attuali applicazioni GDI/GDI+ e le applicazioni Direct3D 10. Direct2D offre un rendering 2D di alta qualità con prestazioni superiori a GDI e GDI+. Offre agli sviluppatori Win32 un controllo più fine sulle risorse e sulla loro gestione. Vedere [Direct2D.](../direct2d/direct2d-portal.md)

## <a name="directwrite"></a>DirectWrite

Molte delle applicazioni attuali devono supportare il rendering del testo di alta qualità, i tipi di carattere del contorno indipendenti dalla risoluzione e il supporto completo per layout e testo Unicode. [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), un nuovo componente DirectX, offre queste funzionalità e altro ancora:

-   Sistema di layout di testo indipendente dal dispositivo che migliora la leggibilità del testo nei documenti e nell'interfaccia utente.
-   Rendering di testo *ClearType* di alta qualità, sottopiede, che può usare GDI, [Direct2D](../direct2d/direct2d-portal.md)o una tecnologia di rendering specifica dell'applicazione.
-   Testo con accelerazione hardware, se usato con [Direct2D.](../direct2d/direct2d-portal.md)
-   Supporto per testo in più formati.
-   Supporto per le funzionalità tipografiche avanzate dei tipi *di carattere OpenType.*
-   Supporto per il layout e il rendering del testo in tutte le lingue supportate.
-   Layout e rendering compatibili con GDI.

Il sistema dei tipi di carattere [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) consente l'utilizzo di qualsiasi tipo di carattere ovunque, in cui gli utenti non devono eseguire un passaggio di installazione separato solo per usare un tipo di carattere e una migliore gerarchia strutturale del raggruppamento dei tipi di carattere per facilitare l'individuazione manuale o programmatica dei tipi di carattere. Le API supportano la misurazione, il disegno e l'hit testing del testo in più formati. DirectWrite il testo in tutte le lingue supportate per le applicazioni globali e localizzate, sulla base dell'infrastruttura linguistica chiave disponibile in Windows 7. DirectWrite offre anche API per il rendering dei glifi di basso livello per gli sviluppatori che vogliono eseguire il proprio layout e l'elaborazione da Unicode a glifo. Vedere [DirectWrite](../directwrite/direct-write-portal.md).

## <a name="windows-imaging-component"></a>Componente Windows Imaging

In Windows Vista, il componente [Windows Imaging ha](/windows/desktop/wic/-wic-lh) introdotto un framework estendibile per l'uso di immagini e metadati delle immagini. I formati di immagine supportati da Windows Imaging Component includono *JPEG,* *PNG* e *TIFF* e i formati di metadati supportati *includono XMP* *ed EXIF.* Con Windows 7, Windows Imaging Component amplia la conformità agli standard fornendo il supporto per la decodifica progressiva delle immagini, le funzionalità *PNG* espanse, i metadati *GIF* e i metadati che si estendono sui segmenti *APPn.* Vedere [Novità di WIC in Windows 7.](/previous-versions//ee720061(v=vs.85))

## <a name="direct3d-11"></a>Direct3D 11

Microsoft Direct3D 11 estende le funzionalità della pipeline Direct3D 10 e offre giochi Windows 7 e applicazioni 3D di fascia alta con accesso efficiente, affidabile e scalabile alla prossima generazione di GPU e CPU multi-core. Oltre alle funzionalità disponibili in Direct3D 10, Direct3D 11 introduce diverse nuove funzionalità.

Le superfici geometriche e di ordine elevato possono ora essere suddivise a più livelli per supportare contenuto dinamico e scalabile nelle rappresentazioni della superficie di patch e suddivisione.

Per usare in modo corretto la potenza di elaborazione parallela disponibile da più core CPU, il multithreading aumenta il numero di potenziali chiamate di rendering per fotogramma distribuendo le chiamate all'applicazione, al runtime e al driver tra più core. Inoltre, la creazione e la gestione delle risorse sono state ottimizzate per l'uso multithreading, consentendo una gestione dinamica più efficiente delle trame per lo streaming.

Sono stati creati nuovi compute shader per utilizzo generico per Direct3D 11. A differenza degli shader esistenti, si tratta di estensioni della pipeline programmabile che consentono all'applicazione di eseguire più operazioni completamente sulla GPU, indipendentemente dalla CPU. [**DrawAuto,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto)introdotto in Direct3D 10, è stato esteso per interagire con un compute shader.

Sono stati apportati diversi miglioramenti al linguaggio di ombreggiatura di alto livello[(HLSL),](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)ad esempio una forma limitata di collegamento dinamico negli shader per migliorare la complessità della specializzazione e costrutti di programmazione orientati a oggetti come classi e interfacce. Vedere Novità di DirectX SDK di marzo [2009.](/previous-versions//bb173043(v=vs.85))

## <a name="direct3d-10-improvements"></a>Miglioramenti di Direct3D 10

Direct3D 10 include una pipeline grafica riprogettata con fasi di shader programmabili e oggetti di stato non modificabili per l'inizializzazione delle fasi a funzione fissa. Gli oggetti di stato semplificano la pipeline e migliorano le prestazioni riducendo al minimo il numero di modifiche di stato necessarie. La programmabilità delle fasi dello shader offre ora estensioni del linguaggio di ombreggiatura di alto livello per supportare istruzioni shader illimitate, risorse shader generalizzate e calcoli interi e bit per bit.

La pipeline introduce anche la fase geometry shader, che consente di eseguire l'offload del lavoro interamente dalla CPU alla GPU. Questa nuova fase consente di creare geometria, trasmettere i dati in memoria ed eseguire il rendering della geometria senza alcuna interazione con la CPU.

Diversi altri miglioramenti sono progettati specificamente per migliorare le prestazioni. Il rendering predicato esegue il culling dell'occlusione per ridurre la quantità di geometria di cui viene eseguito il rendering. Le API di istanze possono ridurre notevolmente la quantità di geometria che deve essere trasferita alla GPU disegnando più istanze di oggetti simili. Gli array di trame consentono alla GPU di eseguire lo scambio di trame senza l'intervento della CPU.

Sono state apportate diverse aggiunte a Direct3D 10 e Direct3D 11 per estendere la gamma di configurazioni che possono essere destinate a queste API. La [Windows WARP (Advanced Rasterization Platform)](/windows/desktop/direct3darticles/directx-warp) implementa il rendering rapido e scalabile della CPU multi-core per Direct3D 10, consentendo il rendering della grafica completo nei sistemi senza hardware grafico. L'aggiunta di nuovi "livelli di funzionalità", denominati in modo specifico [Direct3D 10 Livello 9,](/windows/desktop/direct3d11/d3d11-graphics-reference-10level9)consentono alle api Direct3D 10 e Direct3D 11APIs di guidare l'hardware di classe 9 di Microsoft Direct3D, espandendo il numero di configurazioni che un'applicazione Direct3D 10 o Direct3D 11 può avere come destinazione quasi tutti i sistemi di computer sul mercato. Vedere [Direct3D 10 Graphics (Grafica Direct3D 10).](../direct3d10/d3d10-graphics.md)

## <a name="directxgdi-interoperability"></a>Interoperabilità DirectX/GDI

In Windows Vista il comportamento di un'applicazione che usa DirectX e GDI per eseguire il rendering su una superficie condivisa è diverso a seconda che DWM sia o meno spento. Inoltre, quando DWM è installato, le applicazioni che usano DirectX e GDI si comportano in modo diverso in Windows Vista rispetto a Windows XP. Questo ha causato la disabilitazione di DWM da parte di molti ISV durante l'esecuzione delle applicazioni Windows Vista per garantire un comportamento coerente. Con i miglioramenti apportati a DirectX in Windows 7, un'applicazione può ora combinare liberamente DirectX e GDI senza disabilitare DWM. Windows 7 offre anche prestazioni migliorate per gli scenari che richiedono l'interoperabilità tra DirectX e GDI usando le API Direct3D 10 più efficienti. Vedere [Cenni preliminari sull'interoperatività di Direct2D e GDI.](../direct2d/direct2d-and-gdi-interoperation-overview.md)

 

 