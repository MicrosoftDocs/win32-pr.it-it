---
title: Caricamento di diversi tipi di risorse
description: Viene illustrato come utilizzare un buffer per caricare sia i dati del buffer costante che i dati del buffer dei vertici nella GPU e come suddividere e collocare correttamente i dati all'interno dei buffer.
ms.assetid: 255B0482-21D6-4276-8009-3F3891879CA1
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2edca2cd9f4d3becf5036056a89f91c50f2c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104067"
---
# <a name="uploading-different-types-of-resources"></a>Caricamento di diversi tipi di risorse

Viene illustrato come utilizzare un buffer per caricare sia i dati del buffer costante che i dati del buffer dei vertici nella GPU e come suddividere e collocare correttamente i dati all'interno dei buffer. L'utilizzo di un singolo buffer aumenta la flessibilità di utilizzo della memoria e fornisce alle applicazioni un controllo più rigoroso sull'utilizzo della memoria. Mostra anche le differenze tra i modelli D3D11 e D3D12 per il caricamento di diversi tipi di risorse.

-   [Caricare tipi diversi di risorse](#upload-different-types-of-resources)
    -   [Esempio di codice: D3D11](#code-example-d3d11)
    -   [Esempio di codice: D3D12](#code-example-d3d12)
-   [Costanti](#constants)
-   [Risorse](#uploading-different-types-of-resources)
-   [Reflection delle dimensioni delle risorse](#resource-size-reflection)
-   [Allineamento buffer](#buffer-alignment)
-   [Argomenti correlati](#related-topics)

## <a name="upload-different-types-of-resources"></a>Caricare tipi diversi di risorse

In D3D12 le applicazioni creano un buffer per supportare diversi tipi di dati delle risorse per il caricamento e copiano i dati delle risorse nello stesso buffer in modo analogo per i dati di risorse differenti. Vengono quindi create visualizzazioni singole per associare i dati delle risorse alla pipeline grafica nel nuovo modello di associazione di risorse.

In D3D11, le applicazioni creano buffer distinti per i diversi tipi di dati delle risorse (si noti il diverso `BindFlags` usato nel codice di esempio d3d11 seguente), associando in modo esplicito ogni buffer delle risorse alla pipeline grafica e aggiornando i dati delle risorse con metodi diversi in base ai diversi tipi di risorse.

In D3D12 e D3D11, le applicazioni devono usare solo le risorse di caricamento in cui la CPU scriverà i dati una sola volta e la GPU lo leggerà una volta. Se i dati vengono letti più volte dalla GPU, la GPU non leggerà i dati in modo lineare oppure il rendering sarà già limitato a una GPU. L'opzione migliore potrebbe consistere nell'usare [**ID3D12GraphicsCommandList:: CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) o [**ID3D12GraphicsCommandList:: CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) per copiare i dati del buffer di caricamento in una risorsa predefinita. Una risorsa predefinita può risiedere nella memoria video fisica sulle GPU discrete.

### <a name="code-example-d3d11"></a>Esempio di codice: D3D11

``` syntax
// D3D11: Separate buffers for each resource type.

void main()
{
    // ...

    // Create a constant buffer.
    float constantBufferData[] = ...;

    D3D11_BUFFER_DESC constantBufferDesc = {0};  
    constantBufferDesc.ByteWidth = sizeof(constantBufferData);  
    constantBufferDesc.Usage = D3D11_USAGE_DYNAMIC;  
    constantBufferDesc.BindFlags = D3D11_BIND_CONSTANT_BUFFER;  
    constantBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;  

    ComPtr<ID3D11Buffer> constantBuffer;
    d3dDevice->CreateBuffer(  
        &constantBufferDesc,  
        NULL,
        &constantBuffer  
        );

    // Create a vertex buffer.
    float vertexBufferData[] = ...;

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(vertexBufferData);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;

    ComPtr<ID3D11Buffer> vertexBuffer;
    d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        NULL,
        &vertexBuffer
        );

    // ...
}

void DrawFrame()
{
    // ...

    // Bind buffers to the graphics pipeline.
    d3dDeviceContext->VSSetConstantBuffers(0, 1, constantBuffer.Get());
    d3dDeviceContext->IASetVertexBuffers(0, 1, vertexBuffer.Get(), ...);

    // Update the constant buffer.
    D3D11_MAPPED_SUBRESOURCE mappedResource;  
    d3dDeviceContext->Map(
        constantBuffer.Get(),
        0, 
        D3D11_MAP_WRITE_DISCARD,
        0,
        &mappedResource
        );
    memcpy(mappedResource.pData, constantBufferData,
        sizeof(contatnBufferData));
    d3dDeviceContext->Unmap(constantBuffer.Get(), 0);  

    // Update the vertex buffer.
    d3dDeviceContext->UpdateSubresource(
        vertexBuffer.Get(),
        0,
        NULL,
        vertexBufferData,
        sizeof(vertexBufferData),
        0
    );

    // ...
}
```

### <a name="code-example-d3d12"></a>Esempio di codice: D3D12

``` syntax
// D3D12: One buffer to accommodate different types of resources

ComPtr<ID3D12Resource> m_spUploadBuffer;
UINT8* m_pDataBegin = nullptr;    // starting position of upload buffer
UINT8* m_pDataCur = nullptr;      // current position of upload buffer
UINT8* m_pDataEnd = nullptr;      // ending position of upload buffer

void main()
{
    //
    // Initialize an upload buffer
    //

    InitializeUploadBuffer(64 * 1024);

    // ...
}

void DrawFrame()
{
    // ...

    // Set vertices data to the upload buffer.

    float vertices[] = ...;
    UINT verticesOffset = 0;
    ThrowIfFailed(
        SetDataToUploadBuffer(
            vertices, sizeof(float), sizeof(vertices) / sizeof(float),
            sizeof(float), 
            verticesOffset
            ));

    // Set constant data to the upload buffer.

    float constants[] = ...;
    UINT constantsOffset = 0;
    ThrowIfFailed(
        SetDataToUploadBuffer(
            constants, sizeof(float), sizeof(constants) / sizeof(float), 
            D3D12_CONSTANT_BUFFER_DATA_PLACEMENT_ALIGNMENT, 
            constantsOffset
            ));

    // Create vertex buffer views for the new binding model.

    D3D12_VERTEX_BUFFER_VIEW vertexBufferViewDesc = {
        m_spUploadBuffer->GetGPUVirtualAddress() + verticesOffset,
        sizeof(vertices), // size
        sizeof(float) * 4,  // stride
    };

    commandList->IASetVertexBuffers( 
        0,
        1,
        &vertexBufferViewDesc,
        ));

    // Create constant buffer views for the new binding model.

    D3D12_CONSTANT_BUFFER_VIEW_DESC constantBufferViewDesc = {
        m_spUploadBuffer->GetGPUVirtualAddress() + constantsOffset,
        sizeof(constants) // size
         };

    d3dDevice->CreateConstantBufferView(
        &constantBufferViewDesc,
        ...
        ));

    // Continue command list building and execution ...
}

//
// Create an upload buffer and keep it always mapped.
//

HRESULT InitializeUploadBuffer(SIZE_T uSize)
{
    HRESULT hr = d3dDevice->CreateCommittedResource(
         &CD3DX12_HEAP_PROPERTIES( D3D12_HEAP_TYPE_UPLOAD ),    
               D3D12_HEAP_FLAG_NONE, 
               &CD3DX12_RESOURCE_DESC::Buffer( uSize ), 
               D3D12_RESOURCE_STATE_GENERIC_READ, nullptr,  
               IID_PPV_ARGS( &m_spUploadBuffer ) );

    if (SUCCEEDED(hr))
    {
        void* pData;
        //
        // No CPU reads will be done from the resource.
        //
        CD3DX12_RANGE readRange(0, 0);
        m_spUploadBuffer->Map( 0, &readRange, &pData ); 
        m_pDataCur = m_pDataBegin = reinterpret_cast< UINT8* >( pData );
        m_pDataEnd = m_pDataBegin + uSize;
    }
    return hr;
}

//
// Sub-allocate from the buffer, with offset aligned.
//

HRESULT SuballocateFromBuffer(SIZE_T uSize, UINT uAlign)
{
    m_pDataCur = reinterpret_cast< UINT8* >(
        Align(reinterpret_cast< SIZE_T >(m_pDataCur), uAlign)
        );

    return (m_pDataCur + uSize > m_pDataEnd) ? E_INVALIDARG : S_OK;
}

//
// Place and copy data to the upload buffer.
//

HRESULT SetDataToUploadBuffer(
    const void* pData, 
    UINT bytesPerData, 
    UINT dataCount, 
    UINT alignment, 
    UINT& byteOffset
    )
{
    SIZE_T byteSize = bytesPerData * dataCount;
    HRESULT hr = SuballocateFromBuffer(byteSize, alignment);
    if (SUCCEEDED(hr))
    {
        byteOffset = UINT(m_pDataCur - m_pDataBegin);
        memcpy(m_pDataCur, pData, byteSize); 
        m_pDataCur += byteSize;
    }
    return hr;
}

//
// Align uLocation to the next multiple of uAlign.
//

UINT Align(UINT uLocation, UINT uAlign)
{
    if ( (0 == uAlign) || (uAlign & (uAlign-1)) )
    {
        ThrowException("non-pow2 alignment");
    }

    return ( (uLocation + (uAlign-1)) & ~(uAlign-1) );
}
```

Si noti l'uso delle strutture helper [**CD3DX12 \_ \_ Proprietà heap**](cd3dx12-heap-properties.md) e [**CD3DX12 \_ Resource \_ desc**](cd3dx12-resource-desc.md).

## <a name="constants"></a>Costanti

Per impostare costanti, vertici e indici in un heap upload o readback, usare le API seguenti:

-   [**ID3D12Device::CreateConstantBufferView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**ID3D12GraphicsCommandList::IASetVertexBuffers**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [**ID3D12GraphicsCommandList::IASetIndexBuffer**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a>Risorse

Le risorse sono il concetto di D3D che astrae l'utilizzo della memoria fisica della GPU. Le risorse richiedono lo spazio degli indirizzi virtuali della GPU per accedere alla memoria fisica. La creazione di risorse è a thread libero.

Sono disponibili tre tipi di risorse per quanto riguarda la creazione e la flessibilità degli indirizzi virtuali in D3D12:

-   Risorse sottoposte a commit

    Le risorse di cui è stato eseguito il commit sono l'idea più comune delle risorse D3D nelle generazioni. La creazione di una risorsa di questo tipo consente di allocare l'intervallo di indirizzi virtuali, un heap implicito sufficientemente grande da adattarsi all'intera risorsa ed eseguire il commit dell'intervallo di indirizzi virtuali nella memoria fisica incapsulata dall'heap. Le proprietà dell'heap implicite devono essere passate per corrispondere alla parità funzionale con le versioni D3D precedenti. Vedere [**ID3D12Device:: CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

-   Risorse riservate

    Le risorse riservate sono equivalenti alle risorse D3D11 affiancate. Al momento della creazione, viene allocato solo un intervallo di indirizzi virtuali e non viene eseguito il mapping ad alcun heap. L'applicazione eseguirà il mapping di tali risorse agli heap in un secondo momento. Le funzionalità di tali risorse sono attualmente invariate rispetto a D3D11, perché è possibile eseguirne il mapping a un heap a una granularità del riquadro 64KB con [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings). Vedere [ **ID3D12Device:: CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)

-   Risorse posizionate

    Nuove per D3D12, le applicazioni possono creare heap distinti dalle risorse. Successivamente, l'applicazione può individuare più risorse all'interno di un singolo heap. Questa operazione può essere eseguita senza creare risorse affiancate o riservate, abilitando le funzionalità per tutti i tipi di risorse che possono essere creati direttamente dalle applicazioni. È possibile che più risorse si sovrappongano e che l'applicazione debba utilizzare `TiledResourceBarrier` per riutilizzare correttamente la memoria fisica. Vedere [ **ID3D12Device:: CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)

## <a name="resource-size-reflection"></a>Reflection delle dimensioni delle risorse

Le applicazioni devono usare la reflection delle dimensioni delle risorse per comprendere la quantità di trame della stanza con layout di trama sconosciuti richiesti negli heap. Sono supportati anche i buffer, ma per lo più per praticità.

Le applicazioni devono essere a conoscenza delle principali discrepanze di allineamento, per aiutare a comprimere più densamente le risorse.

Ad esempio, una matrice a elemento singolo con un buffer a un byte restituisce una dimensione di 64KB e un allineamento di 64KB, in quanto i buffer attualmente possono essere allineati solo 64KB.

Inoltre, una matrice a tre elementi con due trame allineate 64KB a Texel singolo e una trama a singolo Texel 4 bit allineata segnala dimensioni diverse in base all'ordine della matrice. Se le trame da 4 MB sono allineate al centro, le dimensioni risultanti sono 12 MB. In caso contrario, la dimensione risultante è 8 MB. L'allineamento restituito sarà sempre di 4 MB, il super-set di tutti gli allineamenti nella matrice di risorse.

Fare riferimento alle seguenti API:

-   [**\_Informazioni sull' \_ allocazione delle risorse D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
-   [**GetResourceAllocationInfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a>Allineamento buffer

Le restrizioni di allineamento del buffer non sono state modificate da D3D11, in particolare:

-   4 MB per le trame multicampionamento.
-   64 KB per trame e buffer a singolo campione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sottoallocazione nei buffer](large-buffers.md)
</dt> </dl>

 

 




