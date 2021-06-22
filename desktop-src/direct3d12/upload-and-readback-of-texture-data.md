---
title: Caricamento di dati di trama tramite buffer
description: Il caricamento di dati di trama 2D o 3D è simile al caricamento di dati 1D, ad eccezione del fatto che le applicazioni devono prestare maggiore attenzione all'allineamento dei dati correlati all'altezza delle righe.
ms.assetid: 22A25A94-A45C-482D-853A-FA6860EE7E4E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72177be1fefbf102e901d28d47413c8bcff41ab
ms.sourcegitcommit: 39754f1af7853adff2525d0936afe9aad2066a9a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/22/2021
ms.locfileid: "112426965"
---
# <a name="uploading-texture-data-through-buffers"></a>Caricamento di dati di trama tramite buffer

Il caricamento di dati di trama 2D o 3D è simile al caricamento di dati 1D, ad eccezione del fatto che le applicazioni devono prestare maggiore attenzione all'allineamento dei dati correlati all'altezza delle righe. I buffer possono essere usati in modo ortogonale e simultaneo da più parti della pipeline grafica e sono molto flessibili.

-   [Caricare dati di trama tramite buffer](#upload-texture-data-via-buffers)
-   [Copia](#copying)
-   [Mapping e annullamento del mapping](#mapping-and-unmapping)
-   [Allineamento del buffer](#buffer-alignment)
-   [Argomenti correlati](#related-topics)

## <a name="upload-texture-data-via-buffers"></a>Caricare dati di trama tramite buffer

Le applicazioni devono caricare i dati [**tramite ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) [**o ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion). È molto più probabile che i dati di trama siano più grandi, a cui si accede ripetutamente e traggono vantaggio dalla coesistenza della cache migliorata dei layout di memoria non lineare rispetto ad altri dati delle risorse. Quando i buffer vengono usati in D3D12, le applicazioni hanno il controllo completo sul posizionamento e sulla disposizione dei dati associati alla copia dei dati delle risorse, purché siano soddisfatti i requisiti di allineamento della memoria.

L'esempio evidenzia dove l'applicazione appiatti semplicemente i dati 2D in 1D prima di posizionarlo nel buffer. Per lo scenario mipmap 2D, l'applicazione può appiattire ogni sotto-risorsa in modo discreto e usare rapidamente un algoritmo di sottoallocazione 1D oppure usare una tecnica di sottoallocazione 2D più complessa per ridurre al minimo l'utilizzo della memoria video. La prima tecnica dovrebbe essere usata più spesso perché è più semplice. La seconda tecnica può essere utile quando si imballa dati su un disco o in una rete. In entrambi i casi, l'applicazione deve comunque chiamare le API di copia per ogni risorsa secondaria.

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

Si noti l'uso delle strutture helper [**CD3DX12 \_ HEAP \_ PROPERTIES**](cd3dx12-heap-properties.md) e [**CD3DX12 \_ TEXTURE COPY \_ \_ LOCATION**](cd3dx12-texture-copy-location.md)e dei metodi [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) e [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).

## <a name="copying"></a>asincrona

I metodi D3D12 consentono alle applicazioni di sostituire i dati D3D11 [**UpdateSubresource,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource) [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)e i dati iniziali della risorsa. Una singola sottorisorsa 3D dei dati di trama principale di riga può trovarsi nelle risorse del buffer. [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) può copiare i dati di trama dal buffer a una risorsa trama con un layout di trama sconosciuto e viceversa. Le applicazioni devono preferire questo tipo di tecnica per popolare le risorse GPU a cui si accede di frequente, creando buffer di grandi dimensioni in un heap UPLOAD durante la creazione delle risorse GPU a cui si accede di frequente in un heap DEFAULT senza accesso alla CPU. Questa tecnica supporta in modo efficiente GPU discrete e le relative grandi quantità di memoria inaccessibile alla CPU, senza compromettere in genere le architetture UMA.

Si notino le due costanti seguenti:

``` syntax
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [**FOOTPRINT DELLE SOTTORISORSE D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [**FOOTPRINT DELLE SOTTORISORSE \_ \_ POSIZIONATE D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [**PERCORSO COPIA TRAMA D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [**TIPO DI COPIA TRAMA D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**ID3D12GraphicsCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**ID3D12CommandQueue::UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a>Mapping e annullamento del mapping

[**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) e [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) possono essere chiamati da più thread in modo sicuro. La prima chiamata a **Map** alloca un intervallo di indirizzi virtuali della CPU per la risorsa. L'ultima chiamata **a Unmap** dealloca l'intervallo di indirizzi virtuali della CPU. L'indirizzo virtuale della CPU viene in genere restituito all'applicazione.

Ogni volta che i dati vengono passati tra CPU e GPU tramite risorse negli heap di readback, è necessario usare [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) e [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) per supportare tutti i sistemi in cui è supportato D3D12. Mantenendo gli intervalli il più possibile ristretti, si ottimizza l'efficienza nei sistemi che richiedono intervalli (vedere [**D3D12 \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).

Le prestazioni degli strumenti di debug traggono vantaggio [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)non solo dall'uso accurato degli intervalli in tutte le chiamate Map  /  [**Unmap,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) ma anche dalle applicazioni che annullano il mapping delle risorse quando non verranno più apportate modifiche alla CPU.

Il metodo D3D11 dell'uso [**di Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (con il parametro DISCARD impostato) per rinominare le risorse non è supportato in D3D12. Le applicazioni devono implementare la ridenominazione delle risorse. Tutte **le chiamate** map sono implicitamente NO OVERWRITE e \_ multi-thread. È responsabilità dell'applicazione assicurarsi che tutte le operazioni GPU pertinenti contenute negli elenchi di comandi siano completate prima dell'accesso ai dati con la CPU. Le chiamate D3D12 a **Map** non scaricano in modo implicito i buffer dei comandi né bloccano l'attesa del completamento del lavoro della GPU. Di conseguenza, **map** e [**unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) possono anche essere ottimizzati in alcuni scenari.

## <a name="buffer-alignment"></a>Allineamento del buffer

Restrizioni di allineamento del buffer:

-   La copia lineare di sottorisorse deve essere allineata a 512 byte (con l'altezza della riga allineata ai byte D3D12 \_ TEXTURE \_ DATA PITCH \_ \_ ALIGNMENT).
-   Le operazioni di lettura dei dati costanti devono essere un multiplo di 256 byte dall'inizio dell'heap, ad esempio solo da indirizzi allineati a 256 byte.
-   Le operazioni di lettura dei dati dell'indice devono essere un multiplo delle dimensioni del tipo di dati dell'indice, ad esempio solo da indirizzi allineati naturalmente per i dati.
-   [**I dati ID3D12GraphicsCommandList::ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) devono essere da offset multipli di 4 (ad esempio solo da indirizzi allineati con DWORD).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sottoallocazione all'interno dei buffer](large-buffers.md)
</dt> </dl>

 

 
