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
# <a name="subresources-direct3d-11-graphics"></a><span data-ttu-id="fc6eb-103">Sottorisorse (grafica Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="fc6eb-103">Subresources (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="fc6eb-104">Questo argomento descrive le sottorisorse di trama o parti di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-104">This topic describes texture subresources, or portions of a resource.</span></span>

<span data-ttu-id="fc6eb-105">Direct3D può fare riferimento a un'intera risorsa oppure può fare riferimento a subset di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-105">Direct3D can reference an entire resource or it can reference subsets of a resource.</span></span> <span data-ttu-id="fc6eb-106">Il termine subresource fa riferimento a un subset di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-106">The term subresource refers to a subset of a resource.</span></span>

<span data-ttu-id="fc6eb-107">Un buffer è definito come una singola risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-107">A buffer is defined as a single subresource.</span></span> <span data-ttu-id="fc6eb-108">Le trame sono leggermente più complesse perché esistono diversi tipi di trama (1D, 2D e così via), alcuni dei quali supportano i livelli mipmap e/o le matrici di trama.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-108">Textures are a little more complicated because there are several different texture types (1D, 2D, etc.) some of which support mipmap levels and/or texture arrays.</span></span> <span data-ttu-id="fc6eb-109">A partire dal caso più semplice, una trama 1D viene definita come una singola risorsa, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-109">Beginning with the simplest case, a 1D texture is defined as a single subresource, as shown in the following illustration.</span></span>

![illustrazione di una trama 1D](images/d3d10-1d-texture.png)

<span data-ttu-id="fc6eb-111">Ciò significa che la matrice di Texel che compongono una trama 1D è contenuta in una singola risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-111">This means that the array of texels that make up a 1D texture are contained in a single subresource.</span></span>

<span data-ttu-id="fc6eb-112">Se si espande una trama 1D con tre livelli di mipmap, è possibile visualizzarla come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-112">If you expand a 1D texture with three mipmap levels, it can be visualized like the following illustration.</span></span>

![illustrazione di una trama 1D con tre livelli di mipmap](images/d3d10-resource-texture1d.png)

<span data-ttu-id="fc6eb-114">Si può pensare a questa come una singola trama costituita da tre sottorisorse.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-114">Think of this as a single texture that is made up of three subresources.</span></span> <span data-ttu-id="fc6eb-115">Una sottorisorsa può essere indicizzata usando il livello di dettaglio (LOD) per una singola trama.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-115">A subresource can be indexed using the level-of-detail (LOD) for a single texture.</span></span> <span data-ttu-id="fc6eb-116">Quando si usa una matrice di trame, l'accesso a una determinata sottorisorsa richiede sia il valore LOD che la trama particolare.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-116">When using an array of textures, accessing a particular subresource requires both the LOD and the particular texture.</span></span> <span data-ttu-id="fc6eb-117">In alternativa, l'API combina queste due parti di informazioni in un singolo indice di sottorisorsa in base zero, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-117">Alternately, the API combines these two pieces of information into a single zero-based subresource index, as shown in the following illustration.</span></span>

![illustrazione di un indice di sottorisorsa in base zero](images/d3d10-resource-texture1darray-sub-indexing.png)

## <a name="selecting-subresources"></a><span data-ttu-id="fc6eb-119">Selezione delle sottorisorse</span><span class="sxs-lookup"><span data-stu-id="fc6eb-119">Selecting Subresources</span></span>

<span data-ttu-id="fc6eb-120">Alcune API accedono a un'intera risorsa, ad esempio il metodo [**sul ID3D11DeviceContext:: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) , altre accedono a una parte di una risorsa, ad esempio il metodo [**sul ID3D11DeviceContext:: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) o il metodo [**sul ID3D11DeviceContext:: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) .</span><span class="sxs-lookup"><span data-stu-id="fc6eb-120">Some APIs access an entire resource (for example the [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) method), others access a portion of a resource (for example the [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) method or the [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) method).</span></span> <span data-ttu-id="fc6eb-121">I metodi che accedono a una parte di una risorsa utilizzano in genere una descrizione della vista, ad esempio la struttura [**\_ \_ \_ DSV della matrice TEX2D d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) , per specificare le sottorisorse a cui accedere.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-121">The methods that access a portion of a resource generally use a view description (such as the [**D3D11\_TEX2D\_ARRAY\_DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) structure) to specify the subresources to access.</span></span>

