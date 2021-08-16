---
title: Sottorisorse (grafica Direct3D 12)
description: Viene descritto come una risorsa viene divisa in sottorisorse e come fare riferimento a una singola, più o sezione di sottorisorse.
ms.assetid: C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2fc4478e71bbafb8a21897f838ee8091592024a4e3c761280911e395f8ae491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911972"
---
# <a name="subresources-direct3d-12-graphics"></a>Sottorisorse (grafica Direct3D 12)

Viene descritto come una risorsa viene divisa in sottorisorse e come fare riferimento a una singola, più o sezione di sottorisorse.

-   [Sottorisorse di esempio](#example-subresources)
    -   [Indicizzazione di sottorisorse](#subresource-indexing)
    -   [Sezione Mip](#mip-slice)
    -   [Sezione matrice](#array-slice)
    -   [Sezione piano](#plane-slice)
    -   [Più sottorisorse](#multiple-subresources)
-   [API di sottorisorse](#subresource-apis)
-   [Argomenti correlati](#related-topics)

## <a name="example-subresources"></a>Sottorisorse di esempio

Se una risorsa contiene un buffer, contiene semplicemente una sottorisorsa con indice 0. Se la risorsa contiene una trama (o una matrice di trame), fare riferimento alle sottorisorse è più complesso.

Alcune API accedono a un'intera risorsa ,ad esempio il metodo [**ID3D12GraphicsCommandList::CopyResource,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) altre accedono a una parte di una risorsa, ad esempio il metodo [**ID3D12Resource::ReadFromSubresource.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) I metodi che accedono a una parte di una risorsa usano in genere una descrizione della visualizzazione ,ad esempio la struttura [**SRV D3D12 \_ TEX2D \_ \_ ARRAY,**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) per specificare le sottorisorse a cui accedere. Per un elenco completo, vedere [la sezione API subresource.](#subresource-apis)

### <a name="subresource-indexing"></a>Indicizzazione di sottorisorse

Per indicizzare una determinata sottorisorsa, i livelli mip vengono indicizzati per primi quando viene indicizzata ogni voce di matrice.

![indicizzazione di sottorisorse](images/subresource-index.png)

### <a name="mip-slice"></a>Sezione Mip

Una sezione mip include un livello mipmap per ogni trama in una matrice, come illustrato nell'immagine seguente.

![sezioni mip di sottorisorse](images/subresource-mip-slice.png)

### <a name="array-slice"></a>Sezione matrice

Data una matrice di trame, ogni trama con mipmap, una sezione di matrice include una trama e tutti i relativi livelli mip, come illustrato nell'immagine seguente.

![sezioni di matrici di sottorisorse](images/subresource-array-slices.png)

### <a name="plane-slice"></a>Sezione piano

In genere i formati planari non vengono usati per archiviare i dati RGBA, ma nei casi in cui si trovano (ad esempio dati RGB 24bpp), un piano può rappresentare l'immagine rossa, uno verde e uno l'immagine blu. Un piano, tuttavia, non è necessariamente un colore, due o più colori possono essere combinati in un unico piano. I dati planari vengono in genere usati per i dati YCbCr sotto-campionati Depth-Stencil dati. Depth-Stencil è l'unico formato che supporta completamente mipmap, matrici e più piani (spesso piano 0 per Profondità e piano 1 per Stencil).

L'indicizzazione della sottorisorsa per una matrice di Depth-Stencil immagini, ognuna con tre livelli mip, è illustrata di seguito.

![depth stencil indicizzazione](images/depth-stencil-indexing.png)

Il sotto-campionamento YCbCr supporta le matrici e dispone di piani, ma non supporta mipmap. Le immagini YCbCr hanno due piani, uno per la luminazione (Y) a cui l'occhio umano è più sensibile e uno per la chrominance (sia Cb che Cr, interleaved) a cui l'occhio umano è meno sensibile. Questo formato consente la compressione dei valori di crominanza per comprimere un'immagine senza influire sulla luminance ed è un formato di compressione video comune per questo motivo, anche se viene usato per comprimere le immagini fisse. L'immagine seguente mostra il formato NV12, notando che la chrominance è stata compressa a un quarto della risoluzione della luminance, ovvero la larghezza di ogni piano è identica e il piano di crominanza è la metà dell'altezza del piano di luminance. I piani verrebbero indicizzati come sottorisorse in modo identico all'esempio Depth-Stencil precedente.

![formato nv12](images/ycbcr.png)

I formati planari esistevano in Direct3D 11, ma i singoli piani non potevano essere indirizzati singolarmente, ad esempio per le operazioni di copia o mapping. Questa modifica è stata modificata in Direct3D 12 in modo che ogni piano riceve il proprio ID sottorisorsa. Confrontare i due metodi seguenti per calcolare l'ID sottorisorsa.

Direct3D 11

``` syntax
inline UINT D3D11CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT MipLevels )
{
    return MipSlice + (ArraySlice * MipLevels); 
}
```

Direct3D 12

``` syntax
inline UINT D3D12CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT PlaneSlice, UINT MipLevels, UINT ArraySize )
{ 
    return MipSlice + (ArraySlice * MipLevels) + (PlaneSlice * MipLevels * ArraySize); 
}
```

La maggior parte dell'hardware presuppone che la memoria per il piano N sia sempre allocata immediatamente dopo il piano N-1.

Un'alternativa all'uso delle sottorisorse è che un'app potrebbe allocare una risorsa completamente separata per ogni piano. In questo caso, l'applicazione comprende che i dati sono planari e usa più risorse per rappresentarlo.

### <a name="multiple-subresources"></a>Più sottorisorse

Una visualizzazione shader-risorsa può selezionare qualsiasi area rettangolare di sottorisorse, usando una delle sezioni descritte in precedenza e un uso judicious dei campi nelle strutture di visualizzazione (ad esempio [**D3D12 \_ TEX2D \_ ARRAY \_ SRV),**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)come illustrato nell'immagine.

![selezione di più sottorisorse](images/subresource-multiple.png)

Una visualizzazione di destinazione di rendering può usare solo una singola sottorisorsa o sezione mip e non può includere sottorisorse da più di una sezione mip. Ciò significa che ogni trama in una visualizzazione di destinazione di rendering deve avere le stesse dimensioni. Una visualizzazione shader-risorsa può selezionare qualsiasi area rettangolare di sottorisorse, come illustrato nell'immagine.

## <a name="subresource-apis"></a>API di sottorisorse

Le API seguenti fanno riferimento e funzionano con le sottorisorse:

Enumerazioni:

-   [**TIPO DI COPIA TRAMA D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)

Le strutture seguenti contengono *indici PlaneSlice,* la maggior parte degli indici *MipSlice.*

-   [**D3D12 \_ TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [**UAV MATRICE D3D12 \_ TEX2D \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

Le strutture seguenti contengono *indici ArraySlice,* la maggior parte degli indici *MipSlice.*

-   [**D3D12 \_ TEX1D \_ ARRAY \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [**D3D12 \_ TEX2DMS \_ ARRAY \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)
-   [**D3D12 \_ TEX1D \_ ARRAY \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**MATRICE D3D12 \_ TEX2DMS \_ \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [**D3D12 \_ TEX1D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2DMS \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [**UAV MATRICE D3D12 \_ TEX1D \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [**UAV MATRICE D3D12 \_ TEX2D \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

Le strutture seguenti contengono *indici MipSlice,* ma non *indici ArraySlice* né *PlaneSlice.*

-   [**D3D12 \_ TEX1D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [**D3D12 \_ TEX2D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [**D3D12 \_ TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [**D3D12 \_ TEX3D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)
-   [**D3D12 \_ TEX1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [**D3D12 \_ TEX3D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

Anche le strutture seguenti fanno riferimento a sottorisorse:

-   [**D3D12 \_ DISCARD \_ REGION:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) struttura usata per preparare l'eliminazione di una risorsa.
-   [**D3D12 \_ PLACED \_ SUBRESOURCE \_ FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) : aggiunge un offset in una risorsa al footprint di base.
-   [**D3D12 \_ RESOURCE \_ TRANSITION \_ BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : descrive la transizione di sottorisorse tra utilizzi diversi (risorsa shader, destinazione di rendering e così via).
-   [**D3D12 \_ SUBRESOURCE \_ DATA:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) i dati delle sottorisorse includono i dati stessi e il passo di riga e sezione.
-   [**D3D12 \_ FOOTPRINT \_ SUBRESOURCE:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) un footprint include il formato, la larghezza, l'altezza, la profondità e il passo di riga della sottorisorsa.
-   [**D3D12 \_ SUBRESOURCE \_ INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : contiene l'offset, l'altezza della riga e l'altezza della sottorisorsa.
-   [**D3D12 \_ SUBRESOURCE \_ TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) : descrive un volume di sottorisorse affiancate (vedere [Risorse affiancate del volume).](volume-tiled-resources.md)
-   [**D3D12 \_ TEXTURE \_ COPY \_ LOCATION:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) descrive una parte di una trama ai fini della copia.
-   [**D3D12 \_ TILED \_ RESOURCE \_ COORDINATE :**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) descrive le coordinate di una risorsa affiancata.

Metodi:

-   [**ID3D12Device::GetCopyablePrints:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) ottiene informazioni su una risorsa, per consentire l'applicazione di una copia.
-   [**ID3D12Device::GetResourceTiling:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) ottiene informazioni sul modo in cui una risorsa affiancata viene suddivisa in riquadri.
-   [**ID3D12GraphicsCommandList::ResolveSubresource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) copia una sottorisorsa multieseguita in una sottorisorsa non multieseguita.
-   [**ID3D12Resource::Map:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) restituisce un puntatore ai dati specificati nella risorsa e nega alla GPU l'accesso alla sottorisorsa.
-   [**ID3D12Resource::ReadFromSubresource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) copia i dati da una sottorisorsa o da un'area rettangolare di una sottorisorsa.
-   [**ID3D12Resource::Unmap:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) annulla il mapping dell'intervallo di memoria specificato e invalida il puntatore alla risorsa. Ripristina l'accesso GPU alla sottorisorsa.
-   [**ID3D12Resource::WriteToSubresource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) copia i dati in una sottorisorsa o in un'area rettangolare di una sottorisorsa.

Le trame devono essere nello stato [**D3D12 \_ RESOURCE \_ STATE \_ COMMON**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) perché l'accesso alla CPU tramite [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) e [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) sia valido, ma i buffer non lo fanno. L'accesso della CPU a una risorsa viene in genere eseguito [**tramite Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Associazione di risorse](resource-binding.md)
</dt> </dl>

 

 




