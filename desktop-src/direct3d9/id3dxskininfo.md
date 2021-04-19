---
description: Le applicazioni usano i metodi dell'interfaccia ID3DXSkinInfo per modificare le matrici ossee, che vengono usate per l'animazione dei dati del vertice. Questa interfaccia non è più strettamente legata a ID3DXMesh e può essere usata per interfacciare qualsiasi set di dati dei vertici.
ms.assetid: 4ccf88b0-2cc7-4e91-a0f2-fb8eea66a3ce
title: Interfaccia ID3DXSkinInfo (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: afb93a0513bef7de1b0815b8b1f50179e2cba41d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322434"
---
# <a name="id3dxskininfo-interface"></a><span data-ttu-id="2be0d-104">Interfaccia ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="2be0d-104">ID3DXSkinInfo interface</span></span>

<span data-ttu-id="2be0d-105">Le applicazioni usano i metodi dell'interfaccia ID3DXSkinInfo per modificare le matrici ossee, che vengono usate per l'animazione dei dati del vertice.</span><span class="sxs-lookup"><span data-stu-id="2be0d-105">Applications use the methods of the ID3DXSkinInfo interface to manipulate bone matrices, which are used to skin vertex data for animation.</span></span> <span data-ttu-id="2be0d-106">Questa interfaccia non è più strettamente legata a [**ID3DXMesh**](id3dxmesh.md) e può essere usata per interfacciare qualsiasi set di dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="2be0d-106">This interface is no longer strictly tied to [**ID3DXMesh**](id3dxmesh.md) and can be used to skin any set of vertex data.</span></span>

## <a name="members"></a><span data-ttu-id="2be0d-107">Membri</span><span class="sxs-lookup"><span data-stu-id="2be0d-107">Members</span></span>

<span data-ttu-id="2be0d-108">L'interfaccia **ID3DXSkinInfo** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2be0d-108">The **ID3DXSkinInfo** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2be0d-109">**ID3DXSkinInfo** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2be0d-109">**ID3DXSkinInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="2be0d-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="2be0d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2be0d-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="2be0d-111">Methods</span></span>

<span data-ttu-id="2be0d-112">L'interfaccia **ID3DXSkinInfo** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2be0d-112">The **ID3DXSkinInfo** interface has these methods.</span></span>



| <span data-ttu-id="2be0d-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="2be0d-113">Method</span></span>                                                                              | <span data-ttu-id="2be0d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2be0d-114">Description</span></span>                                                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2be0d-115">**Clone**</span><span class="sxs-lookup"><span data-stu-id="2be0d-115">**Clone**</span></span>](id3dxskininfo--clone.md)                                               | <span data-ttu-id="2be0d-116">Clona un oggetto info di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="2be0d-116">Clones a skin info object.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="2be0d-117">**ConvertToBlendedMesh**</span><span class="sxs-lookup"><span data-stu-id="2be0d-117">**ConvertToBlendedMesh**</span></span>](id3dxskininfo--converttoblendedmesh.md)                 | <span data-ttu-id="2be0d-118">Accetta una mesh e restituisce una nuova mesh con pesi di Blend per vertice e una tabella delle combinazioni di osso.</span><span class="sxs-lookup"><span data-stu-id="2be0d-118">Takes a mesh and returns a new mesh with per-vertex blend weights and a bone combination table.</span></span> <span data-ttu-id="2be0d-119">La tabella descrive le ossa che influiscono sui subset della mesh.</span><span class="sxs-lookup"><span data-stu-id="2be0d-119">The table describes which bones affect which subsets of the mesh.</span></span><br/>                   |
| [<span data-ttu-id="2be0d-120">**ConvertToIndexedBlendedMesh**</span><span class="sxs-lookup"><span data-stu-id="2be0d-120">**ConvertToIndexedBlendedMesh**</span></span>](id3dxskininfo--converttoindexedblendedmesh.md)   | <span data-ttu-id="2be0d-121">Acquisisce una mesh e restituisce una nuova mesh con pesi di Blend per vertice, indici e una tabella combinata Bone.</span><span class="sxs-lookup"><span data-stu-id="2be0d-121">Takes a mesh and returns a new mesh with per-vertex blend weights, indices, and a bone combination table.</span></span> <span data-ttu-id="2be0d-122">La tabella descrive le tavolozze ossee che influiscono sui subset della mesh.</span><span class="sxs-lookup"><span data-stu-id="2be0d-122">The table describes which bone palettes affect which subsets of the mesh.</span></span><br/> |
| [<span data-ttu-id="2be0d-123">**FindBoneVertexInfluenceIndex**</span><span class="sxs-lookup"><span data-stu-id="2be0d-123">**FindBoneVertexInfluenceIndex**</span></span>](id3dxskininfo--findbonevertexinfluenceindex.md) | <span data-ttu-id="2be0d-124">Recupera l'indice dell'influenza ossea che interessa un singolo vertice.</span><span class="sxs-lookup"><span data-stu-id="2be0d-124">Retrieves the index of the bone influence affecting a single vertex.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="2be0d-125">**GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="2be0d-125">**GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)                         | <span data-ttu-id="2be0d-126">Ottiene i vertici e i pesi influenzati da un osso.</span><span class="sxs-lookup"><span data-stu-id="2be0d-126">Gets the vertices and weights that a bone influences.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="2be0d-127">**Getbonename**</span><span class="sxs-lookup"><span data-stu-id="2be0d-127">**GetBoneName**</span></span>](id3dxskininfo--getbonename.md)                                   | <span data-ttu-id="2be0d-128">Ottiene il nome dell'osso, dall'indice di osso.</span><span class="sxs-lookup"><span data-stu-id="2be0d-128">Gets the bone name, from the bone index.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="2be0d-129">**GetBoneOffsetMatrix**</span><span class="sxs-lookup"><span data-stu-id="2be0d-129">**GetBoneOffsetMatrix**</span></span>](id3dxskininfo--getboneoffsetmatrix.md)                   | <span data-ttu-id="2be0d-130">Ottiene la matrice di offset dell'osso.</span><span class="sxs-lookup"><span data-stu-id="2be0d-130">Gets the bone offset matrix.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="2be0d-131">**GetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="2be0d-131">**GetBoneVertexInfluence**</span></span>](id3dxskininfo--getbonevertexinfluence.md)             | <span data-ttu-id="2be0d-132">Recupera il fattore di fusione e il vertice interessati da un'influenza dell'osso specificata.</span><span class="sxs-lookup"><span data-stu-id="2be0d-132">Retrieves the blend factor and vertex affected by a specified bone influence.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="2be0d-133">**GetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="2be0d-133">**GetDeclaration**</span></span>](id3dxskininfo--getdeclaration.md)                             | <span data-ttu-id="2be0d-134">Ottiene la dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="2be0d-134">Gets the vertex declaration.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="2be0d-135">**GetFVF**</span><span class="sxs-lookup"><span data-stu-id="2be0d-135">**GetFVF**</span></span>](id3dxskininfo--getfvf.md)                                             | <span data-ttu-id="2be0d-136">Ottiene il valore del vertice della funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="2be0d-136">Gets the fixed function vertex value.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="2be0d-137">**GetMaxFaceInfluences**</span><span class="sxs-lookup"><span data-stu-id="2be0d-137">**GetMaxFaceInfluences**</span></span>](id3dxskininfo--getmaxfaceinfluences.md)                 | <span data-ttu-id="2be0d-138">Ottiene le influenze massime della faccia in una mesh triangolare con il buffer di indice specificato.</span><span class="sxs-lookup"><span data-stu-id="2be0d-138">Gets the maximum face influences in a triangle mesh with the specified index buffer.</span></span><br/>                                                                                                |
| [<span data-ttu-id="2be0d-139">**GetMaxVertexInfluences**</span><span class="sxs-lookup"><span data-stu-id="2be0d-139">**GetMaxVertexInfluences**</span></span>](id3dxskininfo--getmaxvertexinfluences.md)             | <span data-ttu-id="2be0d-140">Ottiene il numero massimo di influenze per qualsiasi vertice nella mesh.</span><span class="sxs-lookup"><span data-stu-id="2be0d-140">Gets the maximum number of influences for any vertex in the mesh.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="2be0d-141">**GetMinBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="2be0d-141">**GetMinBoneInfluence**</span></span>](id3dxskininfo--getminboneinfluence.md)                   | <span data-ttu-id="2be0d-142">Ottiene l'influenza dell'osso minima.</span><span class="sxs-lookup"><span data-stu-id="2be0d-142">Gets the minimum bone influence.</span></span> <span data-ttu-id="2be0d-143">I valori più piccoli di quelli che vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="2be0d-143">Influence values smaller than this are ignored.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="2be0d-144">**GetNumBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="2be0d-144">**GetNumBoneInfluences**</span></span>](id3dxskininfo--getnumboneinfluences.md)                 | <span data-ttu-id="2be0d-145">Ottiene il numero di influenze per un osso.</span><span class="sxs-lookup"><span data-stu-id="2be0d-145">Gets the number of influences for a bone.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="2be0d-146">**GetNumBones**</span><span class="sxs-lookup"><span data-stu-id="2be0d-146">**GetNumBones**</span></span>](id3dxskininfo--getnumbones.md)                                   | <span data-ttu-id="2be0d-147">Ottiene il numero di ossa.</span><span class="sxs-lookup"><span data-stu-id="2be0d-147">Gets the number of bones.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="2be0d-148">**Modificare il mapping**</span><span class="sxs-lookup"><span data-stu-id="2be0d-148">**Remap**</span></span>](id3dxskininfo--remap.md)                                               | <span data-ttu-id="2be0d-149">Aggiorna le informazioni sull'influenza ossea in modo che corrispondano ai vertici dopo essere stati riordinati.</span><span class="sxs-lookup"><span data-stu-id="2be0d-149">Updates bone influence information to match vertices after they are reordered.</span></span> <span data-ttu-id="2be0d-150">Questo metodo deve essere chiamato se il buffer dei vertici di destinazione è stato riordinato esternamente.</span><span class="sxs-lookup"><span data-stu-id="2be0d-150">This method should be called if the target vertex buffer has been reordered externally.</span></span><br/>              |
| [<span data-ttu-id="2be0d-151">**SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="2be0d-151">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)                         | <span data-ttu-id="2be0d-152">Imposta il valore di influenza per un osso.</span><span class="sxs-lookup"><span data-stu-id="2be0d-152">Sets the influence value for a bone.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="2be0d-153">**Sebonename**</span><span class="sxs-lookup"><span data-stu-id="2be0d-153">**SetBoneName**</span></span>](id3dxskininfo--setbonename.md)                                   | <span data-ttu-id="2be0d-154">Imposta il nome dell'osso.</span><span class="sxs-lookup"><span data-stu-id="2be0d-154">Sets the bone name.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="2be0d-155">**SetBoneOffsetMatrix**</span><span class="sxs-lookup"><span data-stu-id="2be0d-155">**SetBoneOffsetMatrix**</span></span>](id3dxskininfo--setboneoffsetmatrix.md)                   | <span data-ttu-id="2be0d-156">Imposta la matrice di offset dell'osso.</span><span class="sxs-lookup"><span data-stu-id="2be0d-156">Sets the bone offset matrix.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="2be0d-157">**SetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="2be0d-157">**SetBoneVertexInfluence**</span></span>](id3dxskininfo--setbonevertexinfluence.md)             | <span data-ttu-id="2be0d-158">Imposta un valore di influenza di un osso in un singolo vertice.</span><span class="sxs-lookup"><span data-stu-id="2be0d-158">Sets an influence value of a bone on a single vertex.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="2be0d-159">**Dichiarazione di**</span><span class="sxs-lookup"><span data-stu-id="2be0d-159">**SetDeclaration**</span></span>](id3dxskininfo--setdeclaration.md)                             | <span data-ttu-id="2be0d-160">Imposta la dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="2be0d-160">Sets the vertex declaration.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="2be0d-161">**SetFVF**</span><span class="sxs-lookup"><span data-stu-id="2be0d-161">**SetFVF**</span></span>](id3dxskininfo--setfvf.md)                                             | <span data-ttu-id="2be0d-162">Imposta il tipo FVF (Flexible Vertex Format).</span><span class="sxs-lookup"><span data-stu-id="2be0d-162">Sets the flexible vertex format (FVF) type.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="2be0d-163">**SetMinBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="2be0d-163">**SetMinBoneInfluence**</span></span>](id3dxskininfo--setminboneinfluence.md)                   | <span data-ttu-id="2be0d-164">Imposta l'influenza dell'osso minima.</span><span class="sxs-lookup"><span data-stu-id="2be0d-164">Sets the minimum bone influence.</span></span> <span data-ttu-id="2be0d-165">I valori più piccoli di quelli che vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="2be0d-165">Influence values smaller than this are ignored.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="2be0d-166">**UpdateSkinnedMesh**</span><span class="sxs-lookup"><span data-stu-id="2be0d-166">**UpdateSkinnedMesh**</span></span>](id3dxskininfo--updateskinnedmesh.md)                       | <span data-ttu-id="2be0d-167">Applica il skining del software ai vertici di destinazione in base alle matrici correnti.</span><span class="sxs-lookup"><span data-stu-id="2be0d-167">Applies software skinning to the target vertices based on the current matrices.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="2be0d-168">Commenti</span><span class="sxs-lookup"><span data-stu-id="2be0d-168">Remarks</span></span>

