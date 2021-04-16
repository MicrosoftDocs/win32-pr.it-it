---
description: Descrive un buffer del vertice.
ms.assetid: 0ae8f976-d0ca-4d55-b6db-5be85fa3c799
title: Struttura D3DVERTEXBUFFER_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b2c0838743f8190eeb0e5c825e7125d2e48c0b6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530985"
---
# <a name="d3dvertexbuffer_desc-structure"></a><span data-ttu-id="2a2bc-103">\_Struttura D3DVERTEXBUFFER DESC</span><span class="sxs-lookup"><span data-stu-id="2a2bc-103">D3DVERTEXBUFFER\_DESC structure</span></span>

<span data-ttu-id="2a2bc-104">Descrive un buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="2a2bc-104">Describes a vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a2bc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a2bc-105">Syntax</span></span>


```C++
typedef struct D3DVERTEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
  DWORD           FVF;
} D3DVERTEXBUFFER_DESC, *LPD3DVERTEXBUFFER_DESC;
```



## <a name="members"></a><span data-ttu-id="2a2bc-106">Members</span><span class="sxs-lookup"><span data-stu-id="2a2bc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2a2bc-107">**Formato**</span><span class="sxs-lookup"><span data-stu-id="2a2bc-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="2a2bc-108">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="2a2bc-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2a2bc-109">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato di superficie dei dati del buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="2a2bc-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the vertex buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="2a2bc-110">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2a2bc-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="2a2bc-111">Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="2a2bc-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2a2bc-112">Membro del tipo enumerato [**D3DRESOURCETYPE**](./d3dresourcetype.md) , che identifica questa risorsa come buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="2a2bc-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2a2bc-113">**Utilizzo**</span><span class="sxs-lookup"><span data-stu-id="2a2bc-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="2a2bc-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a2bc-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2a2bc-115">Combinazione di uno o più flag [**D3DUSAGE**](d3dusage.md) .</span><span class="sxs-lookup"><span data-stu-id="2a2bc-115">Combination of one or more [**D3DUSAGE**](d3dusage.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="2a2bc-116">**Pool**</span><span class="sxs-lookup"><span data-stu-id="2a2bc-116">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="2a2bc-117">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="2a2bc-117">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2a2bc-118">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che specifica la classe di memoria allocata per questo buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="2a2bc-118">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2a2bc-119">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="2a2bc-119">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="2a2bc-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a2bc-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2a2bc-121">Dimensioni in byte del buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="2a2bc-121">Size of the vertex buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2a2bc-122">**FVF**</span><span class="sxs-lookup"><span data-stu-id="2a2bc-122">**FVF**</span></span>
</dt> <dd>

<span data-ttu-id="2a2bc-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a2bc-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2a2bc-124">Combinazione di [D3DFVF](d3dfvf.md) che descrive il formato dei vertici in questo buffer.</span><span class="sxs-lookup"><span data-stu-id="2a2bc-124">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format of the vertices in this buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a2bc-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a2bc-125">Requirements</span></span>



| <span data-ttu-id="2a2bc-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a2bc-126">Requirement</span></span> | <span data-ttu-id="2a2bc-127">Valore</span><span class="sxs-lookup"><span data-stu-id="2a2bc-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a2bc-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a2bc-128">Header</span></span><br/> | <dl> <span data-ttu-id="2a2bc-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a2bc-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a2bc-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a2bc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a2bc-131">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="2a2bc-131">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="2a2bc-132">**Getdesc**</span><span class="sxs-lookup"><span data-stu-id="2a2bc-132">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-getdesc)
</dt> <dt>

[<span data-ttu-id="2a2bc-133">Buffer vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2a2bc-133">Vertex Buffers (Direct3D 9)</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
