---
description: Descrive un piano.
ms.assetid: c6da7343-a4f3-4cac-855b-14bd70c0d3c2
title: Struttura D3DXPLANE (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 9949aec16e90a53e01e536255c20f442052bb98b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355654"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a><span data-ttu-id="841d3-103">Struttura D3DXPLANE (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="841d3-103">D3DXPLANE structure (D3DX10Math.h)</span></span>

<span data-ttu-id="841d3-104">Descrive un piano.</span><span class="sxs-lookup"><span data-stu-id="841d3-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="841d3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="841d3-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="841d3-106">Members</span><span class="sxs-lookup"><span data-stu-id="841d3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="841d3-107">**un**</span><span class="sxs-lookup"><span data-stu-id="841d3-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="841d3-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="841d3-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="841d3-109">Il coefficiente del piano di ritaglio nell'equazione del piano generale.</span><span class="sxs-lookup"><span data-stu-id="841d3-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="841d3-110">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="841d3-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="841d3-111">**b**</span><span class="sxs-lookup"><span data-stu-id="841d3-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="841d3-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="841d3-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="841d3-113">Coefficiente b del piano di ritaglio nell'equazione del piano generale.</span><span class="sxs-lookup"><span data-stu-id="841d3-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="841d3-114">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="841d3-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="841d3-115">**c**</span><span class="sxs-lookup"><span data-stu-id="841d3-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="841d3-116">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="841d3-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="841d3-117">Coefficiente c del piano di ritaglio nell'equazione del piano generale.</span><span class="sxs-lookup"><span data-stu-id="841d3-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="841d3-118">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="841d3-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="841d3-119">**d**</span><span class="sxs-lookup"><span data-stu-id="841d3-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="841d3-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="841d3-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="841d3-121">Coefficiente d del piano di ritaglio nell'equazione del piano generale.</span><span class="sxs-lookup"><span data-stu-id="841d3-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="841d3-122">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="841d3-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="841d3-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="841d3-123">Remarks</span></span>

<span data-ttu-id="841d3-124">I membri della struttura **D3DXPLANE** prendono il formato dell'equazione generale del piano.</span><span class="sxs-lookup"><span data-stu-id="841d3-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="841d3-125">Si adattano all'equazione generale del piano in modo che ax + by + CZ + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="841d3-125">They fit into the general plane equation so that ax + by + cz + dw = 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="841d3-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="841d3-126">Requirements</span></span>



| <span data-ttu-id="841d3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="841d3-127">Requirement</span></span> | <span data-ttu-id="841d3-128">Valore</span><span class="sxs-lookup"><span data-stu-id="841d3-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="841d3-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="841d3-129">Header</span></span><br/> | <dl> <span data-ttu-id="841d3-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="841d3-130"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="841d3-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="841d3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="841d3-132">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="841d3-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
