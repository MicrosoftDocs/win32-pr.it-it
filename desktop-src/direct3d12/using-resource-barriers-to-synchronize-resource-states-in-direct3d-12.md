---
title: Uso delle barriere delle risorse per sincronizzare gli Stati delle risorse in Direct3D 12
description: Per ridurre l'utilizzo complessivo della CPU e consentire il multithreading e la pre-elaborazione dei driver, Direct3D 12 sposta la responsabilità della gestione dello stato per ogni risorsa dal driver di grafica all'applicazione.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c766f18e85ab8acc2ed0afad8e680d566a723a68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104548885"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a>Uso delle barriere delle risorse per sincronizzare gli Stati delle risorse in Direct3D 12

Per ridurre l'utilizzo complessivo della CPU e consentire il multithreading e la pre-elaborazione dei driver, Direct3D 12 sposta la responsabilità della gestione dello stato per ogni risorsa dal driver di grafica all'applicazione. Un esempio di stato per risorsa è se è attualmente possibile accedere a una risorsa di trama come tramite un Shader Resource View o come una visualizzazione di destinazione di rendering. In Direct3D 11 i driver sono necessari per tenere traccia di questo stato in background. Si tratta di un'operazione dispendiosa dal punto di vista della CPU e complica notevolmente qualsiasi tipo di progettazione multithread. In Microsoft Direct3D 12 la maggior parte dello stato per ogni risorsa viene gestita dall'applicazione con una singola API, [**ID3D12GraphicsCommandList:: ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).

