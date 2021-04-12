---
description: L'interfaccia ID3DXTextureGutterHelper viene utilizzata per creare e gestire aree di gronda in una trama. Le aree di rilegatura separano le trame e consentono l'interpolazione bilineare per evitare il rendering di artefatti a limiti di trama
ms.assetid: 097e27bf-a1a6-4e7e-bdad-33015b50f91f
title: Interfaccia ID3DXTextureGutterHelper (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ece03e14da490bd6d6f5aef69f9457939bc8bab7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355614"
---
# <a name="id3dxtexturegutterhelper-interface"></a><span data-ttu-id="b9edc-104">Interfaccia ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="b9edc-104">ID3DXTextureGutterHelper interface</span></span>

<span data-ttu-id="b9edc-105">L'interfaccia ID3DXTextureGutterHelper viene utilizzata per creare e gestire aree di gronda in una trama.</span><span class="sxs-lookup"><span data-stu-id="b9edc-105">The ID3DXTextureGutterHelper interface is used to build and manage gutter regions in a texture.</span></span> <span data-ttu-id="b9edc-106">Le aree di rilegatura separano le trame e consentono l'interpolazione bilineare per evitare il rendering di artefatti a limiti di trama</span><span class="sxs-lookup"><span data-stu-id="b9edc-106">Gutter regions separate textures and allow for bilinear interpolation to avoid rendering artifacts at texture boundaries.</span></span>

<span data-ttu-id="b9edc-107">Il Get... i metodi forniscono l'accesso alle strutture di dati utilizzate dall'oggetto Apply... Metodi.</span><span class="sxs-lookup"><span data-stu-id="b9edc-107">The Get... methods provide access to the data structures used by the Apply... methods.</span></span>

## <a name="members"></a><span data-ttu-id="b9edc-108">Membri</span><span class="sxs-lookup"><span data-stu-id="b9edc-108">Members</span></span>

<span data-ttu-id="b9edc-109">L'interfaccia **ID3DXTextureGutterHelper** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b9edc-109">The **ID3DXTextureGutterHelper** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b9edc-110">**ID3DXTextureGutterHelper** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b9edc-110">**ID3DXTextureGutterHelper** also has these types of members:</span></span>

-   [<span data-ttu-id="b9edc-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="b9edc-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b9edc-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="b9edc-112">Methods</span></span>

<span data-ttu-id="b9edc-113">L'interfaccia **ID3DXTextureGutterHelper** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b9edc-113">The **ID3DXTextureGutterHelper** interface has these methods.</span></span>



| <span data-ttu-id="b9edc-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="b9edc-114">Method</span></span>                                                                   | <span data-ttu-id="b9edc-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9edc-115">Description</span></span>                                                                                            |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9edc-116">**ApplyGuttersFloat**</span><span class="sxs-lookup"><span data-stu-id="b9edc-116">**ApplyGuttersFloat**</span></span>](id3dxtexturegutterhelper--applyguttersfloat.md) | <span data-ttu-id="b9edc-117">Applica le grondature a un buffer di trama FLOAT.</span><span class="sxs-lookup"><span data-stu-id="b9edc-117">Applies gutters to a FLOAT texture buffer.</span></span><br/>                                                  |
| [<span data-ttu-id="b9edc-118">**ApplyGuttersPRT**</span><span class="sxs-lookup"><span data-stu-id="b9edc-118">**ApplyGuttersPRT**</span></span>](id3dxtexturegutterhelper--applyguttersprt.md)     | <span data-ttu-id="b9edc-119">Applica le grondanze a un oggetto buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b9edc-119">Applies gutters to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer object.</span></span><br/>               |
| [<span data-ttu-id="b9edc-120">**ApplyGuttersTex**</span><span class="sxs-lookup"><span data-stu-id="b9edc-120">**ApplyGuttersTex**</span></span>](id3dxtexturegutterhelper--applygutterstex.md)     | <span data-ttu-id="b9edc-121">Applica le grondanze a un oggetto trama [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="b9edc-121">Applies gutters to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object.</span></span><br/>        |
| [<span data-ttu-id="b9edc-122">**GetBaryMap**</span><span class="sxs-lookup"><span data-stu-id="b9edc-122">**GetBaryMap**</span></span>](id3dxtexturegutterhelper--getbarymap.md)               | <span data-ttu-id="b9edc-123">Recupera le coordinate baricentrica Texel.</span><span class="sxs-lookup"><span data-stu-id="b9edc-123">Retrieves texel barycentric coordinates.</span></span><br/>                                                    |
| [<span data-ttu-id="b9edc-124">**GetFaceMap**</span><span class="sxs-lookup"><span data-stu-id="b9edc-124">**GetFaceMap**</span></span>](id3dxtexturegutterhelper--getfacemap.md)               | <span data-ttu-id="b9edc-125">Recupera l'indice della faccia mesh a cui appartiene ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="b9edc-125">Retrieves the index of the mesh face to which each texel belongs.</span></span><br/>                           |
| [<span data-ttu-id="b9edc-126">**GetGutterMap**</span><span class="sxs-lookup"><span data-stu-id="b9edc-126">**GetGutterMap**</span></span>](id3dxtexturegutterhelper--getguttermap.md)           | <span data-ttu-id="b9edc-127">Riceve un valore della classe Texel che indica la classe Texel in base alla posizione di ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="b9edc-127">Receives a texel class value that indicates texel class according to each texel's location.</span></span><br/> |
| [<span data-ttu-id="b9edc-128">**GetHeight**</span><span class="sxs-lookup"><span data-stu-id="b9edc-128">**GetHeight**</span></span>](id3dxtexturegutterhelper--getheight.md)                 | <span data-ttu-id="b9edc-129">Recupera l'altezza, in pixel, della trama.</span><span class="sxs-lookup"><span data-stu-id="b9edc-129">Retrieves the height of the texture, in pixels.</span></span><br/>                                             |
| [<span data-ttu-id="b9edc-130">**GetTexelMap**</span><span class="sxs-lookup"><span data-stu-id="b9edc-130">**GetTexelMap**</span></span>](id3dxtexturegutterhelper--gettexelmap.md)             | <span data-ttu-id="b9edc-131">Recupera le coordinate di trama (u, v) di ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="b9edc-131">Retrieves the (u, v) texture coordinates of each texel.</span></span><br/>                                     |
| [<span data-ttu-id="b9edc-132">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="b9edc-132">**GetWidth**</span></span>](id3dxtexturegutterhelper--getwidth.md)                   | <span data-ttu-id="b9edc-133">Recupera la larghezza della trama in pixel.</span><span class="sxs-lookup"><span data-stu-id="b9edc-133">Retrieves the width of the texture, in pixels.</span></span><br/>                                              |
| [<span data-ttu-id="b9edc-134">**ResampleTex**</span><span class="sxs-lookup"><span data-stu-id="b9edc-134">**ResampleTex**</span></span>](id3dxtexturegutterhelper--resampletex.md)             | <span data-ttu-id="b9edc-135">Ricampiona una trama nella parametrizzazione di questo gutterhelper.</span><span class="sxs-lookup"><span data-stu-id="b9edc-135">Resamples a texture into this gutterhelper's parameterization.</span></span><br/>                              |
| [<span data-ttu-id="b9edc-136">**SetBaryMap**</span><span class="sxs-lookup"><span data-stu-id="b9edc-136">**SetBaryMap**</span></span>](id3dxtexturegutterhelper--setbarymap.md)               | <span data-ttu-id="b9edc-137">Imposta le coordinate del baricentrica Texel.</span><span class="sxs-lookup"><span data-stu-id="b9edc-137">Sets texel barycentric coordinates.</span></span><br/>                                                         |
| [<span data-ttu-id="b9edc-138">**SetFaceMap**</span><span class="sxs-lookup"><span data-stu-id="b9edc-138">**SetFaceMap**</span></span>](id3dxtexturegutterhelper--setfacemap.md)               | <span data-ttu-id="b9edc-139">Imposta l'indice della faccia mesh a cui appartiene ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="b9edc-139">Sets the index of the mesh face to which each texel belongs.</span></span><br/>                                |
| [<span data-ttu-id="b9edc-140">**SetGutterMap**</span><span class="sxs-lookup"><span data-stu-id="b9edc-140">**SetGutterMap**</span></span>](id3dxtexturegutterhelper--setguttermap.md)           | <span data-ttu-id="b9edc-141">Imposta un valore della classe Texel che indica la classe Texel in base alla posizione di ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="b9edc-141">Sets a texel class value that indicates texel class according to each texel's location.</span></span><br/>     |
| [<span data-ttu-id="b9edc-142">**SetTexelMap**</span><span class="sxs-lookup"><span data-stu-id="b9edc-142">**SetTexelMap**</span></span>](id3dxtexturegutterhelper--settexelmap.md)             | <span data-ttu-id="b9edc-143">Imposta le coordinate di trama (u, v) di ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="b9edc-143">Sets the (u, v) texture coordinates of each texel.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="b9edc-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9edc-144">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b9edc-145">Se usato con il trasferimento di luminosità pre-calcolato (PRT), questa interfaccia richiede una parametrizzazione univoca del modello.</span><span class="sxs-lookup"><span data-stu-id="b9edc-145">When used with precomputed radiance transfer (PRT), this interface requires a unique parameterization of the model.</span></span> <span data-ttu-id="b9edc-146">Ogni Texel deve corrispondere a un singolo punto sulla superficie del modello e viceversa.</span><span class="sxs-lookup"><span data-stu-id="b9edc-146">Every texel must correspond to a single point on the surface of the model and vice-versa.</span></span> <span data-ttu-id="b9edc-147">Se il modello include più trame, deve essere suddiviso in parti separate, ognuna delle quali contiene un oggetto di supporto per la gronda per trama.</span><span class="sxs-lookup"><span data-stu-id="b9edc-147">If the model includes multiple textures, it must be split into separate pieces that each contain one gutter helper object per texture.</span></span>

 

<span data-ttu-id="b9edc-148">Questa interfaccia può essere utilizzata per generare una mappa nello spazio di trama in cui ogni Texel si trova in una delle quattro classi.</span><span class="sxs-lookup"><span data-stu-id="b9edc-148">This interface can be used to generate a map in texture space in which each texel is in one of four classes.</span></span>



| <span data-ttu-id="b9edc-149">Classe Texel</span><span class="sxs-lookup"><span data-stu-id="b9edc-149">Texel Class</span></span> | <span data-ttu-id="b9edc-150">Percorso Texel</span><span class="sxs-lookup"><span data-stu-id="b9edc-150">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9edc-151">0</span><span class="sxs-lookup"><span data-stu-id="b9edc-151">0</span></span>           | <span data-ttu-id="b9edc-152">Punto non valido; Texel non verrà usato.</span><span class="sxs-lookup"><span data-stu-id="b9edc-152">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="b9edc-153">1</span><span class="sxs-lookup"><span data-stu-id="b9edc-153">1</span></span>           | <span data-ttu-id="b9edc-154">Triangolo interno.</span><span class="sxs-lookup"><span data-stu-id="b9edc-154">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="b9edc-155">2</span><span class="sxs-lookup"><span data-stu-id="b9edc-155">2</span></span>           | <span data-ttu-id="b9edc-156">Barra interna.</span><span class="sxs-lookup"><span data-stu-id="b9edc-156">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="b9edc-157">4</span><span class="sxs-lookup"><span data-stu-id="b9edc-157">4</span></span>           | <span data-ttu-id="b9edc-158">Barra interna; Texel verrà valutato come un esempio completo nei metodi [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)o [**ID3DXTextureGutterHelper:: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) .</span><span class="sxs-lookup"><span data-stu-id="b9edc-158">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

<span data-ttu-id="b9edc-159">Per le classi 1 e 2, un Texel viene archiviato con la faccia a cui appartiene, insieme alle coordinate baricentrica dei primi due vertici della faccia.</span><span class="sxs-lookup"><span data-stu-id="b9edc-159">For classes 1 and 2, a texel is stored with the face it belongs to, along with barycentric coordinates of the first two vertices of that face.</span></span> <span data-ttu-id="b9edc-160">I vertici della gronda vengono assegnati al bordo più vicino nello spazio di trama.</span><span class="sxs-lookup"><span data-stu-id="b9edc-160">Gutter vertices are assigned to the closest edge in texture space.</span></span>

<span data-ttu-id="b9edc-161">Nessuna classe Texel 3.</span><span class="sxs-lookup"><span data-stu-id="b9edc-161">There is no texel class 3.</span></span>

<span data-ttu-id="b9edc-162">L'interfaccia **ID3DXTextureGutterHelper** viene ottenuta chiamando la funzione [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="b9edc-162">The **ID3DXTextureGutterHelper** interface is obtained by calling the [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) function.</span></span>

<span data-ttu-id="b9edc-163">Il tipo LPD3DXTEXTUREGUTTERHELPER è definito come puntatore all'interfaccia **ID3DXTextureGutterHelper** .</span><span class="sxs-lookup"><span data-stu-id="b9edc-163">The LPD3DXTEXTUREGUTTERHELPER type is defined as a pointer to the **ID3DXTextureGutterHelper** interface.</span></span>


```
typedef interface ID3DXTextureGutterHelper ID3DXTextureGutterHelper;
typedef interface ID3DXTextureGutterHelper *LPD3DXTEXTUREGUTTERHELPER;
```



## <a name="requirements"></a><span data-ttu-id="b9edc-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9edc-164">Requirements</span></span>



| <span data-ttu-id="b9edc-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9edc-165">Requirement</span></span> | <span data-ttu-id="b9edc-166">Valore</span><span class="sxs-lookup"><span data-stu-id="b9edc-166">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9edc-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9edc-167">Header</span></span><br/>  | <dl> <span data-ttu-id="b9edc-168"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9edc-168"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b9edc-169">Libreria</span><span class="sxs-lookup"><span data-stu-id="b9edc-169">Library</span></span><br/> | <dl> <span data-ttu-id="b9edc-170"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9edc-170"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b9edc-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9edc-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9edc-172">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="b9edc-172">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
