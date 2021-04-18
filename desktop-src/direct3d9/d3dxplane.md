---
description: Descrive un piano.
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: Struttura D3DXPLANE (D3dx9math. h)
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
- d3dx9math.h
ms.openlocfilehash: 260f9555313aea3443f0728f2b50189228429803
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322109"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a><span data-ttu-id="e5247-103">Struttura D3DXPLANE (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e5247-103">D3DXPLANE structure (D3dx9math.h)</span></span>

<span data-ttu-id="e5247-104">Descrive un piano.</span><span class="sxs-lookup"><span data-stu-id="e5247-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5247-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5247-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="e5247-106">Members</span><span class="sxs-lookup"><span data-stu-id="e5247-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e5247-107">**un**</span><span class="sxs-lookup"><span data-stu-id="e5247-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="e5247-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5247-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e5247-109">Il coefficiente del piano di ritaglio nell'equazione del piano generale.</span><span class="sxs-lookup"><span data-stu-id="e5247-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="e5247-110">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="e5247-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e5247-111">**b**</span><span class="sxs-lookup"><span data-stu-id="e5247-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="e5247-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5247-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e5247-113">Coefficiente b del piano di ritaglio nell'equazione del piano generale.</span><span class="sxs-lookup"><span data-stu-id="e5247-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="e5247-114">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="e5247-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e5247-115">**c**</span><span class="sxs-lookup"><span data-stu-id="e5247-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="e5247-116">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5247-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e5247-117">Coefficiente c del piano di ritaglio nell'equazione del piano generale.</span><span class="sxs-lookup"><span data-stu-id="e5247-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="e5247-118">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="e5247-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e5247-119">**d**</span><span class="sxs-lookup"><span data-stu-id="e5247-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="e5247-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5247-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e5247-121">Coefficiente d del piano di ritaglio nell'equazione del piano generale.</span><span class="sxs-lookup"><span data-stu-id="e5247-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="e5247-122">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="e5247-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5247-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5247-123">Remarks</span></span>

<span data-ttu-id="e5247-124">I membri della struttura **D3DXPLANE** prendono il formato dell'equazione generale del piano.</span><span class="sxs-lookup"><span data-stu-id="e5247-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="e5247-125">Si adattano all'equazione del piano generale, in modo che **un** x + **b** y + **c** z + **d** w = 0.</span><span class="sxs-lookup"><span data-stu-id="e5247-125">They fit into the general plane equation so that **a** x + **b** y + **c** z + **d** w = 0.</span></span>

<span data-ttu-id="e5247-126">I programmatori C++ possono sfruttare l'overload degli operatori e il cast dei tipi con le [**estensioni D3DXPLANE**](d3dxplane-extensions.md) che implementano costruttori di overload e operatori di assegnazione, unario e binari (inclusi uguaglianza).</span><span class="sxs-lookup"><span data-stu-id="e5247-126">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXPLANE Extensions**](d3dxplane-extensions.md) which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5247-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5247-127">Requirements</span></span>



| <span data-ttu-id="e5247-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5247-128">Requirement</span></span> | <span data-ttu-id="e5247-129">Valore</span><span class="sxs-lookup"><span data-stu-id="e5247-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5247-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5247-130">Header</span></span><br/> | <dl> <span data-ttu-id="e5247-131"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5247-131"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5247-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5247-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5247-133">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="e5247-133">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
