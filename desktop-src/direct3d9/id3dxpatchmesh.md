---
description: Questa interfaccia incapsula la funzionalità di patch mesh.
ms.assetid: c70c0fe0-b695-4ad9-b0c6-7854cf8f7593
title: Interfaccia ID3DXPatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f1f13e6abe3a164e8027ddcb6bb33e9f0ca618fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355209"
---
# <a name="id3dxpatchmesh-interface"></a><span data-ttu-id="1c8f2-103">Interfaccia ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="1c8f2-103">ID3DXPatchMesh interface</span></span>

<span data-ttu-id="1c8f2-104">Questa interfaccia incapsula la funzionalità di patch mesh.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-104">This interface encapsulates patch mesh functionality.</span></span>

## <a name="members"></a><span data-ttu-id="1c8f2-105">Membri</span><span class="sxs-lookup"><span data-stu-id="1c8f2-105">Members</span></span>

<span data-ttu-id="1c8f2-106">L'interfaccia **ID3DXPatchMesh** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1c8f2-106">The **ID3DXPatchMesh** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1c8f2-107">**ID3DXPatchMesh** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1c8f2-107">**ID3DXPatchMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="1c8f2-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="1c8f2-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1c8f2-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="1c8f2-109">Methods</span></span>

<span data-ttu-id="1c8f2-110">L'interfaccia **ID3DXPatchMesh** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-110">The **ID3DXPatchMesh** interface has these methods.</span></span>



