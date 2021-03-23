---
title: Sottorisorse (grafica Direct3D 12)
description: Viene descritto come una risorsa è divisa in sottorisorse e viene illustrato come fare riferimento a una singola, più o più sezioni di sottorisorse.
ms.assetid: C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8fa8ea0d48fea7ee8e192d9dcf1fe5e3d22423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548840"
---
# <a name="subresources-direct3d-12-graphics"></a>Sottorisorse (grafica Direct3D 12)

Viene descritto come una risorsa è divisa in sottorisorse e viene illustrato come fare riferimento a una singola, più o più sezioni di sottorisorse.

-   [Sottorisorse di esempio](#example-subresources)
    -   [Indicizzazione delle risorse](#subresource-indexing)
    -   [Sezione MIP](#mip-slice)
    -   [Sezione matrice](#array-slice)
    -   [Sezione piano](#plane-slice)
    -   [Più sottorisorse](#multiple-subresources)
-   [API subresource](#subresource-apis)
-   [Argomenti correlati](#related-topics)

## <a name="example-subresources"></a>Sottorisorse di esempio

Se una risorsa contiene un buffer, contiene semplicemente una sottorisorsa con un indice pari a 0. Se la risorsa contiene una trama (o una matrice di trame), fare riferimento alle sottorisorse è più complessa.

Alcune API accedono a un'intera risorsa, ad esempio il metodo [**ID3D12GraphicsCommandList:: CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) , mentre altre accedono a una parte di una risorsa, ad esempio il metodo [**ID3D12Resource:: ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) . I metodi che accedono a una parte di una risorsa utilizzano in genere una descrizione della vista, ad esempio la struttura [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) , per specificare le sottorisorse a cui accedere. Per un elenco completo, vedere la sezione [API della sottorisorsa](#subresource-apis) .

### <a name="subresource-indexing"></a>Indicizzazione delle risorse

Per indicizzare una determinata sottorisorsa, i livelli MIP vengono indicizzati per primi quando ogni voce della matrice viene indicizzata.

![indicizzazione delle risorse](images/subresource-index.png)

### <a name="mip-slice"></a>Sezione MIP

Una sezione MIP include un livello mipmap per ogni trama in una matrice, come illustrato nella figura seguente.

![sezioni della sottorisorsa MIP](images/subresource-mip-slice.png)

### <a name="array-slice"></a>Sezione matrice

Data una matrice di trame, ogni trama con mipmap, una sezione della matrice include una trama e tutti i livelli MIP, come illustrato nella figura seguente.

![sezioni della matrice della sottorisorsa](images/subresource-array-slices.png)

### <a name="plane-slice"></a>Sezione piano

In genere i formati planari non vengono usati per archiviare i dati di RGBA, ma nei casi in cui sono (probabilmente 24bpp dati RGB), un piano può rappresentare l'immagine rossa, una verde e un'immagine blu. Un piano, tuttavia, non è necessariamente un colore, due o più colori possono essere combinati in un piano. Per i dati YCbCr e Depth-Stencil sottocampionati viene usato più di solito dati planari. Depth-Stencil è l'unico formato che supporta completamente mipmap, matrici e più piani (spesso il piano 0 per la profondità e il piano 1 per stencil).

L'indicizzazione delle sottorisorse per una matrice di due immagini Depth-Stencil, ognuna con tre livelli MIP, è illustrata di seguito.

![indicizzazione depth stencil](images/depth-stencil-indexing.png)

YCbCr sottocampionato supporta matrici con piani, ma non supporta mipmap. Le immagini YCbCr hanno due piani, uno per la luminanza (Y) a cui l'occhio umano è più sensibile e uno per cromatura (CB e CR, con interfoliazione) a cui l'occhio umano è meno sensibile. Questo formato consente la compressione dei valori cromatura per comprimere un'immagine senza influire sulla luminanza ed è un formato di compressione video comune per tale motivo, sebbene venga usato per comprimere le immagini ancora. L'immagine seguente mostra il formato NV12, annotando che cromatura è stato compresso in un trimestre della risoluzione della luminanza, vale a dire che la larghezza di ogni piano è identica e il piano cromatura è metà dell'altezza del piano di luminanza. I piani verrebbero indicizzati come sottorisorse in modo identico al Depth-Stencil esempio precedente.

![formato NV12](images/ycbcr.png)

In Direct3D 11 sono presenti formati planari, ma non è stato possibile risolvere i singoli piani singolarmente, ad esempio per le operazioni di copia o mapping. Questa operazione è stata modificata in Direct3D 12 in modo che ogni piano abbia ricevuto il proprio ID di sottorisorsa. Confrontare i due metodi seguenti per calcolare l'ID della sottorisorsa.

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

La maggior parte dell'hardware presuppone che la memoria per il piano N venga sempre allocata immediatamente dopo il piano N-1.

Un'alternativa all'uso delle sottorisorse è che un'app potrebbe allocare una risorsa completamente separata per ogni piano. In questo caso, l'applicazione riconosce che i dati sono planari e usa più risorse per rappresentarlo.

### <a name="multiple-subresources"></a>Più sottorisorse

Una visualizzazione risorse shader può selezionare qualsiasi area rettangolare di sottorisorse, usando una delle sezioni descritte in precedenza e l'uso oculato dei campi nelle strutture di visualizzazione (ad esempio, [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), come illustrato nell'immagine.

![selezione di più sottorisorse](images/subresource-multiple.png)

Una visualizzazione di destinazione di rendering può utilizzare una sola sezione subresource o MIP e non può includere sottorisorse da più di una sezione MIP. Ovvero ogni trama in una visualizzazione di destinazione di rendering deve avere le stesse dimensioni. Una visualizzazione risorse shader può selezionare qualsiasi area rettangolare di sottorisorse, come illustrato nell'immagine.

## <a name="subresource-apis"></a>API subresource

Le API seguenti fanno riferimento a e funzionano con le sottorisorse:

Enumerazioni:

-   [**\_Tipo di \_ Copia \_ trama D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)

Le strutture seguenti contengono indici *PlaneSlice* , che contengono la maggior parte degli indici *MipSlice* .

-   [**D3D12 \_ TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [**D3D12 \_ TEX2D \_ array \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [**D3D12 \_ TEX2D \_ array \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

Le strutture seguenti contengono indici *ArraySlice* , che contengono la maggior parte degli indici *MipSlice* .

-   [**Vista \_ \_ origine dati matrice TEX1D D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [**Vista \_ \_ origine dati matrice TEX2D D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [**Vista \_ \_ origine dati matrice TEX2DMS D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)
-   [**D3D12 \_ TEX1D \_ array \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [**D3D12 \_ TEX2D \_ array \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2DMS \_ array \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [**D3D12 \_ TEX1D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2DMS \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [**D3D12 \_ TEX1D \_ array \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [**D3D12 \_ TEX2D \_ array \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

Le strutture seguenti contengono indici *MipSlice* , ma non *ArraySlice* né *PlaneSlice* .

-   [**Vista \_ origine dati TEX1D D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [**Vista \_ origine dati TEX2D D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [**D3D12 \_ TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [**D3D12 \_ TEX3D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)
-   [**D3D12 \_ TEX1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [**D3D12 \_ TEX3D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

Anche le strutture seguenti fanno riferimento a sottorisorse:

-   [**D3D12 \_ SCARTO \_ Region**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : struttura utilizzata per la rimozione di una risorsa.
-   [**D3D12 \_ \_ \_ Footprint delle sottorisorse inserito**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) : aggiunge un offset in una risorsa al footprint di base.
-   [**D3D12 \_ \_ \_ Barriera di transizione delle risorse**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : descrive la transizione delle sottorisorse tra diversi utilizzi (risorsa shader, destinazione di rendering e così via).
-   [**D3D12 \_ \_Dati delle sottorisorse**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) : i dati delle sottorisorse includono i dati stessi e il passo delle righe e delle sezioni.
-   [**D3D12 \_ \_Footprint delle sottorisorse**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) : un'impronta include il formato, la larghezza, l'altezza, la profondità e il pitch di riga della sottorisorsa.
-   [**D3D12 \_ Subresource \_ info**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : contiene l'offset, il pitch di riga e il passo di profondità della sottorisorsa.
-   [**D3D12 \_ \_Affiancamento delle risorse**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) : descrive un volume della sottorisorsa affiancata (fare riferimento a [risorse affiancate dal volume](volume-tiled-resources.md)).
-   [**D3D12 \_ TEXTURE \_ copy \_ location**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : descrive una parte di una trama per la copia.
-   [**D3D12 \_ \_ \_ Coordinata della risorsa affiancata**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : descrive le coordinate di una risorsa affiancata.

Metodi:

-   [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : ottiene informazioni su una risorsa, per consentire la copia.
-   [**ID3D12Device:: GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : ottiene informazioni sul modo in cui una risorsa affiancata viene suddivisa in riquadri.
-   [**ID3D12GraphicsCommandList:: ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : copia una sottorisorsa multicampionata in una sottorisorsa non multicampionata.
-   [**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : restituisce un puntatore ai dati specificati nella risorsa e nega l'accesso alla GPU alla sottorisorsa.
-   [**ID3D12Resource:: ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : copia i dati da una sottorisorsa o da un'area rettangolare di una sottorisorsa.
-   [**ID3D12Resource:: annullare**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) : Annulla il mapping dell'intervallo di memoria specificato e invalida il puntatore alla risorsa. Ripristina l'accesso GPU alla sottorisorsa.
-   [**ID3D12Resource:: WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : copia i dati in una sottorisorsa o in un'area rettangolare di una sottorisorsa.

Le trame devono trovarsi nello stato [**comune di \_ stato della risorsa \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) per l'accesso alla CPU tramite [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) e [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) come validi, ma non i buffer. L'accesso alla CPU a una risorsa viene in genere eseguito tramite [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [**annullare**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Associazione di risorse](resource-binding.md)
</dt> </dl>

 

 




