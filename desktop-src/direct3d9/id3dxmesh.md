---
description: Per modificare gli oggetti mesh, le applicazioni utilizzano i metodi dell'interfaccia ID3DXMesh.
ms.assetid: f571fe0b-3f0c-43c9-809c-d1e14f85b720
title: Interfaccia ID3DXMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c2a677edba4bad5e908b6dd69aa21a467b2a245
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355714"
---
# <a name="id3dxmesh-interface"></a><span data-ttu-id="78a0d-103">Interfaccia ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="78a0d-103">ID3DXMesh interface</span></span>

<span data-ttu-id="78a0d-104">Per modificare gli oggetti mesh, le applicazioni utilizzano i metodi dell'interfaccia ID3DXMesh.</span><span class="sxs-lookup"><span data-stu-id="78a0d-104">Applications use the methods of the ID3DXMesh interface to manipulate mesh objects.</span></span>

## <a name="members"></a><span data-ttu-id="78a0d-105">Membri</span><span class="sxs-lookup"><span data-stu-id="78a0d-105">Members</span></span>

<span data-ttu-id="78a0d-106">L'interfaccia **ID3DXMesh** eredita da [**ID3DXBaseMesh**](id3dxbasemesh.md).</span><span class="sxs-lookup"><span data-stu-id="78a0d-106">The **ID3DXMesh** interface inherits from [**ID3DXBaseMesh**](id3dxbasemesh.md).</span></span> <span data-ttu-id="78a0d-107">**ID3DXMesh** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="78a0d-107">**ID3DXMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="78a0d-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="78a0d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="78a0d-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="78a0d-109">Methods</span></span>

<span data-ttu-id="78a0d-110">L'interfaccia **ID3DXMesh** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="78a0d-110">The **ID3DXMesh** interface has these methods.</span></span>



| <span data-ttu-id="78a0d-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="78a0d-111">Method</span></span>                                                            | <span data-ttu-id="78a0d-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78a0d-112">Description</span></span>                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78a0d-113">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="78a0d-113">**LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)     | <span data-ttu-id="78a0d-114">Blocca il buffer mesh che contiene i dati dell'attributo mesh e restituisce un puntatore.</span><span class="sxs-lookup"><span data-stu-id="78a0d-114">Locks the mesh buffer that contains the mesh attribute data, and returns a pointer to it.</span></span><br/>                                   |
| [<span data-ttu-id="78a0d-115">**Ottimizzare**</span><span class="sxs-lookup"><span data-stu-id="78a0d-115">**Optimize**</span></span>](id3dxmesh--optimize.md)                           | <span data-ttu-id="78a0d-116">Genera una nuova mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.</span><span class="sxs-lookup"><span data-stu-id="78a0d-116">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span><br/>                                     |
| [<span data-ttu-id="78a0d-117">**OptimizeInplace**</span><span class="sxs-lookup"><span data-stu-id="78a0d-117">**OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)             | <span data-ttu-id="78a0d-118">Genera una mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.</span><span class="sxs-lookup"><span data-stu-id="78a0d-118">Generates a mesh with reordered faces and vertices to optimize drawing performance.</span></span> <span data-ttu-id="78a0d-119">Questo metodo riordina la mesh esistente.</span><span class="sxs-lookup"><span data-stu-id="78a0d-119">This method reorders the existing mesh.</span></span><br/> |
| [<span data-ttu-id="78a0d-120">**SetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="78a0d-120">**SetAttributeTable**</span></span>](id3dxmesh--setattributetable.md)         | <span data-ttu-id="78a0d-121">Imposta la tabella degli attributi per una mesh e il numero di voci archiviate nella tabella.</span><span class="sxs-lookup"><span data-stu-id="78a0d-121">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span><br/>                                          |
| [<span data-ttu-id="78a0d-122">**UnlockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="78a0d-122">**UnlockAttributeBuffer**</span></span>](id3dxmesh--unlockattributebuffer.md) | <span data-ttu-id="78a0d-123">Sblocca un buffer dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="78a0d-123">Unlocks an attribute buffer.</span></span><br/>                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="78a0d-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="78a0d-124">Remarks</span></span>

<span data-ttu-id="78a0d-125">Per ottenere l'interfaccia **ID3DXMesh** , chiamare la funzione [**D3DXCreateMesh**](d3dxcreatemesh.md) o [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) .</span><span class="sxs-lookup"><span data-stu-id="78a0d-125">To obtain the **ID3DXMesh** interface, call either the [**D3DXCreateMesh**](d3dxcreatemesh.md) or [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) function.</span></span>

<span data-ttu-id="78a0d-126">Questa interfaccia eredita funzionalità aggiuntive dall'interfaccia [**ID3DXBaseMesh**](id3dxbasemesh.md) .</span><span class="sxs-lookup"><span data-stu-id="78a0d-126">This interface inherits additional functionality from the [**ID3DXBaseMesh**](id3dxbasemesh.md) interface.</span></span>

<span data-ttu-id="78a0d-127">Il tipo LPD3DXMESH è definito come puntatore all'interfaccia **ID3DXMesh** .</span><span class="sxs-lookup"><span data-stu-id="78a0d-127">The LPD3DXMESH type is defined as a pointer to the **ID3DXMesh** interface.</span></span>


```
typedef struct ID3DXMesh *LPD3DXMESH;
```



## <a name="requirements"></a><span data-ttu-id="78a0d-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78a0d-128">Requirements</span></span>



| <span data-ttu-id="78a0d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="78a0d-129">Requirement</span></span> | <span data-ttu-id="78a0d-130">Valore</span><span class="sxs-lookup"><span data-stu-id="78a0d-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78a0d-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78a0d-131">Header</span></span><br/>  | <dl> <span data-ttu-id="78a0d-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="78a0d-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="78a0d-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="78a0d-133">Library</span></span><br/> | <dl> <span data-ttu-id="78a0d-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78a0d-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="78a0d-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78a0d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78a0d-136">**ID3DXBaseMesh**</span><span class="sxs-lookup"><span data-stu-id="78a0d-136">**ID3DXBaseMesh**</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="78a0d-137">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="78a0d-137">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="78a0d-138">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="78a0d-138">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




