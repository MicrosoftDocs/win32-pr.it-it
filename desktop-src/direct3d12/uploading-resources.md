---
title: Caricamento di diversi tipi di risorse
description: Illustra come usare un buffer per caricare sia i dati costanti del buffer che i dati del buffer dei vertici nella GPU e come sottoallocare e inserire correttamente i dati all'interno dei buffer.
ms.assetid: 255B0482-21D6-4276-8009-3F3891879CA1
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03d4755124bbadcdd255a6e99739b710845ab14
ms.sourcegitcommit: a30d0436a84986234df673c6def6694d5a8579f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113563781"
---
# <a name="uploading-different-types-of-resources"></a>Caricamento di diversi tipi di risorse

Illustra come usare un buffer per caricare sia i dati costanti del buffer che i dati del buffer dei vertici nella GPU e come sottoallocare e inserire correttamente i dati all'interno dei buffer. L'uso di un singolo buffer aumenta la flessibilità di utilizzo della memoria e offre alle applicazioni un controllo più stretto sull'utilizzo della memoria. Illustra anche le differenze tra i modelli Direct3D 11 e Direct3D 12 per il caricamento di diversi tipi di risorse.

## <a name="upload-different-types-of-resources"></a>Upload diversi tipi di risorse

In Direct3D 12 si crea un buffer per supportare diversi tipi di dati delle risorse per il caricamento e si copiano i dati delle risorse nello stesso buffer in modo simile per dati di risorse diversi. Vengono quindi create singole visualizzazioni per associare i dati delle risorse alla pipeline grafica nel modello di associazione di risorse Direct3D 12.

In Direct3D 11 si creano buffer separati per diversi tipi di dati delle risorse (si noti il diverso usato nel codice di esempio Direct3D 11 riportato di seguito), si associa in modo esplicito ogni buffer di risorse alla pipeline grafica e si aggiornano i dati delle risorse con metodi diversi in base a tipi di `BindFlags` risorse diversi.

Sia in Direct3D 12 che in Direct3D 11 è consigliabile caricare le risorse solo dove la CPU scriverà i dati una sola volta e la GPU la leggerà una sola volta.

In alcuni casi,
* la GPU leggerà i dati più volte oppure
* la GPU non leggerà i dati in modo lineare o
* il rendering è già notevolmente limitato alla GPU.

In questi casi, l'opzione migliore potrebbe essere usare [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) o [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) per copiare i dati del buffer di caricamento in una risorsa predefinita.

Una risorsa predefinita può risiedere nella memoria video fisica in GPU discrete.

### <a name="code-example-direct3d-11"></a>Esempio di codice: Direct3D 11

```cpp
// Direct3D 11: Separate buffers for each resource type.

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

### <a name="code-example-direct3d-12"></a>Esempio di codice: Direct3D 12

```cpp
// Direct3D 12: One buffer to accommodate different types of resources

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

Si noti l'uso delle strutture helper [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) e [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md).

## <a name="constants"></a>Costanti

Per impostare costanti, vertici e indici all'interno di un heap di caricamento o readback, usare le API seguenti.

-   [**ID3D12Device::CreateConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**ID3D12GraphicsCommandList::IASetVertexBuffers**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [**ID3D12GraphicsCommandList::IASetIndexBuffer**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a>Risorse

Le risorse sono il concetto direct3D che astrae l'utilizzo della memoria fisica GPU. Le risorse richiedono lo spazio degli indirizzi virtuali GPU per accedere alla memoria fisica. La creazione di risorse è a thread libero.

Esistono tre tipi di risorse per quanto riguarda la creazione di indirizzi virtuali e la flessibilità in Direct3D 12.

### <a name="committed-resources"></a>Risorse di cui è stato eseguito il commit

Le risorse di cui è stato eseguito il commit sono l'idea più comune di risorse Direct3D nelle generazioni. La creazione di una risorsa di questo tipo alloca un intervallo di indirizzi virtuali, un heap implicito sufficientemente grande da adattarsi all'intera risorsa ed esegue il commit dell'intervallo di indirizzi virtuali nella memoria fisica incapsulata dall'heap. Le proprietà heap implicite devono essere passate in modo che corrispondano alla parità funzionale con le versioni precedenti di Direct3D. Vedere [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

### <a name="reserved-resources"></a>Risorse riservate

Le risorse riservate sono equivalenti alle risorse affiancate Direct3D 11. Al momento della creazione, viene allocato solo un intervallo di indirizzi virtuali e non ne viene eseguito il mapping ad alcun heap. L'applicazione esegue il mapping di tali risorse agli heap in un secondo momento. Le funzionalità di tali risorse sono attualmente invariate rispetto a Direct3D 11, perché possono essere mappate a un heap con una granularità del riquadro di 64 KB con [**UpdateTileMappings.**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) Vedere [**ID3D12Device::CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).

### <a name="placed-resources"></a>Risorse posizionate

Una novità di Direct3D 12 è la creazione di heap separati dalle risorse. Successivamente, è possibile individuare più risorse all'interno di un singolo heap. È possibile farlo senza creare risorse affiancate o riservate, abilitando le funzionalità per tutti i tipi di risorse che possono essere create direttamente dall'applicazione. È possibile che più risorse si sovrappongano ed è necessario usare [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) per usare di nuovo correttamente la memoria fisica. Fare riferimento [**a ID3D12Device::CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).

## <a name="resource-size-reflection"></a>Reflection delle dimensioni delle risorse

È necessario usare la reflection delle dimensioni delle risorse per comprendere la quantità di trame di spazio con layout di trama sconosciuti necessari negli heap. Sono supportati anche i buffer, ma soprattutto per praticità.

È necessario essere a conoscenza delle principali discrepanze di allineamento, per facilitare la creazione di un pacchetto di risorse più denso.

Ad esempio, una matrice a elemento singolo con  un buffer a un byte restituisce dimensioni di 64 KB e *allineamento* di 64 KB, perché i buffer possono essere allineati solo a 64 KB.

Inoltre, una matrice a tre elementi con due trame allineate a 64 KB a texel singolo e una trama allineata a 4 MB a texel singolo segnala dimensioni diverse in base all'ordine della matrice. Se le trame allineate a 4 MB si trova al centro, la dimensione *risultante* è 12 MB. In caso contrario, la dimensione risultante è 8 MB. L'allineamento restituito sarebbe sempre di 4 MB, il superset di tutti gli allineamenti nella matrice di risorse.

Fare riferimento alle API seguenti.

- [**INFORMAZIONI SULL'ALLOCAZIONE DELLE RISORSE D3D12 \_ \_ \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
- [**GetResourceAllocationInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a>Allineamento del buffer

Le restrizioni di allineamento del buffer non sono cambiate rispetto a Direct3D 11, in particolare:

- 4 MB per trame multi-campione.
- 64 KB per trame e buffer a campione singolo.

## <a name="related-topics"></a>Argomenti correlati

* [Sottoallocazione all'interno dei buffer](large-buffers.md)
