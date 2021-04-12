---
description: Le applicazioni utilizzano i metodi dell'interfaccia ID3DXBaseMesh per modificare ed eseguire query sugli oggetti mesh e mesh progressivi.
ms.assetid: ec4ccd77-e370-470c-9325-3d794a8f7f16
title: Interfaccia ID3DXBaseMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58029639852b30f5de357bb2643583615c45485c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355029"
---
# <a name="id3dxbasemesh-interface"></a><span data-ttu-id="02691-103">Interfaccia ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="02691-103">ID3DXBaseMesh interface</span></span>

<span data-ttu-id="02691-104">Le applicazioni utilizzano i metodi dell'interfaccia **ID3DXBaseMesh** per modificare ed eseguire query sugli oggetti mesh e mesh progressivi.</span><span class="sxs-lookup"><span data-stu-id="02691-104">Applications use the methods of the **ID3DXBaseMesh** interface to manipulate and query mesh and progressive mesh objects.</span></span>

## <a name="members"></a><span data-ttu-id="02691-105">Membri</span><span class="sxs-lookup"><span data-stu-id="02691-105">Members</span></span>

<span data-ttu-id="02691-106">L'interfaccia **ID3DXBaseMesh** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="02691-106">The **ID3DXBaseMesh** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="02691-107">**ID3DXBaseMesh** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="02691-107">**ID3DXBaseMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="02691-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="02691-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="02691-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="02691-109">Methods</span></span>

<span data-ttu-id="02691-110">L'interfaccia **ID3DXBaseMesh** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="02691-110">The **ID3DXBaseMesh** interface has these methods.</span></span>



| <span data-ttu-id="02691-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="02691-111">Method</span></span>                                                                            | <span data-ttu-id="02691-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02691-112">Description</span></span>                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02691-113">**CloneMesh**</span><span class="sxs-lookup"><span data-stu-id="02691-113">**CloneMesh**</span></span>](id3dxbasemesh--clonemesh.md)                                     | <span data-ttu-id="02691-114">Clona una mesh usando un dichiaratore.</span><span class="sxs-lookup"><span data-stu-id="02691-114">Clones a mesh using a declarator.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="02691-115">**CloneMeshFVF**</span><span class="sxs-lookup"><span data-stu-id="02691-115">**CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)                               | <span data-ttu-id="02691-116">Clona una mesh usando un codice FVF (Flexible Vertex Format).</span><span class="sxs-lookup"><span data-stu-id="02691-116">Clones a mesh using a flexible vertex format (FVF) code.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="02691-117">**ConvertAdjacencyToPointReps**</span><span class="sxs-lookup"><span data-stu-id="02691-117">**ConvertAdjacencyToPointReps**</span></span>](id3dxbasemesh--convertadjacencytopointreps.md) | <span data-ttu-id="02691-118">Converte le informazioni adiacenza mesh in una matrice di rappresentanti punto.</span><span class="sxs-lookup"><span data-stu-id="02691-118">Converts mesh adjacency information to an array of point representatives.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="02691-119">**ConvertPointRepsToAdjacency**</span><span class="sxs-lookup"><span data-stu-id="02691-119">**ConvertPointRepsToAdjacency**</span></span>](id3dxbasemesh--convertpointrepstoadjacency.md) | <span data-ttu-id="02691-120">Converte i dati rappresentativi del punto in informazioni adiacenza mesh.</span><span class="sxs-lookup"><span data-stu-id="02691-120">Converts point representative data to mesh adjacency information.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="02691-121">**DrawSubset**</span><span class="sxs-lookup"><span data-stu-id="02691-121">**DrawSubset**</span></span>](id3dxbasemesh--drawsubset.md)                                   | <span data-ttu-id="02691-122">Disegna un subset di una mesh.</span><span class="sxs-lookup"><span data-stu-id="02691-122">Draws a subset of a mesh.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="02691-123">**GenerateAdjacency**</span><span class="sxs-lookup"><span data-stu-id="02691-123">**GenerateAdjacency**</span></span>](id3dxbasemesh--generateadjacency.md)                     | <span data-ttu-id="02691-124">Genera un elenco di bordi della mesh, oltre a un elenco di visi che condividono ogni bordo.</span><span class="sxs-lookup"><span data-stu-id="02691-124">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="02691-125">**GetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="02691-125">**GetAttributeTable**</span></span>](id3dxbasemesh--getattributetable.md)                     | <span data-ttu-id="02691-126">Recupera una tabella di attributi per una mesh o il numero di voci archiviate in una tabella di attributi per una mesh.</span><span class="sxs-lookup"><span data-stu-id="02691-126">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span><br/>                                                                                          |
| [<span data-ttu-id="02691-127">**GetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="02691-127">**GetDeclaration**</span></span>](id3dxbasemesh--getdeclaration.md)                           | <span data-ttu-id="02691-128">Recupera una dichiarazione che descrive i vertici nella mesh.</span><span class="sxs-lookup"><span data-stu-id="02691-128">Retrieves a declaration describing the vertices in the mesh.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="02691-129">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="02691-129">**GetDevice**</span></span>](id3dxbasemesh--getdevice.md)                                     | <span data-ttu-id="02691-130">Recupera il dispositivo associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="02691-130">Retrieves the device associated with the mesh.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="02691-131">**GetFVF**</span><span class="sxs-lookup"><span data-stu-id="02691-131">**GetFVF**</span></span>](id3dxbasemesh--getfvf.md)                                           | <span data-ttu-id="02691-132">Ottiene il valore del vertice della funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="02691-132">Gets the fixed function vertex value.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="02691-133">**GetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="02691-133">**GetIndexBuffer**</span></span>](id3dxbasemesh--getindexbuffer.md)                           | <span data-ttu-id="02691-134">Recupera i dati in un buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="02691-134">Retrieves the data in an index buffer.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="02691-135">**GetNumBytesPerVertex**</span><span class="sxs-lookup"><span data-stu-id="02691-135">**GetNumBytesPerVertex**</span></span>](id3dxbasemesh--getnumbytespervertex.md)               | <span data-ttu-id="02691-136">Ottiene il numero di byte per vertice.</span><span class="sxs-lookup"><span data-stu-id="02691-136">Gets the number of bytes per vertex.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="02691-137">**GetNumFaces**</span><span class="sxs-lookup"><span data-stu-id="02691-137">**GetNumFaces**</span></span>](id3dxbasemesh--getnumfaces.md)                                 | <span data-ttu-id="02691-138">Recupera il numero di visi nella rete.</span><span class="sxs-lookup"><span data-stu-id="02691-138">Retrieves the number of faces in the mesh.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="02691-139">**GetNumVertices**</span><span class="sxs-lookup"><span data-stu-id="02691-139">**GetNumVertices**</span></span>](id3dxbasemesh--getnumvertices.md)                           | <span data-ttu-id="02691-140">Recupera il numero di vertici nella rete.</span><span class="sxs-lookup"><span data-stu-id="02691-140">Retrieves the number of vertices in the mesh.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="02691-141">**GetOptions**</span><span class="sxs-lookup"><span data-stu-id="02691-141">**GetOptions**</span></span>](id3dxbasemesh--getoptions.md)                                   | <span data-ttu-id="02691-142">Recupera le opzioni di mesh abilitate per questa mesh al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="02691-142">Retrieves the mesh options enabled for this mesh at creation time.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="02691-143">**GetVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="02691-143">**GetVertexBuffer**</span></span>](id3dxbasemesh--getvertexbuffer.md)                         | <span data-ttu-id="02691-144">Recupera il buffer dei vertici associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="02691-144">Retrieves the vertex buffer associated with the mesh.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="02691-145">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="02691-145">**LockIndexBuffer**</span></span>](id3dxbasemesh--lockindexbuffer.md)                         | <span data-ttu-id="02691-146">Blocca un buffer di indice e ottiene un puntatore alla memoria del buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="02691-146">Locks an index buffer and obtains a pointer to the index buffer memory.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="02691-147">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="02691-147">**LockVertexBuffer**</span></span>](id3dxbasemesh--lockvertexbuffer.md)                       | <span data-ttu-id="02691-148">Blocca un buffer dei vertici e ottiene un puntatore alla memoria del buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="02691-148">Locks a vertex buffer and obtains a pointer to the vertex buffer memory.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="02691-149">**UnlockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="02691-149">**UnlockIndexBuffer**</span></span>](id3dxbasemesh--unlockindexbuffer.md)                     | <span data-ttu-id="02691-150">Sblocca un buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="02691-150">Unlocks an index buffer.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="02691-151">**UnlockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="02691-151">**UnlockVertexBuffer**</span></span>](id3dxbasemesh--unlockvertexbuffer.md)                   | <span data-ttu-id="02691-152">Sblocca un buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="02691-152">Unlocks a vertex buffer.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="02691-153">**UpdateSemantics**</span><span class="sxs-lookup"><span data-stu-id="02691-153">**UpdateSemantics**</span></span>](id3dxbasemesh--updatesemantics.md)                         | <span data-ttu-id="02691-154">Questo metodo consente all'utente di modificare la dichiarazione mesh senza modificare il layout dei dati del buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="02691-154">This method allows the user to change the mesh declaration without changing the data layout of the vertex buffer.</span></span> <span data-ttu-id="02691-155">La chiamata è valida solo se il vecchio e il nuovo formato di dichiarazione hanno le stesse dimensioni del vertice.</span><span class="sxs-lookup"><span data-stu-id="02691-155">The call is valid only if the old and new declaration formats have the same vertex size.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="02691-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="02691-156">Remarks</span></span>

