---
description: Descrive un volume.
ms.assetid: c0224f4e-3d32-4bdd-b56c-4e8aa291bb27
title: Struttura D3DVOLUME_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVOLUME_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b736333cefcfc8a3307ff7a0cecd53cd96bc0af2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355189"
---
# <a name="d3dvolume_desc-structure"></a><span data-ttu-id="2b1f1-103">\_Struttura D3DVOLUME DESC</span><span class="sxs-lookup"><span data-stu-id="2b1f1-103">D3DVOLUME\_DESC structure</span></span>

<span data-ttu-id="2b1f1-104">Descrive un volume.</span><span class="sxs-lookup"><span data-stu-id="2b1f1-104">Describes a volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b1f1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b1f1-105">Syntax</span></span>


```C++
typedef struct D3DVOLUME_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Width;
  UINT            Height;
  UINT            Depth;
} D3DVOLUME_DESC, *LPD3DVOLUME_DESC;
```



## <a name="members"></a><span data-ttu-id="2b1f1-106">Members</span><span class="sxs-lookup"><span data-stu-id="2b1f1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2b1f1-107">**Formato**</span><span class="sxs-lookup"><span data-stu-id="2b1f1-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="2b1f1-108">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="2b1f1-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2b1f1-109">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato di superficie del volume.</span><span class="sxs-lookup"><span data-stu-id="2b1f1-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the volume.</span></span>

</dd> <dt>

<span data-ttu-id="2b1f1-110">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2b1f1-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="2b1f1-111">Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="2b1f1-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2b1f1-112">Membro del tipo enumerato [**D3DRESOURCETYPE**](./d3dresourcetype.md) , che identifica questa risorsa come volume.</span><span class="sxs-lookup"><span data-stu-id="2b1f1-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a volume.</span></span>

</dd> <dt>

<span data-ttu-id="2b1f1-113">**Utilizzo**</span><span class="sxs-lookup"><span data-stu-id="2b1f1-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="2b1f1-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b1f1-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2b1f1-115">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="2b1f1-115">Currently not used.</span></span> <span data-ttu-id="2b1f1-116">Restituito sempre come 0.</span><span class="sxs-lookup"><span data-stu-id="2b1f1-116">Always returned as 0.</span></span>

</dd> <dt>

<span data-ttu-id="2b1f1-117">**Pool**</span><span class="sxs-lookup"><span data-stu-id="2b1f1-117">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="2b1f1-118">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="2b1f1-118">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2b1f1-119">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che specifica la classe di memoria allocata per questo volume.</span><span class="sxs-lookup"><span data-stu-id="2b1f1-119">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this volume.</span></span>

</dd> <dt>

<span data-ttu-id="2b1f1-120">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="2b1f1-120">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="2b1f1-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b1f1-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2b1f1-122">Larghezza, in pixel, del volume.</span><span class="sxs-lookup"><span data-stu-id="2b1f1-122">Width of the volume, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="2b1f1-123">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="2b1f1-123">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="2b1f1-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b1f1-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2b1f1-125">Altezza, in pixel, del volume.</span><span class="sxs-lookup"><span data-stu-id="2b1f1-125">Height of the volume, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="2b1f1-126">**Livello nidificazione**</span><span class="sxs-lookup"><span data-stu-id="2b1f1-126">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="2b1f1-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b1f1-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2b1f1-128">Profondità del volume, in pixel.</span><span class="sxs-lookup"><span data-stu-id="2b1f1-128">Depth of the volume, in pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b1f1-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b1f1-129">Requirements</span></span>



| <span data-ttu-id="2b1f1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b1f1-130">Requirement</span></span> | <span data-ttu-id="2b1f1-131">Valore</span><span class="sxs-lookup"><span data-stu-id="2b1f1-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b1f1-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b1f1-132">Header</span></span><br/> | <dl> <span data-ttu-id="2b1f1-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b1f1-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b1f1-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b1f1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b1f1-135">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="2b1f1-135">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="2b1f1-136">**Getdesc**</span><span class="sxs-lookup"><span data-stu-id="2b1f1-136">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-getdesc)
</dt> <dt>

[<span data-ttu-id="2b1f1-137">**GetLevelDesc**</span><span class="sxs-lookup"><span data-stu-id="2b1f1-137">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-getleveldesc)
</dt> </dl>

 

 
