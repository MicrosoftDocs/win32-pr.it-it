---
description: Descrive una superficie di rendering.
ms.assetid: cffa1555-1fa2-427d-8bcb-da0e61d82152
title: Struttura D3DXRTS_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 3a0b52f258956f7b62734ca97cc5d1bf5ed00ac3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969345"
---
# <a name="d3dxrts_desc-structure"></a><span data-ttu-id="a3291-103">\_Struttura D3DXRTS DESC</span><span class="sxs-lookup"><span data-stu-id="a3291-103">D3DXRTS\_DESC structure</span></span>

<span data-ttu-id="a3291-104">Descrive una superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="a3291-104">Describes a render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3291-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3291-105">Syntax</span></span>


```C++
typedef struct D3DXRTS_DESC {
  UINT      Width;
  UINT      Height;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTS_DESC, *LPD3DXRTS_DESC;
```



## <a name="members"></a><span data-ttu-id="a3291-106">Members</span><span class="sxs-lookup"><span data-stu-id="a3291-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a3291-107">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="a3291-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="a3291-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3291-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a3291-109">Larghezza della superficie di rendering, in pixel.</span><span class="sxs-lookup"><span data-stu-id="a3291-109">Width of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a3291-110">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="a3291-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="a3291-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3291-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a3291-112">Altezza della superficie di rendering, in pixel.</span><span class="sxs-lookup"><span data-stu-id="a3291-112">Height of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a3291-113">**Formato**</span><span class="sxs-lookup"><span data-stu-id="a3291-113">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="a3291-114">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="a3291-114">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a3291-115">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato pixel della superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="a3291-115">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the pixel format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="a3291-116">**DepthStencil**</span><span class="sxs-lookup"><span data-stu-id="a3291-116">**DepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="a3291-117">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3291-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a3291-118">Se **true**, la superficie di rendering supporta una superficie di stencil profondità; in caso contrario, questo membro è impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="a3291-118">If **TRUE**, the render surface supports a depth-stencil surface; otherwise this member is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a3291-119">**DepthStencilFormat**</span><span class="sxs-lookup"><span data-stu-id="a3291-119">**DepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="a3291-120">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="a3291-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a3291-121">Se DepthStencil è impostato su **true**, questo parametro è un membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato di stencil depth della superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="a3291-121">If DepthStencil is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the depth-stencil format of the render surface.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3291-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3291-122">Requirements</span></span>



| <span data-ttu-id="a3291-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3291-123">Requirement</span></span> | <span data-ttu-id="a3291-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a3291-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3291-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3291-125">Header</span></span><br/> | <dl> <span data-ttu-id="a3291-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3291-126"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3291-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3291-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3291-128">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="a3291-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="a3291-129">**ID3DXRenderToSurface:: getdesc**</span><span class="sxs-lookup"><span data-stu-id="a3291-129">**ID3DXRenderToSurface::GetDesc**</span></span>](id3dxrendertosurface--getdesc.md)
</dt> </dl>

 

 