<span data-ttu-id="fc6eb-122">Le illustrazioni nelle sezioni seguenti illustrano i termini usati da una descrizione della vista durante l'accesso a una matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-122">The illustrations in the following sections show the terms used by a view description when accessing an array of textures.</span></span>

### <a name="array-slice"></a><span data-ttu-id="fc6eb-123">Sezione matrice</span><span class="sxs-lookup"><span data-stu-id="fc6eb-123">Array Slice</span></span>

<span data-ttu-id="fc6eb-124">Data una matrice di trame, ogni trama con mipmap, una *sezione di matrice* , rappresentata dal rettangolo bianco, include una trama e tutte le relative sottorisorse, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-124">Given an array of textures, each texture with mipmaps, an *array slice* (represented by the white rectangle) includes one texture and all of its subresources, as shown in the following illustration.</span></span>

![illustrazione di una sezione di matrice](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a><span data-ttu-id="fc6eb-126">Sezione MIP</span><span class="sxs-lookup"><span data-stu-id="fc6eb-126">Mip Slice</span></span>

<span data-ttu-id="fc6eb-127">Una *sezione MIP* , rappresentata dal rettangolo bianco, include un livello mipmap per ogni trama in una matrice, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-127">A *mip slice* (represented by the white rectangle) includes one mipmap level for every texture in an array, as shown in the following illustration.</span></span>

![illustrazione di una sezione MIP](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a><span data-ttu-id="fc6eb-129">Selezione di una singola sottorisorsa</span><span class="sxs-lookup"><span data-stu-id="fc6eb-129">Selecting a Single Subresource</span></span>

<span data-ttu-id="fc6eb-130">È possibile usare questi due tipi di sezioni per scegliere una singola sottorisorsa, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-130">You can use these two types of slices to choose a single subresource, as shown in the following illustration.</span></span>

![illustrazione della scelta di una sottorisorsa tramite una sezione della matrice e una sezione MIP](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a><span data-ttu-id="fc6eb-132">Selezione di più sottorisorse</span><span class="sxs-lookup"><span data-stu-id="fc6eb-132">Selecting Multiple Subresources</span></span>

<span data-ttu-id="fc6eb-133">In alternativa, è possibile usare questi due tipi di sezioni con il numero di livelli di mipmap e/o il numero di trame per scegliere più sottorisorse, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-133">Or you can use these two types of slices with the number of mipmap levels and/or number of textures, to choose multiple subresources, as shown in the following illustration.</span></span>

![illustrazione della scelta di più sottorisorse](images/d3d10-resource-subresources-2.png)

> [!Note]  
> <span data-ttu-id="fc6eb-135">Una [**visualizzazione di destinazione di rendering**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) può utilizzare una sola sezione subresource o MIP e non può includere sottorisorse da più di una sezione MIP.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-135">A [**render-target view**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) can only use a single subresource or mip slice and cannot include subresources from more than one mip slice.</span></span> <span data-ttu-id="fc6eb-136">Ovvero ogni trama in una visualizzazione di destinazione di rendering deve avere le stesse dimensioni.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-136">That is, every texture in a render-target view must be the same size.</span></span> <span data-ttu-id="fc6eb-137">Una [**visualizzazione risorse shader**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) può selezionare qualsiasi area rettangolare di sottorisorse, come illustrato nella figura.</span><span class="sxs-lookup"><span data-stu-id="fc6eb-137">A [**shader-resource view**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) can select any rectangular region of subresources, as shown in the figure.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fc6eb-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fc6eb-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc6eb-139">Risorse</span><span class="sxs-lookup"><span data-stu-id="fc6eb-139">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 




