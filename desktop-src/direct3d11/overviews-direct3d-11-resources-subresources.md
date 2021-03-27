---
title: Sottorisorse (grafica Direct3D 11)
description: Questo argomento descrive le sottorisorse di trama o parti di una risorsa.
ms.assetid: 57444cb5-6c8b-4dac-8d6b-ca2b45eafac9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a432dbfbcbf08c4359ea436a3e8fa025c801d12
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047664"
---
# <a name="subresources-direct3d-11-graphics"></a>Sottorisorse (grafica Direct3D 11)

Questo argomento descrive le sottorisorse di trama o parti di una risorsa.

Direct3D può fare riferimento a un'intera risorsa oppure può fare riferimento a subset di una risorsa. Il termine subresource fa riferimento a un subset di una risorsa.

Un buffer è definito come una singola risorsa. Le trame sono leggermente più complesse perché esistono diversi tipi di trama (1D, 2D e così via), alcuni dei quali supportano i livelli mipmap e/o le matrici di trama. A partire dal caso più semplice, una trama 1D viene definita come una singola risorsa, come illustrato nella figura seguente.

![illustrazione di una trama 1D](images/d3d10-1d-texture.png)

Ciò significa che la matrice di Texel che compongono una trama 1D è contenuta in una singola risorsa.

Se si espande una trama 1D con tre livelli di mipmap, è possibile visualizzarla come illustrato nella figura seguente.

![illustrazione di una trama 1D con tre livelli di mipmap](images/d3d10-resource-texture1d.png)

Si può pensare a questa come una singola trama costituita da tre sottorisorse. Una sottorisorsa può essere indicizzata usando il livello di dettaglio (LOD) per una singola trama. Quando si usa una matrice di trame, l'accesso a una determinata sottorisorsa richiede sia il valore LOD che la trama particolare. In alternativa, l'API combina queste due parti di informazioni in un singolo indice di sottorisorsa in base zero, come illustrato nella figura seguente.

![illustrazione di un indice di sottorisorsa in base zero](images/d3d10-resource-texture1darray-sub-indexing.png)

## <a name="selecting-subresources"></a>Selezione delle sottorisorse

Alcune API accedono a un'intera risorsa, ad esempio il metodo [**sul ID3D11DeviceContext:: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) , altre accedono a una parte di una risorsa, ad esempio il metodo [**sul ID3D11DeviceContext:: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) o il metodo [**sul ID3D11DeviceContext:: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) . I metodi che accedono a una parte di una risorsa utilizzano in genere una descrizione della vista, ad esempio la struttura [**\_ \_ \_ DSV della matrice TEX2D d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) , per specificare le sottorisorse a cui accedere.

Le illustrazioni nelle sezioni seguenti illustrano i termini usati da una descrizione della vista durante l'accesso a una matrice di trame.

### <a name="array-slice"></a>Sezione matrice

Data una matrice di trame, ogni trama con mipmap, una *sezione di matrice* , rappresentata dal rettangolo bianco, include una trama e tutte le relative sottorisorse, come illustrato nella figura seguente.

![illustrazione di una sezione di matrice](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a>Sezione MIP

Una *sezione MIP* , rappresentata dal rettangolo bianco, include un livello mipmap per ogni trama in una matrice, come illustrato nella figura seguente.

![illustrazione di una sezione MIP](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a>Selezione di una singola sottorisorsa

È possibile usare questi due tipi di sezioni per scegliere una singola sottorisorsa, come illustrato nella figura seguente.

![illustrazione della scelta di una sottorisorsa tramite una sezione della matrice e una sezione MIP](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a>Selezione di più sottorisorse

In alternativa, è possibile usare questi due tipi di sezioni con il numero di livelli di mipmap e/o il numero di trame per scegliere più sottorisorse, come illustrato nella figura seguente.

![illustrazione della scelta di più sottorisorse](images/d3d10-resource-subresources-2.png)

> [!Note]  
> Una [**visualizzazione di destinazione di rendering**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) può utilizzare una sola sezione subresource o MIP e non può includere sottorisorse da più di una sezione MIP. Ovvero ogni trama in una visualizzazione di destinazione di rendering deve avere le stesse dimensioni. Una [**visualizzazione risorse shader**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) può selezionare qualsiasi area rettangolare di sottorisorse, come illustrato nella figura.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 




