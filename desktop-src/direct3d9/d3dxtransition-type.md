---
description: Definisce lo stile di transizione tra i valori di un'animazione mesh.
ms.assetid: 4416ef28-ba6b-47ca-be7d-831daad619e5
title: Enumerazione D3DXTRANSITION_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRANSITION_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0ca6ef7f9dcee8e865a1cd4089aecd1bc239d5d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969342"
---
# <a name="d3dxtransition_type-enumeration"></a><span data-ttu-id="73d90-103">\_Enumerazione del tipo D3DXTRANSITION</span><span class="sxs-lookup"><span data-stu-id="73d90-103">D3DXTRANSITION\_TYPE enumeration</span></span>

<span data-ttu-id="73d90-104">Definisce lo stile di transizione tra i valori di un'animazione mesh.</span><span class="sxs-lookup"><span data-stu-id="73d90-104">Defines the transition style between values of a mesh animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="73d90-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73d90-105">Syntax</span></span>


```C++
typedef enum D3DXTRANSITION_TYPE { 
  D3DXTRANSITION_LINEAR         = 0x000,
  D3DXTRANSITION_EASEINEASEOUT  = 0x001,
  D3DXTRANSITION_FORCE_DWORD    = 0x7fffffff
} D3DXTRANSITION_TYPE, *LPD3DXTRANSITION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="73d90-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="73d90-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="73d90-107"><span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION \_ lineare**</span><span class="sxs-lookup"><span data-stu-id="73d90-107"><span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="73d90-108">Transizione lineare tra i valori.</span><span class="sxs-lookup"><span data-stu-id="73d90-108">Linear transition between values.</span></span>

</dd> <dt>

<span data-ttu-id="73d90-109"><span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**\_EASEINEASEOUT D3DXTRANSITION**</span><span class="sxs-lookup"><span data-stu-id="73d90-109"><span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION\_EASEINEASEOUT**</span></span>
</dt> <dd>

<span data-ttu-id="73d90-110">Semplicità di transizione della spline tra i valori.</span><span class="sxs-lookup"><span data-stu-id="73d90-110">Ease-in, ease-out spline transition between values.</span></span>

</dd> <dt>

<span data-ttu-id="73d90-111"><span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="73d90-111"><span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="73d90-112">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="73d90-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="73d90-113">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="73d90-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="73d90-114">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="73d90-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73d90-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="73d90-115">Remarks</span></span>

<span data-ttu-id="73d90-116">Il calcolo per la rampa da Ease in a Ease Out viene calcolato come segue:</span><span class="sxs-lookup"><span data-stu-id="73d90-116">The calculation for the ramp from ease in to ease out is calculated as follows:</span></span>

<dl> <span data-ttu-id="73d90-117">Q (t) = 2 (x-y) t ³ + 3 (y-x) t ² + x</span><span class="sxs-lookup"><span data-stu-id="73d90-117">Q(t) = 2(x - y)t³ + 3(y - x)t² + x</span></span>  
</dl>

<span data-ttu-id="73d90-118">dove la rampa è una funzione Q (t) con le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="73d90-118">where the ramp is a function Q(t) with the following properties:</span></span>

-   <span data-ttu-id="73d90-119">Q (t) è una spline cubica.</span><span class="sxs-lookup"><span data-stu-id="73d90-119">Q(t) is a cubic spline.</span></span>
-   <span data-ttu-id="73d90-120">Q (t) esegue l'interpolazione tra x e y come intervallo t compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="73d90-120">Q(t) interpolates between x and y as t ranges from 0 to 1.</span></span>
-   <span data-ttu-id="73d90-121">Q (t) è orizzontale quando t = 0 e t = 1.</span><span class="sxs-lookup"><span data-stu-id="73d90-121">Q(t) is horizontal when t = 0 and t = 1.</span></span>

<span data-ttu-id="73d90-122">In matematica, questo si traduce in:</span><span class="sxs-lookup"><span data-stu-id="73d90-122">Mathematically, this translates into:</span></span>

<dl> <span data-ttu-id="73d90-123">Q (t) = at ³ + BT ² + CT + D (e quindi Q ' (t) = 3At ² + 2Bt + C)</span><span class="sxs-lookup"><span data-stu-id="73d90-123">Q(t) = At³ + Bt² + Ct + D (and therefore, Q'(t) = 3At² + 2Bt + C)</span></span>  
<span data-ttu-id="73d90-124">2a) Q (0) = x</span><span class="sxs-lookup"><span data-stu-id="73d90-124">2a) Q(0) = x</span></span>  
<span data-ttu-id="73d90-125">2b) Q (1) = y</span><span class="sxs-lookup"><span data-stu-id="73d90-125">2b) Q(1) = y</span></span>  
<span data-ttu-id="73d90-126">3a) Q ' (0) = 0</span><span class="sxs-lookup"><span data-stu-id="73d90-126">3a) Q'(0) = 0</span></span>  
<span data-ttu-id="73d90-127">3B) Q ' (1) = 0</span><span class="sxs-lookup"><span data-stu-id="73d90-127">3b) Q'(1) = 0</span></span>  
</dl>

<span data-ttu-id="73d90-128">Risoluzione per A, B, C, D:</span><span class="sxs-lookup"><span data-stu-id="73d90-128">Solving for A, B, C, D:</span></span>

<dl> <span data-ttu-id="73d90-129">D = x (da 2a)</span><span class="sxs-lookup"><span data-stu-id="73d90-129">D = x (from 2a)</span></span>  
<span data-ttu-id="73d90-130">C = 0 (da 3A)</span><span class="sxs-lookup"><span data-stu-id="73d90-130">C = 0 (from 3a)</span></span>  
<span data-ttu-id="73d90-131">3A + 2B = 0 (da 3B)</span><span class="sxs-lookup"><span data-stu-id="73d90-131">3A + 2B = 0 (from 3b)</span></span>  
<span data-ttu-id="73d90-132">A + B = y-x (da 2b e D = x)</span><span class="sxs-lookup"><span data-stu-id="73d90-132">A + B = y - x (from 2b and D = x)</span></span>  
</dl>

<span data-ttu-id="73d90-133">Di conseguenza:</span><span class="sxs-lookup"><span data-stu-id="73d90-133">Therefore:</span></span>

<dl> <span data-ttu-id="73d90-134">A = 2 (x-y), B = 3 (y-x), C = 0, D = x</span><span class="sxs-lookup"><span data-stu-id="73d90-134">A = 2(x - y), B = 3(y - x), C = 0, D = x</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="73d90-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73d90-135">Requirements</span></span>



| <span data-ttu-id="73d90-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="73d90-136">Requirement</span></span> | <span data-ttu-id="73d90-137">Valore</span><span class="sxs-lookup"><span data-stu-id="73d90-137">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73d90-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="73d90-138">Header</span></span><br/> | <dl> <span data-ttu-id="73d90-139"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="73d90-139"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73d90-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73d90-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73d90-141">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="73d90-141">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