-   [Uso dell'API ResourceBarrier per gestire lo stato per risorsa](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [Stati delle risorse](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [Stati iniziali per le risorse](#initial-states-for-resources)
    -   [Restrizioni sullo stato delle risorse di lettura/scrittura](#readwrite-resource-state-restrictions)
    -   [Stati delle risorse per la presentazione dei buffer indietro](#resource-states-for-presenting-back-buffers)
    -   [Eliminazione di risorse](#discarding-resources)
-   [Transizioni di stato implicite](#implicit-state-transitions)
    -   [Innalzamento di stato comune](#common-state-promotion)
    -   [Stato decadimento in comune](#state-decay-to-common)
    -   [Implicazioni per le prestazioni](#performance-implications)
-   [Suddividere le barriere](#split-barriers)
-   [Scenario di esempio di barriera delle risorse](#resource-barrier-example-scenario)
-   [Esempio di promozione e decadimento dello stato comune](#common-state-promotion-and-decay-sample)
-   [Esempio di barriere Split](#example-of-split-barriers)
-   [Argomenti correlati](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a>Uso dell'API ResourceBarrier per gestire lo stato per risorsa

[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifica al driver Graphics le situazioni in cui il driver potrebbe dover sincronizzare più accessi alla memoria in cui è archiviata una risorsa. Il metodo viene chiamato con una o più strutture di descrizione della barriera delle risorse che indicano il tipo di barriera della risorsa dichiarata.

Esistono tre tipi di barriere per le risorse:

-   **Barriera di transizione** : una barriera di transizione indica che un set di sottorisorse viene sottoposto a transizione tra diversi usi. Una struttura della [**\_ \_ \_ barriera di transizione delle risorse D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) viene utilizzata per specificare la sottorisorsa che esegue la transizione, nonché gli stati *before* e *after* della sottorisorsa.

    Il sistema verifica che le transizioni delle sottorisorse in un elenco di comandi siano coerenti con le transizioni precedenti nello stesso elenco di comandi. Il livello di debug rileva ulteriormente lo stato della sottorisorsa per trovare altri errori, tuttavia questa convalida è conservativa e non esaustiva.

    Si noti che è possibile usare il \_ flag D3D12 Resource \_ Barrier \_ All \_ Resources per specificare che tutte le sottorisorse all'interno di una risorsa sono in fase di transizione.

-   **Barriera di alias** : una barriera di aliasing indica una transizione tra gli utilizzi di due risorse diverse con mapping sovrapposti nello stesso heap. Questo vale sia per le risorse riservate che per quelle posizionate. Una struttura di barriera per l' [**\_ \_ aliasing \_ delle risorse D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) viene usata per specificare sia la risorsa *before* che la risorsa *after* .

    Si noti che una o entrambe le risorse possono essere NULL, a indicare che qualsiasi risorsa affiancata potrebbe causare l'aliasing. Per ulteriori informazioni sull'utilizzo di risorse affiancate, vedere [risorse affiancate](../direct3d11/tiled-resources.md) e [risorse affiancate al volume](volume-tiled-resources.md).

-   **Barriera di visualizzazione di accesso non ordinato (UAV)** : una barriera UAV indica che tutti gli accessi UAV, sia di lettura che di scrittura, a una determinata risorsa devono essere completati tra gli accessi UAV futuri, sia di lettura che di scrittura. Non è necessario che un'app inserisca una barriera UAV tra due chiamate di estrazione o di invio che leggono solo da un UAV. Non è inoltre necessario inserire una barriera UAV tra due chiamate di richiamo o di invio che scrivono nello stesso UAV se l'applicazione sa che è sicuro eseguire l'accesso UAV in qualsiasi ordine. Per specificare la risorsa UAV a cui si applica la barriera, viene usata una struttura di [**\_ \_ \_ barriera UAV della risorsa D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) . L'applicazione può specificare NULL per il UAV della barriera, che indica che qualsiasi accesso UAV potrebbe richiedere la barriera.

Quando [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) viene chiamato con una matrice di descrizioni della barriera delle risorse, l'API si comporta come se venisse chiamata una volta per ogni elemento, nell'ordine in cui sono state specificate.

In un determinato momento, una sottorisorsa si trova esattamente in uno stato, determinato dal set di flag di stato [**\_ delle risorse \_ D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) forniti a [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier). L'applicazione deve garantire che gli stati *before* e *after* delle chiamate consecutive a **ResourceBarrier** accettino.

> [!TIP]
>
> Le applicazioni devono eseguire il batch di più transizioni in una chiamata API laddove possibile.

 

### <a name="resource-states"></a>Stati delle risorse

Per l'elenco completo degli Stati delle risorse tra cui una risorsa può passare, vedere l'argomento di riferimento per l'enumerazione [**\_ \_ degli Stati delle risorse D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) .

Per le barriere Split Resource, vedere [**anche \_ \_ \_ flag di barriera delle risorse D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).

### <a name="initial-states-for-resources"></a>Stati iniziali per le risorse

Le risorse possono essere create con qualsiasi stato iniziale specificato dall'utente (valido per la descrizione della risorsa), con le eccezioni seguenti:

-   Gli heap di caricamento devono iniziare con lo stato della \_ risorsa \_ D3D12 \_ lettura generica \_ , che è una combinazione OR bit per bit di:
    -   \_ \_ Vertex dello stato della risorsa D3D12 \_ \_ e \_ \_ buffer costante
    -   \_ \_ \_ Buffer indice stato risorsa \_ D3D12
    -   \_Origine della \_ copia dello stato della risorsa \_ D3D12 \_
    -   \_ \_ Risorsa dello stato della risorsa \_ non \_ pixel \_ shader \_ di D3D12
    -   \_ \_ \_ \_ Risorsa pixel shader dello stato della risorsa D3D12 \_
    -   \_ \_ \_ Argomento indiretto dello stato della risorsa D3D12 \_
-   Gli heap readback devono iniziare nello stato di \_ \_ copia dello stato della risorsa D3D12 \_ \_ .
-   I buffer indietro della catena di scambio iniziano automaticamente nello \_ stato comune della risorsa D3D12 \_ \_ .

Prima che un heap possa essere la destinazione di un'operazione di copia GPU, in genere l'heap deve prima essere passato allo \_ \_ stato di copia dello stato della risorsa D3D12 \_ \_ . Tuttavia, le risorse create negli heap di caricamento devono iniziare in e non possono essere modificate dallo \_ stato di lettura generico poiché solo la CPU eseguirà la scrittura. Viceversa, le risorse di cui è stato eseguito il commit create negli heap READBACK devono iniziare da e non possono essere modificate dallo stato di copia \_ dest.

### <a name="readwrite-resource-state-restrictions"></a>Restrizioni sullo stato delle risorse di lettura/scrittura

I bit di utilizzo dello stato delle risorse usati per descrivere lo stato di una risorsa sono divisi in Stati di sola lettura e di lettura/scrittura. L'argomento di riferimento per [**gli \_ \_ Stati della risorsa D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indica il livello di accesso in lettura/scrittura per ogni bit nell'enumerazione.

Al massimo, è possibile impostare un solo bit di lettura/scrittura per qualsiasi risorsa. Se è impostato un bit di scrittura, non è possibile impostare alcun bit di sola lettura per tale risorsa. Se non è impostato alcun bit di scrittura, è possibile impostare un numero qualsiasi di bit di lettura.

### <a name="resource-states-for-presenting-back-buffers"></a>Stati delle risorse per la presentazione dei buffer indietro

Prima che venga visualizzato un buffer nascosto, questo deve trovarsi nello \_ stato comune della risorsa D3D12 \_ \_ . Si noti che lo stato della risorsa D3D12 stato \_ risorsa \_ \_ presente è un sinonimo di D3D12 \_ risorsa \_ stato \_ comune ed entrambi hanno un valore pari a 0. Se [**IDXGISwapChain::P**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) reinviata (o [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) viene chiamato su una risorsa che non si trova attualmente in questo stato, viene generato un avviso di livello debug.

### <a name="discarding-resources"></a>Eliminazione di risorse

Tutte le sottorisorse in una risorsa devono trovarsi nello \_ stato di destinazione di rendering o \_ nello stato di scrittura di profondità, rispettivamente per le destinazioni di rendering o per le risorse dello stencil di profondità, quando viene chiamato [**ID3D12GraphicsCommandList::D iscardresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) .

## <a name="implicit-state-transitions"></a>Transizioni di stato implicite

Le risorse possono essere "promosse" solo dal \_ comune stato della risorsa D3D12 \_ \_ . Analogamente, le risorse risulteranno "decadimento" solo per \_ lo stato della risorsa D3D12 \_ \_ comune.

### <a name="common-state-promotion"></a>Innalzamento di stato comune

Tutte le risorse del buffer e le trame con il \_ flag di risorsa D3D12 \_ consentono di impostare il \_ \_ \_ flag di accesso simultaneo in modo implicito dallo \_ stato della risorsa D3D12 \_ \_ comune allo stato pertinente per il primo accesso alla GPU, inclusa la lettura generica \_ per coprire qualsiasi scenario di lettura. È possibile accedere a qualsiasi risorsa nello stato comune in un unico stato con

<dl> 1 flag di scrittura o  
uno o più flag di lettura  
</dl>

Le risorse possono essere promosse dallo stato comune in base alla tabella seguente:



| Flag di stato                    | Stato promuovibile                             |                                      |
|-------------------------------|----------------------------------------------|--------------------------------------|
|                               | **Buffer e trame Simultaneous-Access** | **Trame senza accesso simultaneo** |
| VERTEX \_ e \_ \_ buffer costante | Sì                                          | No                                   |
| \_buffer indice                 | Sì                                          | No                                   |
| destinazione di rendering \_                | Sì                                          | No                                   |
| accesso non ordinato \_             | Sì                                          | No                                   |
| scrittura APPROFONDIta \_                  | No<sup>\*</sup>                              | No                                   |
| lettura APPROFONDIta \_                   | No<sup>\*</sup>                              | No                                   |
| \_ \_ risorsa shader non pixel \_  | Sì                                          | Sì                                  |
| \_risorsa pixel shader \_       | Sì                                          | Sì                                  |
| FLUSSO in \_ uscita                   | Sì                                          | No                                   |
| argomento indiretto \_            | Sì                                          | No                                   |
| COPIA \_ dest                    | Sì                                          | Sì                                  |
| COPIA \_ origine                  | Sì                                          | Sì                                  |
| RISOLvi \_ dest                 | Sì                                          | No                                   |
| RISOLvi \_ origine               | Sì                                          | No                                   |
| PREDICAZIONE                   | Sì                                          | No                                   |



 

<sup>\*</sup>Le risorse di stencil Depth devono essere trame con accesso non simultaneo e pertanto non possono mai essere innalzate di livello in modo implicito.

Quando si verifica questo accesso, la promozione agisce come una barriera di risorsa implicita. Per gli accessi successivi, le barriere delle risorse saranno necessarie per modificare lo stato delle risorse, se necessario. Si noti che la promozione da uno stato di lettura promosso a più Stati di lettura è valida, ma questo non è il caso per gli Stati di scrittura.  
Se, ad esempio, una risorsa nello stato comune viene promossa alla \_ risorsa pixel shader \_ in una chiamata di progetto, può comunque essere promossa a NON_PIXEL \_ \_ risorsa shader | \_Risorsa pixel shader \_ in un'altra chiamata di progetto. Tuttavia, se viene usato in un'operazione di scrittura, ad esempio una destinazione di copia, una barriera di transizione dello stato della risorsa dagli Stati di lettura promossi combinati, qui NON_PIXEL \_ \_ risorsa shader | \_Risorsa pixel shader \_ per la copia di \_ dest è necessaria.  
Analogamente, se promosso da comune a copia \_ dest, una barriera è ancora necessaria per eseguire la transizione da copia \_ dest a destinazione di rendering \_ .

Si noti che la promozione dello stato comune è "Free" perché non è necessario che la GPU esegua le attese di sincronizzazione. La promozione rappresenta il fatto che le risorse nello stato comune non devono richiedere un ulteriore rilevamento del lavoro o del driver della GPU per supportare determinati accessi.

### <a name="state-decay-to-common"></a>Stato decadimento in comune

Il rovescio della promozione dello stato comune è il decadimento dello \_ stato della risorsa D3D12 \_ \_ comune. Le risorse che soddisfano determinati requisiti vengono considerate senza stato e restituiscono lo stato comune quando la GPU termina l'esecuzione di un'operazione [**oggetti executecommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) . Il decadimento non si verifica tra gli elenchi di comandi eseguiti insieme nella stessa chiamata **oggetti executecommandlist** .

Quando un'operazione [**oggetti executecommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) viene completata sulla GPU, le risorse seguenti determineranno il decadimento:

-   Risorse a cui si accede in una coda di copia *o*
-   Risorse del buffer per qualsiasi tipo di coda *o*
-   Le risorse di trama in qualsiasi tipo di coda con il \_ flag di risorsa D3D12 consentono il set di flag di \_ \_ \_ accesso simultaneo \_ *o*
-   Qualsiasi risorsa innalzata in modo implicito a uno stato di sola lettura.

Analogamente all'innalzamento di stato comune, il decadimento è gratuito in quanto non è necessaria alcuna sincronizzazione aggiuntiva. La combinazione di innalzamento di stato comune e decadimento può aiutare a eliminare molte transizioni [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) non necessarie. In alcuni casi, questo può offrire miglioramenti significativi delle prestazioni.

I buffer e le risorse di Simultaneous-Access decadono nello stato comune indipendentemente dal fatto che siano stati esplicitamente sottoposti a transizione usando barriere delle risorse o innalzate in modo implicito.

### <a name="performance-implications"></a>Implicazioni per le prestazioni

Quando si registrano transizioni [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) esplicite nelle risorse nello stato comune, è corretto usare lo stato \_ della risorsa D3D12 \_ \_ comune o qualsiasi stato promuovibile come valore di *rimboschimento* nella struttura della \_ barriera della transizione di risorse D3D12 \_ \_ . Questo consente la gestione dello stato tradizionale che ignora il decadimento automatico dei buffer e delle trame ad accesso simultaneo. Questo potrebbe non essere auspicabile, in quanto evitando che le chiamate **ResourceBarrier** di transizione con risorse note nello stato comune possano migliorare significativamente le prestazioni. Le barriere alle risorse possono essere costose. Sono progettati per forzare gli scaricamenti della cache, le modifiche al layout di memoria e altre sincronizzazioni che potrebbero non essere necessarie per le risorse già nello stato comune. Un elenco di comandi che usa una barriera delle risorse da uno stato non comune a un altro stato non comune in una risorsa attualmente nello stato comune può presentare un sovraccarico non necessario.

Evitare inoltre transizioni esplicite di [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) per \_ lo stato della risorsa D3D12, a \_ \_ meno che non sia assolutamente necessario (ad esempio, l'accesso successivo si trova in una coda dei comandi di copia che richiede che le risorse inizino nello stato comune). Una transizione eccessiva allo stato comune può rallentare notevolmente le prestazioni della GPU.

In sintesi, provare a basarsi sull'innalzamento di stato comune e il decadimento ogni volta che la semantica consente di uscire senza emettere chiamate [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) .

## <a name="split-barriers"></a>Suddividere le barriere

Una barriera di transizione delle risorse con il flag di blocco della \_ barriera delle risorse D3D12 \_ \_ \_ \_ inizia una barriera divisa e la barriera di transizione è detta in sospeso. Mentre la barriera è in sospeso, la risorsa (Sub) non può essere letta o scritta dalla GPU. L'unica barriera di transizione legale che può essere applicata a una risorsa (Sub) con una barriera in sospeso è uno con gli stessi stati *before* e *after* e il \_ flag di fine del flag di barriera della risorsa D3D12, la \_ \_ \_ \_ cui barriera completa la transizione in sospeso.

Le barriere Split forniscono suggerimenti alla GPU che una risorsa nello stato a verrà successivamente usata nello stato *B* in *un* secondo momento. In questo modo l'opzione GPU consente di ottimizzare il carico di lavoro di transizione, possibilmente riducendo o eliminando i blocchi di esecuzione. Il rilascio della barriera di sola fine garantisce che tutte le operazioni di transizione GPU siano finite prima di passare al comando successivo.

L'uso di barriere Split può contribuire a migliorare le prestazioni, soprattutto in scenari con più motori o in cui le risorse sono in lettura/scrittura in modo sparse in uno o più elenchi di comandi.

## <a name="resource-barrier-example-scenario"></a>Scenario di esempio di barriera delle risorse

Nei frammenti di codice seguenti viene illustrato l'utilizzo del metodo [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) in un esempio multithread.

Creazione della visualizzazione depth stencil, transizione a uno stato scrivibile.


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



Creazione della visualizzazione buffer dei vertici, prima modifica da uno stato comune a una destinazione, quindi da una destinazione a uno stato leggibile generico.


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



Creazione della visualizzazione buffer dell'indice, prima modifica da uno stato comune a una destinazione, quindi da una destinazione a uno stato leggibile generico.


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



Creazione di trame e visualizzazioni delle risorse dello shader. La trama viene modificata da uno stato comune a una destinazione e quindi da una destinazione a una risorsa pixel shader.


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



Inizio di un frame; Questa operazione non solo utilizza [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) per indicare che il backBuffer deve essere utilizzato come destinazione di rendering, ma inizializza anche la risorsa frame, che chiama **ResourceBarrier** sul buffer depth stencil.


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



Terminazione di un frame, che indica che il buffer nascosto è ora usato per presentare.


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



L'inizializzazione di una risorsa frame, chiamata quando si inizia un frame, esegue la transizione del buffer di depth stencil a scrivibile.


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



Le barriere sono invertite a metà Frame e la transizione della mappa Shadow da scrivibile a leggibile.


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



Finish viene chiamato quando viene terminato un frame, passando il mapping dell'ombreggiatura a uno stato comune.


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a>Esempio di promozione e decadimento dello stato comune

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

## <a name="example-of-split-barriers"></a>Esempio di barriere Split

Nell'esempio seguente viene illustrato come utilizzare una barriera Split per ridurre le stallo della pipeline. Il codice che segue non usa le barriere Split:

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

Il codice seguente usa le barriere Split:

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

[Esercitazioni video su DirectX Advanced Learning: barriere delle risorse e rilevamento dello stato](https://www.youtube.com/watch?v=nmB2XMasz2o)

[Sincronizzazione multimotore](./user-mode-heap-synchronization.md)

[Invio di lavoro in Direct3D 12](command-queues-and-command-lists.md)

[Uno sguardo all'interno delle barriere dello stato della risorsa D3D12](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

