---
title: Caricamento dei dati di trama tramite buffer
description: Il caricamento di dati di trama 2D o 3D è simile al caricamento di dati 1D, ad eccezione del fatto che le applicazioni devono prestare maggiore attenzione all'allineamento dei dati correlato al passo della riga.
ms.assetid: 22A25A94-A45C-482D-853A-FA6860EE7E4E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aadbd1e71b3c9895b75c973397488472b57f8eb1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548888"
---
# <a name="uploading-texture-data-through-buffers"></a>Caricamento dei dati di trama tramite buffer

Il caricamento di dati di trama 2D o 3D è simile al caricamento di dati 1D, ad eccezione del fatto che le applicazioni devono prestare maggiore attenzione all'allineamento dei dati correlato al passo della riga. I buffer possono essere usati in modo ortogonale e simultaneamente da più parti della pipeline grafica e sono molto flessibili.

-   [Caricare i dati di trama tramite buffer](#upload-texture-data-via-buffers)
-   [Copia](#copying)
-   [Mapping e annullamento del mapping](#mapping-and-unmapping)
-   [Allineamento buffer](#buffer-alignment)
-   [Argomenti correlati](#related-topics)

## <a name="upload-texture-data-via-buffers"></a>Caricare i dati di trama tramite buffer

Le applicazioni devono caricare i dati tramite [**ID3D12GraphicsCommandList:: CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) o [**ID3D12GraphicsCommandList:: CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion). È molto più probabile che i dati della trama siano più grandi, a cui si accede ripetutamente e che possano trarre vantaggio dalla migliore cache coerenza dei layout di memoria non lineare rispetto ad altri dati della risorsa. Quando i buffer vengono usati in D3D12, le applicazioni hanno il controllo completo sul posizionamento e la disposizione dei dati associati alla copia dei dati delle risorse, purché i requisiti di allineamento della memoria siano soddisfatti.

Nell'esempio viene evidenziata la posizione in cui l'applicazione appiattisce semplicemente i dati 2D in 1D prima di posizionarli nel buffer. Per lo scenario mipmap 2D, l'applicazione può rendere flat ogni sottorisorsa in modo discreta e usare rapidamente un algoritmo di sottoallocazione 1D oppure usare una tecnica di allocazione 2D più complessa per ridurre al minimo l'utilizzo della memoria del video. Si prevede che la prima tecnica venga utilizzata più spesso perché è più semplice. La seconda tecnica può essere utile quando si imballano i dati su un disco o in una rete. In entrambi i casi, l'applicazione deve comunque chiamare le API di copia per ogni risorsa secondaria.

``` syntax
// Prepare a pBitmap in memory, with bitmapWidth, bitmapHeight, and pixel format of DXGI_FORMAT_B8G8R8A8_UNORM. 
//
// Sub-allocate from the buffer for texture data.
//

D3D12_SUBRESOURCE_FOOTPRINT pitchedDesc = { 0 };
pitchedDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
pitchedDesc.Width = bitmapWidth;
pitchedDesc.Height = bitmapHeight;
pitchedDesc.Depth = 1;
pitchedDesc.RowPitch = Align(bitmapWidth * sizeof(DWORD), D3D12_TEXTURE_DATA_PITCH_ALIGNMENT);

//
// Note that the helper function UpdateSubresource in D3DX12.h, and ID3D12Device::GetCopyableFootprints 
// can help applications fill out D3D12_SUBRESOURCE_FOOTPRINT and D3D12_PLACED_SUBRESOURCE_FOOTPRINT structures.
//
// Refer to the D3D12 Code example for the previous section "Uploading Different Types of Resources"
// for the code for SuballocateFromBuffer.
//

SuballocateFromBuffer(
    pitchedDesc.Height * pitchedDesc.RowPitch,
    D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT
    );

D3D12_PLACED_SUBRESOURCE_FOOTPRINT placedTexture2D = { 0 };
placedTexture2D.Offset = m_pDataCur – m_pDataBegin;
placedTexture2D.Footprint = pitchedDesc;

//
// Copy texture data from DWORD* pBitmap->pixels to the buffer
//

for (UINT y = 0; y < bitmapHeight; y++)
{
  UINT8 *pScan = m_pDataBegin + placedTexture2D.Offset + y * pitchedDesc.RowPitch;
  memcpy( pScan, &(pBitmap->pixels[y * bitmapWidth]), sizeof(DWORD) * bitmapWidth );
}

//
// Create default texture2D resource.
//

D3D12_RESOURCE_DESC  textureDesc { ... };

CComPtr<ID3D12Resource> texture2D;
d3dDevice->CreateCommittedResource( 
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT), 
        D3D12_HEAP_FLAG_NONE, &textureDesc, 
        D3D12_RESOURCE_STATE_COPY_DEST, 
        nullptr, 
        IID_PPV_ARGS(&texture2D) );

//
// Copy heap data to texture2D.
//

commandList->CopyTextureRegion( 
        &CD3DX12_TEXTURE_COPY_LOCATION( texture2D, 0 ), 
        0, 0, 0, 
        &CD3DX12_TEXTURE_COPY_LOCATION( m_spUploadHeap, placedTexture2D ), 
        nullptr );
```

Si noti l'uso delle strutture helper [**CD3DX12 le \_ \_ proprietà dell'heap**](cd3dx12-heap-properties.md) e il [**\_ \_ \_ percorso di copia della trama CD3DX12**](cd3dx12-texture-copy-location.md)e i metodi [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) e [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).

## <a name="copying"></a>asincrona

I metodi D3D12 consentono alle applicazioni di sostituire D3D11 [**UpdateSubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)e i dati iniziali delle risorse. Una singola risorsa di sottorisorsa 3D che vale la pena dei dati di trama principali potrebbe trovarsi nelle risorse del buffer. [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) è in grado di copiare i dati di trama dal buffer a una risorsa di trama con un layout di trama sconosciuto e viceversa. Le applicazioni devono preferire questo tipo di tecnica per popolare le risorse GPU a cui si accede di frequente, creando buffer di grandi dimensioni in un heap di caricamento durante la creazione delle risorse GPU a cui si accede di frequente in un heap predefinito privo di accesso alla CPU. Una tecnica di questo tipo supporta in modo efficiente GPU discrete e le relative grandi quantità di memoria non accessibile dalla CPU, senza compromettere in genere le architetture UMA.

Si notino le due costanti seguenti:

``` syntax
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [**\_Footprint delle sottorisorse D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [**\_Footprint di \_ risorse sottoposte a D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [**\_ \_ Percorso copia trama \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [**\_Tipo di \_ Copia \_ trama D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**ID3D12GraphicsCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**ID3D12CommandQueue::UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a>Mapping e annullamento del mapping

[**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) e [**annullare**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) possono essere chiamati da più thread in modo sicuro. La prima chiamata a **Map** alloca un intervallo di indirizzi virtuali della CPU per la risorsa. L'ultima chiamata a **annullare** dealloca l'intervallo di indirizzi virtuali della CPU. L'indirizzo virtuale della CPU viene comunemente restituito all'applicazione.

Ogni volta che i dati vengono passati tra la CPU e la GPU tramite le risorse negli heap readback, è necessario usare [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) e [**annullare**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) per supportare tutti i sistemi D3D12 è supportato in. Il minor numero possibile di intervalli consente di massimizzare l'efficienza sui sistemi che richiedono intervalli (vedere [**l' \_ intervallo di D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).

Le prestazioni degli strumenti di debug traggono vantaggio non solo dall'utilizzo accurato degli intervalli in tutte le chiamate annullare della [**mappa**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)  /  [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) , ma anche dalle applicazioni che annullano il mapping delle risorse quando le modifiche alla CPU non verranno più eseguite.

Il metodo D3D11 di utilizzo della proprietà [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (con il set di parametri scarto) per rinominare le risorse non è supportato in D3D12. Le applicazioni devono implementare la ridenominazione delle risorse. Tutte le chiamate alla **mappa** sono IMPLICITamente prive \_ di sovrascrittura e multithread. È responsabilità dell'applicazione garantire che qualsiasi lavoro GPU pertinente contenuto negli elenchi di comandi sia terminato prima di accedere ai dati con la CPU. Le chiamate D3D12 a **Map** non scaricano in modo implicito i buffer dei comandi, né bloccano l'attesa del completamento del lavoro della GPU. Di conseguenza, **Map** e [**annullare**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) possono anche essere ottimizzati in alcuni scenari.

## <a name="buffer-alignment"></a>Allineamento buffer

Restrizioni di allineamento del buffer:

-   La copia della sottorisorsa lineare deve essere allineata a 512 byte (con il passo di riga allineato ai \_ \_ byte di allineamento del passo dei dati della trama D3D12 \_ \_ ).
-   Le letture dei dati costanti devono essere un multiplo di 256 byte a partire dall'inizio dell'heap, ovvero solo da indirizzi a 256 byte allineati.
-   La lettura dei dati dell'indice deve essere un multiplo della dimensione del tipo di dati dell'indice, ovvero solo da indirizzi che sono allineati naturalmente per i dati.
-   [**ID3D12GraphicsCommandList::D rawinstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) e [**ID3D12GraphicsCommandList::D**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) i dati rawindexedinstanced devono essere costituiti da offset multipli di 4 (ovvero solo da indirizzi DWORD allineati).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sottoallocazione nei buffer](large-buffers.md)
</dt> </dl>

 

 