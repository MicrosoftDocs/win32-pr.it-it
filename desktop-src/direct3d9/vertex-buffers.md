---
description: I buffer dei vertici, rappresentati dall'interfaccia IDirect3DVertexBuffer9, sono buffer di memoria contenenti dati del vertice.
ms.assetid: vs|directx_sdk|~\vertex_buffers.htm
title: Buffer vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e38feb34e7b9f637f383bf451bff812d9ee6fb1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746111"
---
# <a name="vertex-buffers-direct3d-9"></a>Buffer vertex (Direct3D 9)

I buffer dei vertici, rappresentati dall'interfaccia [**IDirect3DVertexBuffer9**](/windows/desktop/api) , sono buffer di memoria contenenti dati del vertice. I buffer dei vertici possono contenere qualsiasi tipo di vertice, trasformato o non trasformato, acceso o non illuminato, di cui è possibile eseguire il rendering tramite l'uso dei metodi di rendering nell'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) . È possibile elaborare i vertici in un buffer vertex per eseguire operazioni quali trasformazione, illuminazione o generazione di flag di ritaglio. La trasformazione viene sempre eseguita.

La flessibilità dei buffer vertex li rende i punti di staging ideali per il riutilizzo della geometria trasformata. È possibile creare un singolo buffer dei vertici, trasformarlo e ritagliarvi i vertici ed eseguire il rendering del modello nella scena il numero di volte necessario senza trasformarlo, anche con le modifiche dello stato di rendering Interleave. Questa operazione è utile quando si esegue il rendering di modelli che usano più trame: la geometria viene trasformata una sola volta e quindi ne viene eseguito il rendering in base alle esigenze, con interfoliazione con le modifiche di trama richieste. Le modifiche dello stato di rendering apportate dopo l'elaborazione dei vertici diventano effettive alla successiva elaborazione dei vertici.

-   [Descrizione](#description)
-   [Pool di memoria e utilizzo](#memory-pool-and-usage)

## <a name="description"></a>Descrizione

Un vertex buffer viene descritto in termini di funzionalità: se può esistere solo nella memoria di sistema, se viene usato solo per le operazioni di scrittura e il tipo e il numero di vertici che può contenere. Tutti questi tratti sono contenuti in una struttura [**D3DVERTEXBUFFER \_ desc**](d3dvertexbuffer-desc.md) .

Il formato membro è impostato su D3DFMT \_ VERTEXDATA per indicare che si tratta di un buffer di vertice. Il tipo identifica il tipo di risorsa del buffer dei vertici. Il membro della struttura Usage contiene flag di funzionalità generali. Il \_ flag SOFTWAREPROCESSING di D3DUSAGE indica che il buffer vertex deve essere usato con l'elaborazione dei vertici software. La presenza del \_ flag WRITEONLY di D3DUSAGE nell'utilizzo indica che la memoria del buffer dei vertici viene utilizzata solo per le operazioni di scrittura. Questo consente di liberare il driver per inserire i dati dei vertici nella migliore posizione di memoria per consentire l'elaborazione e il rendering rapidi. Se il \_ flag WRITEONLY di D3DUSAGE non viene utilizzato, è meno probabile che i dati vengano inseriti in un percorso non efficiente per le operazioni di lettura. Questo comporta una certa velocità di elaborazione e di rendering. Se questo flag non viene specificato, si presuppone che le applicazioni eseguano operazioni di lettura e scrittura sui dati all'interno del buffer dei vertici.

Pool specifica la classe di memoria allocata per il buffer dei vertici. Il \_ flag SYSTEMMEM di D3DPOOL indica che il sistema ha creato il buffer dei vertici nella memoria di sistema.

Il membro size archivia le dimensioni, in byte, dei dati del buffer dei vertici. Il membro FVF contiene una combinazione di [D3DFVF](d3dfvf.md) che identificano il tipo di vertici contenuti nel buffer.

## <a name="memory-pool-and-usage"></a>Pool di memoria e utilizzo

È possibile creare buffer vertex con il metodo [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/desktop/api) , che accetta i parametri di utilizzo e del pool (classe di memoria). **IDirect3DDevice9:: CreateVertexBuffer** può essere creato anche con un codice FVF specificato da usare nell'elaborazione del vertice di una funzione fissa o come output dei vertici del processo. Per informazioni dettagliate, vedere [FVF vertex buffers (Direct3D 9)](fvf-vertex-buffers.md).

Il \_ flag D3DUSAGE SOFTWAREPROCESSING può essere impostato quando è abilitata l'elaborazione di vertici in modalità mista o software (D3DCREATE \_ mixed \_ VERTEXPROCESSING/D3DCREATE \_ software \_ VERTEXPROCESSING) per tale dispositivo. \_È necessario impostare D3DUSAGE SOFTWAREPROCESSING per i buffer da usare con l'elaborazione dei vertici software in modalità mista, ma non per ottenere le migliori prestazioni possibili quando si usa l'elaborazione dei vertici hardware in modalità mista. \_VERTEXPROCESSING hardware D3DCREATE \_ ). Tuttavia, l'impostazione \_ di D3DUSAGE SOFTWAREPROCESSING è l'unica opzione quando è necessario usare un singolo buffer con l'elaborazione dei vertici hardware e software. D3DUSAGE \_ SOFTWAREPROCESSING è consentito per le applicazioni miste e per i dispositivi software.

È possibile forzare i buffer dei vertici e degli indici nella memoria di sistema specificando D3DPOOL \_ SYSTEMMEM, anche quando l'elaborazione del vertice viene eseguita in hardware. Questo è un modo per evitare quantità eccessivamente elevate di memoria con blocco di pagina quando un driver inserisce questi buffer nella memoria AGP.

In questa sezione vengono introdotti i concetti necessari per comprendere e utilizzare i buffer dei vertici in un'applicazione Direct3D. Le informazioni sono suddivise nelle sezioni riportate di seguito.

-   [Creazione di un buffer vertex (Direct3D 9)](creating-a-vertex-buffer.md)
-   [Accesso al contenuto di un buffer vertex (Direct3D 9)](accessing-the-contents-of-a-vertex-buffer.md)
-   [Rendering da un buffer vertex (Direct3D 9)](rendering-from-a-vertex-buffer.md)
-   [Buffer vertex FVF (Direct3D 9)](fvf-vertex-buffers.md)
-   [Elaborazione del vertice della funzione fissa (Direct3D 9)](fixed-function-vertex-processing.md)
-   [Elaborazione Vertex programmabile (Direct3D 9)](programmable-vertex-processing.md)
-   [Tipi di dispositivi e requisiti di elaborazione dei vertici (Direct3D 9)](device-types-and-vertex-processing-requirements.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse Direct3D](direct3d-resources.md)
</dt> <dt>

[Rendering dai buffer di Vertex e index (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> <dt>

[Buffer di indice (Direct3D 9)](index-buffers.md)
</dt> </dl>

 

 
