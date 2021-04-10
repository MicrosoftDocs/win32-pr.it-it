---
description: Definisce un rettangolo.
ms.assetid: a8590411-fd34-4048-a41f-b4155d955573
title: Struttura D3DRECT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9a22b74869afa16ca0c55ac50975eb36ba590c7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762100"
---
# <a name="d3drect-structure"></a><span data-ttu-id="931c1-103">Struttura D3DRECT</span><span class="sxs-lookup"><span data-stu-id="931c1-103">D3DRECT structure</span></span>

<span data-ttu-id="931c1-104">Definisce un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="931c1-104">Defines a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="931c1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="931c1-105">Syntax</span></span>


```C++
typedef struct D3DRECT {
  LONG x1;
  LONG y1;
  LONG x2;
  LONG y2;
} D3DRECT;
```



## <a name="members"></a><span data-ttu-id="931c1-106">Members</span><span class="sxs-lookup"><span data-stu-id="931c1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="931c1-107">**X1**</span><span class="sxs-lookup"><span data-stu-id="931c1-107">**x1**</span></span>
</dt> <dd>

<span data-ttu-id="931c1-108">Tipo: **[ **Long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="931c1-108">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="931c1-109">Coordinata x dell'angolo superiore sinistro del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="931c1-109">The x-coordinate of the upper-left corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="931c1-110">**Y1**</span><span class="sxs-lookup"><span data-stu-id="931c1-110">**y1**</span></span>
</dt> <dd>

<span data-ttu-id="931c1-111">Tipo: **[ **Long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="931c1-111">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="931c1-112">Coordinata y dell'angolo superiore sinistro del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="931c1-112">The y-coordinate of the upper-left corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="931c1-113">**X2**</span><span class="sxs-lookup"><span data-stu-id="931c1-113">**x2**</span></span>
</dt> <dd>

<span data-ttu-id="931c1-114">Tipo: **[ **Long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="931c1-114">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="931c1-115">Coordinata x dell'angolo inferiore destro del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="931c1-115">The x-coordinate of the lower-right corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="931c1-116">**Y2**</span><span class="sxs-lookup"><span data-stu-id="931c1-116">**y2**</span></span>
</dt> <dd>

<span data-ttu-id="931c1-117">Tipo: **[ **Long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="931c1-117">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="931c1-118">Coordinata y dell'angolo inferiore destro del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="931c1-118">The y-coordinate of the lower-right corner of the rectangle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="931c1-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="931c1-119">Requirements</span></span>



| <span data-ttu-id="931c1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="931c1-120">Requirement</span></span> | <span data-ttu-id="931c1-121">Valore</span><span class="sxs-lookup"><span data-stu-id="931c1-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="931c1-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="931c1-122">Header</span></span><br/> | <dl> <span data-ttu-id="931c1-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="931c1-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="931c1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="931c1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="931c1-125">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="931c1-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="931c1-126">**Deselezionare**</span><span class="sxs-lookup"><span data-stu-id="931c1-126">**Clear**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
</dt> </dl>

 

 