<span data-ttu-id="02691-157">Una mesh è un oggetto costituito da un set di visi poligonali.</span><span class="sxs-lookup"><span data-stu-id="02691-157">A mesh is an object made up of a set of polygonal faces.</span></span> <span data-ttu-id="02691-158">Una mesh definisce un set di vertici e un set di visi (i visi vengono definiti in termini di vertici e normali della mesh).</span><span class="sxs-lookup"><span data-stu-id="02691-158">A mesh defines a set of vertices and a set of faces (the faces are defined in terms of the vertices and normals of the mesh).</span></span>

<span data-ttu-id="02691-159">Il tipo LPD3DXBASEMESH è definito come puntatore all'interfaccia **ID3DXBaseMesh** .</span><span class="sxs-lookup"><span data-stu-id="02691-159">The LPD3DXBASEMESH type is defined as a pointer to the **ID3DXBaseMesh** interface.</span></span>


```
typedef struct ID3DXBaseMesh *LPD3DXBASEMESH;
```



## <a name="requirements"></a><span data-ttu-id="02691-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02691-160">Requirements</span></span>



| <span data-ttu-id="02691-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="02691-161">Requirement</span></span> | <span data-ttu-id="02691-162">Valore</span><span class="sxs-lookup"><span data-stu-id="02691-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02691-163">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02691-163">Header</span></span><br/>  | <dl> <span data-ttu-id="02691-164"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="02691-164"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="02691-165">Libreria</span><span class="sxs-lookup"><span data-stu-id="02691-165">Library</span></span><br/> | <dl> <span data-ttu-id="02691-166"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02691-166"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="02691-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02691-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02691-168">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="02691-168">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
