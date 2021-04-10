---
description: Questa interfaccia viene implementata dall'applicazione per allocare o liberare oggetti contenitore di frame e mesh. I metodi di questo metodo vengono chiamati durante il caricamento e l'eliminazione delle gerarchie dei frame.
ms.assetid: b2c4ecb7-3655-4120-b957-724a754e948a
title: Interfaccia ID3DXAllocateHierarchy (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec7fb2da335ecd84889b75e81c850d16368f31eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058678"
---
# <a name="id3dxallocatehierarchy-interface"></a><span data-ttu-id="48c5d-104">Interfaccia ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="48c5d-104">ID3DXAllocateHierarchy interface</span></span>

<span data-ttu-id="48c5d-105">Questa interfaccia viene implementata dall'applicazione per allocare o liberare oggetti contenitore di frame e mesh.</span><span class="sxs-lookup"><span data-stu-id="48c5d-105">This interface is implemented by the application to allocate or free frame and mesh container objects.</span></span> <span data-ttu-id="48c5d-106">I metodi di questo metodo vengono chiamati durante il caricamento e l'eliminazione delle gerarchie dei frame.</span><span class="sxs-lookup"><span data-stu-id="48c5d-106">Methods on this are called during loading and destroying frame hierarchies.</span></span>

## <a name="members"></a><span data-ttu-id="48c5d-107">Membri</span><span class="sxs-lookup"><span data-stu-id="48c5d-107">Members</span></span>

<span data-ttu-id="48c5d-108">L'interfaccia **ID3DXAllocateHierarchy** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="48c5d-108">The **ID3DXAllocateHierarchy** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="48c5d-109">**ID3DXAllocateHierarchy** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="48c5d-109">**ID3DXAllocateHierarchy** also has these types of members:</span></span>

-   [<span data-ttu-id="48c5d-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="48c5d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="48c5d-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="48c5d-111">Methods</span></span>

<span data-ttu-id="48c5d-112">L'interfaccia **ID3DXAllocateHierarchy** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="48c5d-112">The **ID3DXAllocateHierarchy** interface has these methods.</span></span>



| <span data-ttu-id="48c5d-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="48c5d-113">Method</span></span>                                                                       | <span data-ttu-id="48c5d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48c5d-114">Description</span></span>                                                  |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="48c5d-115">**CreateFrame**</span><span class="sxs-lookup"><span data-stu-id="48c5d-115">**CreateFrame**</span></span>](id3dxallocatehierarchy--createframe.md)                   | <span data-ttu-id="48c5d-116">Richiede l'allocazione di un oggetto frame.</span><span class="sxs-lookup"><span data-stu-id="48c5d-116">Requests allocation of a frame object.</span></span><br/>            |
| [<span data-ttu-id="48c5d-117">**CreateMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="48c5d-117">**CreateMeshContainer**</span></span>](id3dxallocatehierarchy--createmeshcontainer.md)   | <span data-ttu-id="48c5d-118">Richiede l'allocazione di un oggetto contenitore mesh.</span><span class="sxs-lookup"><span data-stu-id="48c5d-118">Requests allocation of a mesh container object.</span></span><br/>   |
| [<span data-ttu-id="48c5d-119">**DestroyFrame**</span><span class="sxs-lookup"><span data-stu-id="48c5d-119">**DestroyFrame**</span></span>](id3dxallocatehierarchy--destroyframe.md)                 | <span data-ttu-id="48c5d-120">Richiede la deallocazione di un oggetto frame.</span><span class="sxs-lookup"><span data-stu-id="48c5d-120">Requests deallocation of a frame object.</span></span><br/>          |
| [<span data-ttu-id="48c5d-121">**DestroyMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="48c5d-121">**DestroyMeshContainer**</span></span>](id3dxallocatehierarchy--destroymeshcontainer.md) | <span data-ttu-id="48c5d-122">Richiede la deallocazione di un oggetto contenitore mesh.</span><span class="sxs-lookup"><span data-stu-id="48c5d-122">Requests deallocation of a mesh container object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="48c5d-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="48c5d-123">Remarks</span></span>

<span data-ttu-id="48c5d-124">Il tipo LPD3DXALLOCATEHIERARCHY è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="48c5d-124">The LPD3DXALLOCATEHIERARCHY type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXAllocateHierarchy ID3DXAllocateHierarchy;
typedef interface ID3DXAllocateHierarchy *LPD3DXALLOCATEHIERARCHY;
```



## <a name="requirements"></a><span data-ttu-id="48c5d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48c5d-125">Requirements</span></span>



| <span data-ttu-id="48c5d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="48c5d-126">Requirement</span></span> | <span data-ttu-id="48c5d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="48c5d-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48c5d-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="48c5d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="48c5d-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="48c5d-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="48c5d-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="48c5d-130">Library</span></span><br/> | <dl> <span data-ttu-id="48c5d-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48c5d-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="48c5d-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48c5d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48c5d-133">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="48c5d-133">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
