---
description: I vertex buffer, rappresentati dall'interfaccia IDirect3DVertexBuffer9, sono buffer di memoria che contengono dati sui vertici.
ms.assetid: vs|directx_sdk|~\vertex_buffers.htm
title: Vertex Buffer (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ceec0f5aee30597b20142945a4ffd3cbcd29500db4113ac2c8dcdd27d045d6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043999"
---
# <a name="vertex-buffers-direct3d-9"></a>Vertex Buffer (Direct3D 9)

I vertex buffer, rappresentati [**dall'interfaccia IDirect3DVertexBuffer9,**](/windows/desktop/api) sono buffer di memoria che contengono dati sui vertici. I vertex buffer possono contenere qualsiasi tipo di vertice, trasformato o non trasformato, acceso o non illuminato, di cui è possibile eseguire il rendering tramite l'uso dei metodi di rendering [**nell'interfaccia IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) È possibile elaborare i vertici in un vertex buffer per eseguire operazioni quali trasformazione, illuminazione o generazione di flag di ritaglio. La trasformazione viene sempre eseguita.

La flessibilità dei vertex buffer li rende punti di staging ideali per il riutilizzo della geometria trasformata. È possibile creare un singolo vertex buffer, trasformare, illuminare e ritagliare i vertici al suo interno ed eseguire il rendering del modello nella scena il numero di volte necessario senza trasformarlo nuovamente, anche con modifiche dello stato di rendering interleaved. Ciò è utile quando si esegue il rendering di modelli che usano più trame: la geometria viene trasformata una sola volta e quindi ne è possibile eseguire il rendering in base alle esigenze, interfoliando con le modifiche di trama necessarie. Le modifiche dello stato di rendering apportate dopo l'elaborazione dei vertici vengono applicate alla successiva elaborazione dei vertici.

-   [Descrizione](#description)
-   [Pool di memoria e utilizzo](#memory-pool-and-usage)

## <a name="description"></a>Descrizione

Un vertex buffer viene descritto in termini di funzionalità: se può esistere solo nella memoria di sistema, se viene usato solo per operazioni di scrittura e il tipo e il numero di vertici che può contenere. Tutti questi tratti sono mantenuti in una [**struttura \_ DESC D3DVERTEXBUFFER.**](d3dvertexbuffer-desc.md)

Il membro Format è impostato su D3DFMT VERTEXDATA per indicare che si \_ tratta di un vertex buffer. Il tipo identifica il tipo di risorsa del vertex buffer. Il membro della struttura Usage contiene flag di funzionalità generali. Il flag D3DUSAGE SOFTWAREPROCESSING indica che il vertex buffer deve essere usato con \_ l'elaborazione dei vertici software. La presenza del flag D3DUSAGE WRITEONLY in Usage indica che la memoria del vertex buffer viene usata \_ solo per le operazioni di scrittura. In questo modo il driver può inserire i dati dei vertici nella posizione di memoria migliore per abilitare l'elaborazione e il rendering veloci. Se il flag D3DUSAGE WRITEONLY non viene usato, è meno probabile che il driver metta i dati in un percorso inefficiente per \_ le operazioni di lettura. Ciò consente di sacrificare una certa velocità di elaborazione e rendering. Se questo flag non viene specificato, si presuppone che le applicazioni eseggono operazioni di lettura e scrittura sui dati all'interno del vertex buffer.

Pool specifica la classe di memoria allocata per il vertex buffer. Il flag SYSTEMMEM D3DPOOL indica che il sistema ha \_ creato il vertex buffer nella memoria di sistema.

Il membro Size archivia le dimensioni, in byte, dei dati del vertex buffer. Il membro FVF contiene una combinazione [di D3DFVF](d3dfvf.md) che identificano il tipo di vertici contenuti nel buffer.

## <a name="memory-pool-and-usage"></a>Pool di memoria e utilizzo

È possibile creare vertex buffer con il metodo [**IDirect3DDevice9::CreateVertexBuffer,**](/windows/desktop/api) che accetta i parametri di pool (classe di memoria) e di utilizzo. È anche possibile creare **IDirect3DDevice9::CreateVertexBuffer** con un codice FVF specificato da usare nell'elaborazione dei vertici di funzione fissa o come output dei vertici del processo. Per informazioni dettagliate, [vedere FVF Vertex Buffers (Direct3D 9)](fvf-vertex-buffers.md).

Il flag D3DUSAGE SOFTWAREPROCESSING può essere impostato quando è abilitata l'elaborazione dei vertici software o in modalità mista \_ (D3DCREATE \_ MIXED \_ VERTEXPROCESSING/D3DCREATE \_ SOFTWARE \_ VERTEXPROCESSING) per tale dispositivo. D3DUSAGE SOFTWAREPROCESSING deve essere impostato per l'uso dei buffer con l'elaborazione dei vertici software in modalità mista, ma non deve essere impostato per le migliori prestazioni possibili quando si usa l'elaborazione dei vertici hardware in modalità \_ mista. D3DCREATE \_ HARDWARE \_ VERTEXPROCESSING). Tuttavia, l'impostazione D3DUSAGE SOFTWAREPROCESSING è l'unica opzione quando un singolo buffer deve essere usato con l'elaborazione dei \_ vertici hardware e software. D3DUSAGE SOFTWAREPROCESSING è consentito sia per i dispositivi \_ misti che per i dispositivi software.

È possibile forzare i buffer di vertici e indici nella memoria di sistema specificando SYSTEMMEM D3DPOOL, anche quando l'elaborazione dei vertici viene eseguita \_ nell'hardware. Questo è un modo per evitare grandi quantità di memoria bloccata dalla pagina quando un driver sta inserendo questi buffer nella memoria AGP.

Questa sezione presenta i concetti necessari per comprendere e usare i vertex buffer in un'applicazione Direct3D. Le informazioni sono suddivise nelle sezioni seguenti.

-   [Creazione di un vertex buffer (Direct3D 9)](creating-a-vertex-buffer.md)
-   [Accesso al contenuto di un vertex buffer (Direct3D 9)](accessing-the-contents-of-a-vertex-buffer.md)
-   [Rendering da un vertex buffer (Direct3D 9)](rendering-from-a-vertex-buffer.md)
-   [Buffer dei vertici FVF (Direct3D 9)](fvf-vertex-buffers.md)
-   [Elaborazione dei vertici delle funzioni fisse (Direct3D 9)](fixed-function-vertex-processing.md)
-   [Elaborazione di vertici programmabili (Direct3D 9)](programmable-vertex-processing.md)
-   [Tipi di dispositivo e requisiti di elaborazione dei vertici (Direct3D 9)](device-types-and-vertex-processing-requirements.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse Direct3D](direct3d-resources.md)
</dt> <dt>

[Rendering da vertex e buffer di indice (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> <dt>

[Buffer di indice (Direct3D 9)](index-buffers.md)
</dt> </dl>

 

 