| <span data-ttu-id="1c8f2-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="1c8f2-111">Method</span></span>                                                                           | <span data-ttu-id="1c8f2-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c8f2-112">Description</span></span>                                                                                     |
|:---------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c8f2-113">**CloneMesh**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-113">**CloneMesh**</span></span>](id3dxpatchmesh--clonemesh.md)                                   | <span data-ttu-id="1c8f2-114">Crea una nuova mesh della patch con la dichiarazione di vertice specificata.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-114">Creates a new patch mesh with the specified vertex declaration.</span></span><br/>                      |
| [<span data-ttu-id="1c8f2-115">**GenerateAdjacency**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-115">**GenerateAdjacency**</span></span>](id3dxpatchmesh--generateadjacency.md)                   | <span data-ttu-id="1c8f2-116">Generare un elenco di bordi della rete e le patch che condividono ogni bordo.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-116">Generate a list of mesh edges and the patches that share each edge.</span></span><br/>                  |
| [<span data-ttu-id="1c8f2-117">**GetControlVerticesPerPatch**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-117">**GetControlVerticesPerPatch**</span></span>](id3dxpatchmesh--getcontrolverticesperpatch.md) | <span data-ttu-id="1c8f2-118">Ottiene il numero di vertici di controllo per patch.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-118">Gets the number of control vertices per patch.</span></span><br/>                                       |
| [<span data-ttu-id="1c8f2-119">**GetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-119">**GetDeclaration**</span></span>](id3dxpatchmesh--getdeclaration.md)                         | <span data-ttu-id="1c8f2-120">Ottiene la dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-120">Gets the vertex declaration.</span></span><br/>                                                         |
| [<span data-ttu-id="1c8f2-121">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-121">**GetDevice**</span></span>](id3dxpatchmesh--getdevice.md)                                   | <span data-ttu-id="1c8f2-122">Ottiene il dispositivo che ha creato la mesh.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-122">Gets the device that created the mesh.</span></span><br/>                                               |
| [<span data-ttu-id="1c8f2-123">**GetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-123">**GetDisplaceParam**</span></span>](id3dxpatchmesh--getdisplaceparam.md)                     | <span data-ttu-id="1c8f2-124">Ottiene i parametri di spostamento della geometria mesh.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-124">Gets mesh geometry displacement parameters.</span></span><br/>                                          |
| [<span data-ttu-id="1c8f2-125">**GetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-125">**GetIndexBuffer**</span></span>](id3dxpatchmesh--getindexbuffer.md)                         | <span data-ttu-id="1c8f2-126">Ottiene il buffer dell'indice mesh.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-126">Gets the mesh index buffer.</span></span><br/>                                                          |
| [<span data-ttu-id="1c8f2-127">**GetNumPatches**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-127">**GetNumPatches**</span></span>](id3dxpatchmesh--getnumpatches.md)                           | <span data-ttu-id="1c8f2-128">Ottiene il numero di patch nella rete.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-128">Gets the number of patches in the mesh.</span></span><br/>                                              |
| [<span data-ttu-id="1c8f2-129">**GetNumVertices**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-129">**GetNumVertices**</span></span>](id3dxpatchmesh--getnumvertices.md)                         | <span data-ttu-id="1c8f2-130">Ottiene il numero di vertici nella rete.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-130">Gets the number of vertices in the mesh.</span></span><br/>                                             |
| [<span data-ttu-id="1c8f2-131">**GetOptions**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-131">**GetOptions**</span></span>](id3dxpatchmesh--getoptions.md)                                 | <span data-ttu-id="1c8f2-132">Ottiene il tipo di patch.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-132">Gets the type of patch.</span></span><br/>                                                              |
| [<span data-ttu-id="1c8f2-133">**GetPatchInfo**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-133">**GetPatchInfo**</span></span>](id3dxpatchmesh--getpatchinfo.md)                             | <span data-ttu-id="1c8f2-134">Ottiene gli attributi della patch.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-134">Gets the attributes of the patch.</span></span><br/>                                                    |
| [<span data-ttu-id="1c8f2-135">**GetTessSize**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-135">**GetTessSize**</span></span>](id3dxpatchmesh--gettesssize.md)                               | <span data-ttu-id="1c8f2-136">Ottiene le dimensioni della mesh tassellati, dato un livello a mosaico.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-136">Gets the size of the tessellated mesh, given a tessellation level.</span></span><br/>                   |
| [<span data-ttu-id="1c8f2-137">**GetVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-137">**GetVertexBuffer**</span></span>](id3dxpatchmesh--getvertexbuffer.md)                       | <span data-ttu-id="1c8f2-138">Ottiene il buffer del vertice mesh.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-138">Gets the mesh vertex buffer.</span></span><br/>                                                         |
| [<span data-ttu-id="1c8f2-139">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-139">**LockAttributeBuffer**</span></span>](id3dxpatchmesh--lockattributebuffer.md)               | <span data-ttu-id="1c8f2-140">Blocca il buffer dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-140">Locks the attribute buffer.</span></span><br/>                                                          |
| [<span data-ttu-id="1c8f2-141">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-141">**LockIndexBuffer**</span></span>](id3dxpatchmesh--lockindexbuffer.md)                       | <span data-ttu-id="1c8f2-142">Blocca il buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-142">Lock the index buffer.</span></span><br/>                                                               |
| [<span data-ttu-id="1c8f2-143">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-143">**LockVertexBuffer**</span></span>](id3dxpatchmesh--lockvertexbuffer.md)                     | <span data-ttu-id="1c8f2-144">Blocca il buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-144">Lock the vertex buffer.</span></span><br/>                                                              |
| [<span data-ttu-id="1c8f2-145">**Ottimizzare**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-145">**Optimize**</span></span>](id3dxpatchmesh--optimize.md)                                     | <span data-ttu-id="1c8f2-146">Ottimizza la mesh della patch per un efficiente mosaico.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-146">Optimizes the patch mesh for efficient tessellation.</span></span><br/>                                 |
| [<span data-ttu-id="1c8f2-147">**SetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-147">**SetDisplaceParam**</span></span>](id3dxpatchmesh--setdisplaceparam.md)                     | <span data-ttu-id="1c8f2-148">Imposta i parametri di spostamento della geometria mesh.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-148">Sets mesh geometry displacement parameters.</span></span><br/>                                          |
| [<span data-ttu-id="1c8f2-149">**Conteggiarla suddividerla**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-149">**Tessellate**</span></span>](id3dxpatchmesh--tessellate.md)                                 | <span data-ttu-id="1c8f2-150">Esegue lo schema a mosaico uniforme in base al livello del mosaico.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-150">Performs uniform tessellation based on the tessellation level.</span></span><br/>                       |
| [<span data-ttu-id="1c8f2-151">**TessellateAdaptive**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-151">**TessellateAdaptive**</span></span>](id3dxpatchmesh--tessellateadaptive.md)                 | <span data-ttu-id="1c8f2-152">Esegue lo schema a mosaico adattivo basato sul criterio a mosaico adattivo basato su z.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-152">Performs adaptive tessellation based on the z-based adaptive tessellation criterion.</span></span><br/> |
| [<span data-ttu-id="1c8f2-153">**UnlockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-153">**UnlockAttributeBuffer**</span></span>](id3dxpatchmesh--unlockattributebuffer.md)           | <span data-ttu-id="1c8f2-154">Sbloccare il buffer dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-154">Unlock the attribute buffer.</span></span><br/>                                                         |
| [<span data-ttu-id="1c8f2-155">**UnlockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-155">**UnlockIndexBuffer**</span></span>](id3dxpatchmesh--unlockindexbuffer.md)                   | <span data-ttu-id="1c8f2-156">Sbloccare il buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-156">Unlock the index buffer.</span></span><br/>                                                             |
| [<span data-ttu-id="1c8f2-157">**UnlockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="1c8f2-157">**UnlockVertexBuffer**</span></span>](id3dxpatchmesh--unlockvertexbuffer.md)                 | <span data-ttu-id="1c8f2-158">Sbloccare il buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-158">Unlock the vertex buffer.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="1c8f2-159">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c8f2-159">Remarks</span></span>

<span data-ttu-id="1c8f2-160">Una mesh patch è un reticolo costituito da una serie di patch.</span><span class="sxs-lookup"><span data-stu-id="1c8f2-160">A patch mesh is a mesh that consists of a series of patches.</span></span>

<span data-ttu-id="1c8f2-161">Per ottenere l'interfaccia **ID3DXPatchMesh** , chiamare la funzione [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="1c8f2-161">To obtain the **ID3DXPatchMesh** interface, call the [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) function.</span></span>

<span data-ttu-id="1c8f2-162">Il tipo LPD3DXPATCHMESH è definito come puntatore all'interfaccia **ID3DXPatchMesh** , come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="1c8f2-162">The LPD3DXPATCHMESH type is defined as a pointer to the **ID3DXPatchMesh** interface, as follows:</span></span>


```
typedef struct ID3DXPatchMesh *LPD3DXPATCHMESH;
```



## <a name="requirements"></a><span data-ttu-id="1c8f2-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c8f2-163">Requirements</span></span>



| <span data-ttu-id="1c8f2-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c8f2-164">Requirement</span></span> | <span data-ttu-id="1c8f2-165">Valore</span><span class="sxs-lookup"><span data-stu-id="1c8f2-165">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c8f2-166">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c8f2-166">Header</span></span><br/>  | <dl> <span data-ttu-id="1c8f2-167"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c8f2-167"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1c8f2-168">Libreria</span><span class="sxs-lookup"><span data-stu-id="1c8f2-168">Library</span></span><br/> | <dl> <span data-ttu-id="1c8f2-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c8f2-169"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1c8f2-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c8f2-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c8f2-171">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="1c8f2-171">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="1c8f2-172">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="1c8f2-172">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