<span data-ttu-id="2be0d-169">Creare un'interfaccia **ID3DXSkinInfo** con [**D3DXCreateSkinInfo**](d3dxcreateskininfo.md), [**D3DXCreateSkinInfoFromBlendedMesh**](d3dxcreateskininfofromblendedmesh.md)o [**D3DXCreateSkinInfoFVF**](d3dxcreateskininfofvf.md).</span><span class="sxs-lookup"><span data-stu-id="2be0d-169">Create a **ID3DXSkinInfo** interface with [**D3DXCreateSkinInfo**](d3dxcreateskininfo.md), [**D3DXCreateSkinInfoFromBlendedMesh**](d3dxcreateskininfofromblendedmesh.md), or [**D3DXCreateSkinInfoFVF**](d3dxcreateskininfofvf.md).</span></span>

<span data-ttu-id="2be0d-170">Il tipo LPD3DXSKININFO è definito come puntatore all'interfaccia **ID3DXSkinInfo** .</span><span class="sxs-lookup"><span data-stu-id="2be0d-170">The LPD3DXSKININFO type is defined as a pointer to the **ID3DXSkinInfo** interface.</span></span>


```
typedef struct ID3DXSkinInfo *LPD3DXSKININFO;
```



## <a name="requirements"></a><span data-ttu-id="2be0d-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2be0d-171">Requirements</span></span>



| <span data-ttu-id="2be0d-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="2be0d-172">Requirement</span></span> | <span data-ttu-id="2be0d-173">Valore</span><span class="sxs-lookup"><span data-stu-id="2be0d-173">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2be0d-174">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2be0d-174">Header</span></span><br/>  | <dl> <span data-ttu-id="2be0d-175"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2be0d-175"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2be0d-176">Libreria</span><span class="sxs-lookup"><span data-stu-id="2be0d-176">Library</span></span><br/> | <dl> <span data-ttu-id="2be0d-177"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2be0d-177"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2be0d-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2be0d-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2be0d-179">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="2be0d-179">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
