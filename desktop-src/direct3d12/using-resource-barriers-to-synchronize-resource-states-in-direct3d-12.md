---
title: Uso delle barriere delle risorse per sincronizzare gli stati delle risorse in Direct3D 12
description: Per ridurre l'utilizzo complessivo della CPU e abilitare il multithreading dei driver e la pre-elaborazione, Direct3D 12 sposta la responsabilità della gestione dello stato per risorsa dal driver di grafica all'applicazione.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df27e7997b4f3f56ae8e87688e5cc136dc7eb87d
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343476"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a>Uso delle barriere delle risorse per sincronizzare gli stati delle risorse in Direct3D 12

Per ridurre l'utilizzo complessivo della CPU e abilitare il multithreading dei driver e la pre-elaborazione, Direct3D 12 sposta la responsabilità della gestione dello stato per risorsa dal driver di grafica all'applicazione. Un esempio di stato per risorsa è se è attualmente in corso l'accesso a una risorsa trama come tramite un Shader Resource View o come visualizzazione di destinazione di rendering. In Direct3D 11 i driver dovevano tenere traccia di questo stato in background. Questa operazione è costosa dal punto di vista della CPU e complica significativamente qualsiasi tipo di progettazione multi-thread. In Microsoft Direct3D 12 la maggior parte dello stato per risorsa viene gestita dall'applicazione con una singola API, [**ID3D12GraphicsCommandList::ResourceBarrier.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

-   [Uso dell'API ResourceBarrier per gestire lo stato per ogni risorsa](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [Stati delle risorse](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [Stati iniziali per le risorse](#initial-states-for-resources)
    -   [Restrizioni dello stato delle risorse di lettura/scrittura](#readwrite-resource-state-restrictions)
    -   [Stati delle risorse per la presentazione dei buffer nascosto](#resource-states-for-presenting-back-buffers)
    -   [Rimozione delle risorse](#discarding-resources)
-   [Transizioni di stato implicite](#implicit-state-transitions)
    -   [Promozione dello stato comune](#common-state-promotion)
    -   [Decadimento dello stato a comune](#state-decay-to-common)
    -   [Implicazioni per le prestazioni](#performance-implications)
-   [Split Barriers](#split-barriers)
-   [Scenario di esempio di barriera delle risorse](#resource-barrier-example-scenario)
-   [Esempio comune di promozione e decadimento dello stato](#common-state-promotion-and-decay-sample)
-   [Esempio di barriere di divisione](#example-of-split-barriers)
-   [Argomenti correlati](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a>Uso dell'API ResourceBarrier per gestire lo stato per ogni risorsa

[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifica al driver di grafica le situazioni in cui il driver potrebbe dover sincronizzare più accessi alla memoria in cui è archiviata una risorsa. Il metodo viene chiamato con una o più strutture di descrizione della barriera delle risorse che indicano il tipo di barriera di risorse dichiarato.

Esistono tre tipi di barriere alle risorse:

-   **Barriera di transizione:** una barriera di transizione indica che un set di sottorisorse esegue la transizione tra utilizzi diversi. Una [**struttura D3D12 \_ RESOURCE TRANSITION \_ \_ BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) viene usata per specificare la sottorisorsa in fase di transizione, nonché gli stati *prima* e dopo della sottorisorsa. 

    Il sistema verifica che le transizioni di sottorisorse in un elenco di comandi siano coerenti con le transizioni precedenti nello stesso elenco di comandi. Il livello di debug tiene inoltre traccia dello stato della sottorisorsa per trovare altri errori, ma questa convalida è conservativa e non esaustiva.

    Si noti che è possibile usare il flag D3D12 RESOURCE BARRIER ALL SUBRESOURCES per specificare che è in corso la transizione di tutte le \_ \_ \_ \_ sottorisorse all'interno di una risorsa.

-   **Barriera di aliasing:** una barriera di aliasing indica una transizione tra gli utilizzi di due risorse diverse che hanno mapping sovrapposti nello stesso heap. Questo vale sia per le risorse riservate che per le risorse inserite. Una [**struttura D3D12 \_ RESOURCE \_ ALIASING \_ BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) viene usata per specificare sia la risorsa *prima* che la *risorsa dopo.*

    Si noti che una o entrambe le risorse possono essere NULL, a indicare che qualsiasi risorsa affiancata potrebbe causare l'aliasing. Per altre informazioni sull'uso delle risorse affiancate, vedere [Risorse affiancate](../direct3d11/tiled-resources.md) e [Risorse in riquadri del volume](volume-tiled-resources.md).

-   Barriera della visualizzazione di accesso non ordinato : una barriera di **UAV** indica che tutti gli accessi UAV, sia in lettura che in scrittura, a una determinata risorsa devono essere completati tra gli accessi UAV futuri, sia in lettura che in scrittura. Non è necessario che un'app metta una barriera UAV tra due chiamate di disegno o invio che leggono solo da un UAV. Inoltre, non è necessario inserire una barriera UAV tra due chiamate di disegno o invio che scrivono nello stesso UAV se l'applicazione sa che è sicuro eseguire l'accesso UAV in qualsiasi ordine. Una [**struttura D3D12 \_ RESOURCE \_ UAV \_ BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) viene usata per specificare la risorsa UAV a cui si applica la barriera. L'applicazione può specificare NULL per l'UAV della barriera, che indica che qualsiasi accesso UAV potrebbe richiedere la barriera.

Quando [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) viene chiamato con una matrice di descrizioni della barriera di risorse, l'API si comporta come se fosse stata chiamata una volta per ogni elemento, nell'ordine in cui sono stati forniti.

In qualsiasi momento, una sottorisorsa si trova esattamente in uno stato, determinato dal set di flag [**D3D12 \_ RESOURCE \_ STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) forniti a [**ResourceBarrier.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) L'applicazione deve garantire che gli *stati prima* e *dopo* le chiamate consecutive a **ResourceBarrier siano d'accordo.**

> [!TIP]
>
> Le applicazioni devono eseguire più transizioni in batch in un'unica chiamata API, laddove possibile.

 

### <a name="resource-states"></a>Stati delle risorse

Per l'elenco completo degli stati delle risorse tra cui una risorsa può eseguire la transizione, vedere l'argomento di riferimento per [**l'enumerazione D3D12 \_ RESOURCE \_ STATES.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)

Per le barriere di suddivisione delle risorse, vedere [**anche D3D12 \_ RESOURCE BARRIER \_ \_ FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).

### <a name="initial-states-for-resources"></a>Stati iniziali per le risorse

Le risorse possono essere create con qualsiasi stato iniziale specificato dall'utente (valido per la descrizione della risorsa), con le eccezioni seguenti:

-   Gli heap di caricamento devono iniziare con lo stato D3D12 RESOURCE STATE GENERIC READ, che è una combinazione \_ OR bit per bit \_ \_ \_ di:
    -   VERTICE DELLO STATO DELLA RISORSA D3D12 \_ \_ E BUFFER \_ \_ \_ \_ COSTANTE
    -   BUFFER DELL'INDICE DELLO \_ \_ STATO DELLA \_ RISORSA \_ D3D12
    -   ORIGINE COPIA STATO RISORSA D3D12 \_ \_ \_ \_
    -   RISORSA D3D12 \_ RESOURCE STATE NON PIXEL \_ \_ \_ \_ \_ SHADER
    -   RISORSA \_ \_ PIXEL \_ \_ SHADER \_ DELLO STATO DELLA RISORSA D3D12
    -   ARGOMENTO INDIRETTO DELLO STATO DELLA RISORSA D3D12 \_ \_ \_ \_
-   Gli heap di readback devono essere avviati nello stato D3D12 \_ RESOURCE \_ STATE COPY \_ \_ DEST.
-   I buffer back della catena di scambio vengono avviati automaticamente nello stato D3D12 \_ RESOURCE \_ STATE \_ COMMON.

Prima che un heap possa essere la destinazione di un'operazione di copia GPU, in genere l'heap deve essere passato allo stato D3D12 \_ RESOURCE \_ STATE COPY \_ \_ DEST. Tuttavia, le risorse create negli heap UPLOAD devono iniziare in e non possono passare dallo stato GENERIC READ perché solo la CPU sta \_ eseguendo la scrittura. Al contrario, le risorse di cui è stato eseguito il commit create negli heap READBACK devono iniziare in e non possono cambiare dallo stato COPY \_ DEST.

### <a name="readwrite-resource-state-restrictions"></a>Restrizioni relative allo stato delle risorse di lettura/scrittura

I bit di utilizzo dello stato della risorsa usati per descrivere uno stato della risorsa sono suddivisi in stati di sola lettura e di lettura/scrittura. L'argomento di riferimento [**per D3D12 \_ RESOURCE \_ STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indica il livello di accesso in lettura/scrittura per ogni bit nell'enumerazione.

Al massimo, è possibile impostare un solo bit di lettura/scrittura per qualsiasi risorsa. Se è impostato un bit di scrittura, non è possibile impostare alcun bit di sola lettura per tale risorsa. Se non è impostato alcun bit di scrittura, è possibile impostare un numero qualsiasi di bit di lettura.

### <a name="resource-states-for-presenting-back-buffers"></a>Stati delle risorse per la presentazione di buffer back

Prima di presentare un buffer nascosto, deve essere nello stato D3D12 \_ RESOURCE \_ STATE \_ COMMON. Si noti che lo stato della risorsa D3D12 RESOURCE STATE PRESENT è un sinonimo di \_ \_ \_ D3D12 RESOURCE STATE COMMON ed entrambi hanno un valore \_ \_ pari a \_ 0. Se [**IDXGISwapChain::P resent**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (o [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) viene chiamato su una risorsa che non è attualmente in questo stato, viene generato un avviso del livello di debug.

### <a name="discarding-resources"></a>Rimozione delle risorse

Tutte le sottorisorse in una risorsa devono essere nello stato RENDER TARGET o DEPTH WRITE, rispettivamente per le destinazioni di rendering/le risorse depth-stencil, quando viene chiamato \_ \_ [**ID3D12GraphicsCommandList::D iscardResource.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)

## <a name="implicit-state-transitions"></a>Transizioni di stato implicite

Le risorse possono essere "promosse" solo al di fuori di D3D12 \_ RESOURCE \_ STATE \_ COMMON. Analogamente, le risorse "decadono" solo a D3D12 \_ RESOURCE \_ STATE \_ COMMON.

### <a name="common-state-promotion"></a>Promozione dello stato comune

Tutte le risorse del buffer e le trame con il flag DI RISORSA D3D12 ALLOW SIMULTANEOUS ACCESS impostato vengono \_ \_ promosse implicitamente da \_ \_ \_ D3D12 RESOURCE STATE \_ COMMON \_ \_ \_ allo stato pertinente al primo accesso alla GPU, inclusa la lettura generica per coprire qualsiasi scenario di lettura. È possibile accedere a qualsiasi risorsa nello stato COMMON come se si trovava in un unico stato con

<dl> 1 flag WRITE o  
1 o più flag READ  
</dl>

Le risorse possono essere promosse dallo stato COMMON in base alla tabella seguente:



| Flag di stato                    | Buffer e Simultaneous-Access trame                             | Trame ad accesso non simultaneo                                     |
|-------------------------------|----------------------------------------------|--------------------------------------|
| VERTEX \_ E \_ CONSTANT \_ BUFFER | Sì                                          | No                                   |
| INDEX \_ BUFFER                 | Sì                                          | No                                   |
| DESTINAZIONE DI \_ RENDERING                | Sì                                          | No                                   |
| ACCESSO NON \_ ORDINATO             | Sì                                          | No                                   |
| SCRITTURA \_ PROFONDITÀ                  | No<sup>\*</sup>                              | No                                   |
| LETTURA \_ DI PROFONDITÀ                   | No<sup>\*</sup>                              | No                                   |
| RISORSA NON \_ PIXEL \_ \_ SHADER  | Sì                                          | Sì                                  |
| RISORSA PIXEL \_ \_ SHADER       | Sì                                          | Sì                                  |
| STREAM \_ OUT                   | Sì                                          | No                                   |
| ARGOMENTO \_ INDIRETTO            | Sì                                          | No                                   |
| COPIA \_ DEST                    | Sì                                          | Sì                                  |
| COPIA \_ ORIGINE                  | Sì                                          | Sì                                  |
| RISOLVERE \_ IL DEST                 | Sì                                          | No                                   |
| RISOLVERE \_ L'ORIGINE               | Sì                                          | No                                   |
| PREDICAZIONE                   | Sì                                          | No                                   |



 

<sup>\*</sup>Le risorse depth-stencil devono essere trame di accesso non simultanee e pertanto non possono mai essere promosse in modo implicito.

Quando si verifica questo accesso, la promozione agisce come una barriera di risorse implicita. Per gli accessi successivi, sarà necessario modificare lo stato della risorsa, se necessario. Si noti che la promozione da uno stato di lettura promosso a più stati di lettura è valida, ma questo non è il caso degli stati di scrittura.  
Ad esempio, se una risorsa nello stato comune viene promossa a RISORSA PIXEL SHADER in una chiamata draw, può comunque essere promossa a NON_PIXEL \_ \_ RISORSA SHADER \_ \_ | RISORSA PIXEL \_ SHADER \_ in un'altra chiamata draw. Tuttavia, se viene usato in un'operazione di scrittura, ad esempio una destinazione di copia, una barriera di transizione dello stato della risorsa dagli stati di lettura alzati di livello combinati, NON_PIXEL \_ SHADER \_ RESOURCE | RISORSA PIXEL \_ \_ SHADER, per \_ copiare DEST è necessario.  
Analogamente, se promosso da COMMON a COPY DEST, è comunque necessario un ostacolo per la transizione da \_ COPY \_ DEST a RENDER \_ TARGET.

Si noti che la promozione dello stato comune è "gratuita" perché la GPU non deve eseguire attese di sincronizzazione. La promozione rappresenta il fatto che le risorse nello stato COMMON non devono richiedere operazioni aggiuntive sulla GPU o sul rilevamento dei driver per supportare determinati accessi.

### <a name="state-decay-to-common"></a>Decadimento dello stato a comune

Il lato opposto della promozione dello stato comune è il decadimento a D3D12 \_ RESOURCE \_ STATE \_ COMMON. Le risorse che soddisfano determinati requisiti sono considerate senza stato e tornano effettivamente allo stato comune quando la GPU termina l'esecuzione di [**un'operazione ExecuteCommandLists.**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) Il decadimento non si verifica tra gli elenchi di comandi eseguiti insieme nella stessa **chiamata a ExecuteCommandLists.**

Quando un'operazione [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) viene completata nella GPU, le risorse seguenti verranno decadimento:

-   Risorse a cui si accede in una coda di copia *o*
-   Buffer delle risorse in qualsiasi tipo di coda *o*
-   Risorse di trama in qualsiasi tipo di coda per cui è impostato il flag DI RISORSA D3D12 \_ \_ ALLOW SIMULTANEOUS ACCESS \_ \_ \_ *oppure*
-   Qualsiasi risorsa promossa in modo implicito a uno stato di sola lettura.

Come la promozione dello stato comune, il decadimento è gratuito perché non è necessaria alcuna sincronizzazione aggiuntiva. La combinazione di promozione e decadimento comuni dello stato consente di eliminare molte [**transizioni resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) non necessarie. In alcuni casi, ciò può offrire miglioramenti significativi delle prestazioni.

I buffer e Simultaneous-Access risorse verranno decadimento allo stato comune indipendentemente dal fatto che siano state esplicitamente transizionate usando barriere di risorse o promosse in modo implicito.

### <a name="performance-implications"></a>Implicazioni per le prestazioni

Quando si registrano transizioni esplicite di [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) sulle risorse nello stato comune, è corretto usare D3D12 RESOURCE STATE COMMON o qualsiasi stato promobile come valore BeforeState nella struttura \_ \_ \_ D3D12 RESOURCE TRANSITION  \_ \_ \_ BARRIER. Ciò consente la gestione dello stato tradizionale che ignora il decadimento automatico dei buffer e delle trame ad accesso simultaneo. Questo potrebbe non essere consigliabile, tuttavia, poiché evitare chiamate **ResourceBarrier** di transizione con risorse note allo stato comune può migliorare significativamente le prestazioni. Le barriere delle risorse possono essere costose. Sono progettate per forzare lo scaricamento della cache, le modifiche al layout della memoria e altre operazioni di sincronizzazione che potrebbero non essere necessarie per le risorse già in stato comune. Un elenco di comandi che usa una barriera di risorse da uno stato non comune a un altro stato non comune in una risorsa attualmente nello stato comune può introdurre un sovraccarico non necessario.

Evitare inoltre transizioni esplicite di [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) a D3D12 RESOURCE STATE COMMON a meno che non sia assolutamente necessario \_ (ad esempio, l'accesso successivo si trova in una coda di comandi COPY che richiede che le risorse inizino \_ \_ nello stato comune). Le transizioni eccessive allo stato comune possono rallentare notevolmente le prestazioni della GPU.

In breve, provare a fare affidamento sulla promozione dello stato comune e decadimento ogni volta che la semantica consente di uscire senza emettere chiamate [**a ResourceBarrier.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

## <a name="split-barriers"></a>Dividere le barriere

Una barriera di transizione della risorsa con il flag D3D12 RESOURCE BARRIER FLAG BEGIN ONLY avvia una barriera di divisione e la barriera di transizione viene \_ \_ detto in \_ \_ \_ sospeso. Mentre la barriera è in sospeso, la risorsa (secondaria) non può essere letta o scritta dalla GPU. L'unica barriera di transizione legale che può essere applicata a una risorsa  (secondaria) con una barriera in sospeso è una con gli stessi stati *prima* e dopo e il flag D3D12 RESOURCE BARRIER FLAG END ONLY, che consente di completare la transizione in \_ \_ \_ \_ \_ sospeso.

Le barriere di divisione forniscono suggerimenti alla GPU che una risorsa nello stato *A* verrà usata successivamente nello stato *B.* In questo modo la GPU può ottimizzare il carico di lavoro di transizione, riducendo o eliminando i blocchi di esecuzione. L'emissione della barriera end-only garantisce che tutte le operazioni di transizione gpu vengono completate prima di passare al comando successivo.

L'uso di barriere di divisione può contribuire a migliorare le prestazioni, in particolare in scenari con più motori o in cui le risorse sono in fase di transizione in lettura/scrittura in uno o più elenchi di comandi.

## <a name="resource-barrier-example-scenario"></a>Scenario di esempio di barriera delle risorse

I frammenti di codice seguenti illustrano l'uso [**del metodo ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) in un esempio di multithreading.

Creazione della depth stencil, transizione a uno stato scrivibile.


```C++
// Create the depth stencil.
{
    CD3DX12_RESOURCE_DESC shadowTextureDesc(
        D3D12_RESOURCE_DIMENSION_TEXTURE2D,
        0,
        static_cast<UINT>(m_viewport.Width), 
        static_cast<UINT>(m_viewport.Height), 
        1,
        1,
        DXGI_FORMAT_D32_FLOAT,
        1, 
        0,
        D3D12_TEXTURE_LAYOUT_UNKNOWN,
        D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL | D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE);

    D3D12_CLEAR_VALUE clearValue;    // Performance tip: Tell the runtime at resource creation the desired clear value.
    clearValue.Format = DXGI_FORMAT_D32_FLOAT;
    clearValue.DepthStencil.Depth = 1.0f;
    clearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &shadowTextureDesc,
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &clearValue,
        IID_PPV_ARGS(&m_depthStencil)));

    // Create the depth stencil view.
    m_device->CreateDepthStencilView(m_depthStencil.Get(), nullptr, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



Creazione della visualizzazione del buffer dei vertici, prima di tutto da uno stato comune a uno di destinazione e quindi da una destinazione a uno stato leggibile generico.


```C++
// Create the vertex buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_vertexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the vertex buffer.
        D3D12_SUBRESOURCE_DATA vertexData = {};
        vertexData.pData = pAssetData + SampleAssets::VertexDataOffset;
        vertexData.RowPitch = SampleAssets::VertexDataSize;
        vertexData.SlicePitch = vertexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy vertex buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_vertexBuffer.Get(), m_vertexBufferUpload.Get(), 0, 0, 1, &vertexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_vertexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER));

        PIXEndEvent(commandList.Get());
    }
```



Creazione della index buffer, prima di tutto da uno stato comune a uno di destinazione e quindi da una destinazione a uno stato leggibile generico.


```C++
// Create the index buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_indexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_indexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the index buffer.
        D3D12_SUBRESOURCE_DATA indexData = {};
        indexData.pData = pAssetData + SampleAssets::IndexDataOffset;
        indexData.RowPitch = SampleAssets::IndexDataSize;
        indexData.SlicePitch = indexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy index buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_indexBuffer.Get(), m_indexBufferUpload.Get(), 0, 0, 1, &indexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_indexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_INDEX_BUFFER));

        PIXEndEvent(commandList.Get());
    }

    // Initialize the index buffer view.
    m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
    m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
    m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
}
```



Creazione di trame e visualizzazioni delle risorse shader. La trama viene modificata da uno stato comune a una destinazione e quindi da una destinazione a una pixel shader risorsa.


```C++
    // Create each texture and SRV descriptor.
    const UINT srvCount = _countof(SampleAssets::Textures);
    PIXBeginEvent(commandList.Get(), 0, L"Copy diffuse and normal texture data to default resources...");
    for (int i = 0; i < srvCount; i++)
    {
        // Describe and create a Texture2D.
        const SampleAssets::TextureResource &tex = SampleAssets::Textures[i];
        CD3DX12_RESOURCE_DESC texDesc(
            D3D12_RESOURCE_DIMENSION_TEXTURE2D,
            0,
            tex.Width, 
            tex.Height, 
            1,
            static_cast<UINT16>(tex.MipLevels),
            tex.Format,
            1, 
            0,
            D3D12_TEXTURE_LAYOUT_UNKNOWN,
            D3D12_RESOURCE_FLAG_NONE);

        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
            D3D12_HEAP_FLAG_NONE,
            &texDesc,
            D3D12_RESOURCE_STATE_COPY_DEST,
            nullptr,
            IID_PPV_ARGS(&m_textures[i])));

        {
            const UINT subresourceCount = texDesc.DepthOrArraySize * texDesc.MipLevels;
            UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_textures[i].Get(), 0, subresourceCount);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
                D3D12_HEAP_FLAG_NONE,
                &CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize),
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&m_textureUploads[i])));

            // Copy data to the intermediate upload heap and then schedule a copy 
            // from the upload heap to the Texture2D.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pAssetData + tex.Data->Offset;
            textureData.RowPitch = tex.Data->Pitch;
            textureData.SlicePitch = tex.Data->Size;

            UpdateSubresources(commandList.Get(), m_textures[i].Get(), m_textureUploads[i].Get(), 0, 0, subresourceCount, &textureData);
            commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_textures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
        }

        // Describe and create an SRV.
        D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
        srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        srvDesc.Format = tex.Format;
        srvDesc.Texture2D.MipLevels = tex.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = 0;
        srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
        m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);

        // Move to the next descriptor slot.
        cbvSrvHandle.Offset(cbvSrvDescriptorSize);
    }
```



Inizio di un frame; non solo usa [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) per indicare che il buffer nascosto deve essere usato come destinazione di rendering, ma inizializza anche la risorsa frame (che chiama **ResourceBarrier** sul buffer depth stencil).


```C++
// Assemble the CommandListPre command list.
void D3D12Multithreading::BeginFrame()
{
    m_pCurrentFrameResource->Init();

    // Indicate that the back buffer will be used as a render target.
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    // Clear the render target and depth stencil.
    const float clearColor[] = { 0.0f, 0.0f, 0.0f, 1.0f };
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearDepthStencilView(m_dsvHeap->GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPre]->Close());
}

// Assemble the CommandListMid command list.
void D3D12Multithreading::MidFrame()
{
    // Transition our shadow map from the shadow pass to readable in the scene pass.
    m_pCurrentFrameResource->SwapBarriers();

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListMid]->Close());
}
```



Terminazione di un frame, che indica che il buffer nascosto viene ora usato per la presentazione.


```C++
// Assemble the CommandListPost command list.
void D3D12Multithreading::EndFrame()
{
    m_pCurrentFrameResource->Finish();

    // Indicate that the back buffer will now be used to present.
    m_pCurrentFrameResource->m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPost]->Close());
}
```



L'inizializzazione di una risorsa frame, chiamata all'inizio di un frame, esegue la transizione depth stencil buffer a scrivibile.


```C++
void FrameResource::Init()
{
    // Reset the command allocators and lists for the main thread.
    for (int i = 0; i < CommandListCount; i++)
    {
        ThrowIfFailed(m_commandAllocators[i]->Reset());
        ThrowIfFailed(m_commandLists[i]->Reset(m_commandAllocators[i].Get(), m_pipelineState.Get()));
    }

    // Clear the depth stencil buffer in preparation for rendering the shadow map.
    m_commandLists[CommandListPre]->ClearDepthStencilView(m_shadowDepthView, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    // Reset the worker command allocators and lists.
    for (int i = 0; i < NumContexts; i++)
    {
        ThrowIfFailed(m_shadowCommandAllocators[i]->Reset());
        ThrowIfFailed(m_shadowCommandLists[i]->Reset(m_shadowCommandAllocators[i].Get(), m_pipelineStateShadowMap.Get()));

        ThrowIfFailed(m_sceneCommandAllocators[i]->Reset());
        ThrowIfFailed(m_sceneCommandLists[i]->Reset(m_sceneCommandAllocators[i].Get(), m_pipelineState.Get()));
    }
}
```



Le barriere vengono scambiate nel fotogramma intermedio, con la transizione della mappa ombreggiatura da scrivibile a leggibile.


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



Il metodo Finish viene chiamato al termine di un frame, con la transizione della mappa ombreggiatura a uno stato comune.


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a>Esempio comune di promozione e decadimento dello stato

``` syntax
    // Create a buffer resource using D3D12_RESOURCE_STATE_COMMON as the init state
    ID3D12Resource *pResource;
    CreateCommittedVertexBufferInCommonState(1024, &pResource);

    // Copy data to the buffer without the need for a barrier.
    // Promotes pResource state to D3D12_RESOURCE_STATE_COPY_DEST.
    pCommandList->CopyBufferRegion(pResource, 0, pOtherResource, 0, 1024); 

    // To use pResource as a vertex buffer a transition barrier is needed.
    // Note the StateBefore is D3D12_RESOURCE_STATE_COPY_DEST.
    D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TYPE_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_FLAG_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COPY_DEST;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    // Use pResource as a vertex buffer
    D3D12_VERTEX_BUFFER_VIEW vbView;
    vbView.BufferLocation = pResource->GetGPUVirtualAddress();
    vbView.SizeInBytes = 1024;
    vbView.StrideInBytes = sizeof(MyVertex);

    pCommandList->IASetVertexBuffers(0, 1, &vbView);
    pCommandList->Draw();

    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 
    pCommandList->Reset(pAllocator, pPipelineState);

    // Since the reset command list will be executed in a separate call to 
    // ExecuteCommandLists, the previous state of pResource
    // will have decayed to D3D12_RESOURCE_STATE_COMMON so, again, no barrier is needed
    pCommandList->CopyBufferRegion(pResource, 0, pDifferentResource, 0, 1024);

    FinishRecordingCommandList(pCommandList);
    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 

    WaitForQueue(pCommandQueue);

    // The previous ExecuteCommandLists call has finished so 
    // pResource has decayed to D3D12_RESOURCE_STATE_COMMON
```

## <a name="example-of-split-barriers"></a>Esempio di barriere di divisione

L'esempio seguente illustra come usare una barriera di divisione per ridurre i blocchi della pipeline. Il codice seguente non usa barriere di divisione:

``` syntax
 D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource
    OtherStuff(); // .. other gpu work

    // Transition pResource to PIXEL_SHADER_RESOURCE
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    Read(pResource); // ... read from pResource
```

Il codice seguente usa le barriere di divisione:

``` syntax
D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource

    // Done writing to pResource. Start barrier to PIXEL_SHADER_RESOURCE and
    // then do other work
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_BEGIN_ONLY;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    OtherStuff(); // .. other gpu work

    // Need to read from pResource so end barrier
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_END_ONLY;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    Read(pResource); // ... read from pResource
```

## <a name="related-topics"></a>Argomenti correlati

[Esercitazioni video sull'apprendimento avanzato di DirectX: Barriere delle risorse e rilevamento dello stato](https://www.youtube.com/watch?v=nmB2XMasz2o)

[Sincronizzazione di più motori](./user-mode-heap-synchronization.md)

[Invio di lavoro in Direct3D 12](command-queues-and-command-lists.md)

[Uno sguardo all'interno delle barriere dello stato delle risorse D3D12](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

