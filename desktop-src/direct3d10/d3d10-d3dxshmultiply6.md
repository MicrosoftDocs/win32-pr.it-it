---
description: Calcola il prodotto di due funzioni di armonica sferica (f e g). Entrambe le funzioni sono di ordine N = 6.
ms.assetid: 3b68b238-c1ae-4ab8-89ed-bdf815463143
title: Funzione D3DXSHMultiply6 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply6
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0768bb8be1f2f23693a431a2c0ea8f3d5a6846d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323193"
---
# <a name="d3dxshmultiply6-function"></a><span data-ttu-id="dc85d-104">D3DXSHMultiply6 (funzione)</span><span class="sxs-lookup"><span data-stu-id="dc85d-104">D3DXSHMultiply6 function</span></span>

<span data-ttu-id="dc85d-105">Calcola il prodotto di due funzioni di armonica sferica (f e g).</span><span class="sxs-lookup"><span data-stu-id="dc85d-105">Computes the product of two spherical harmonics functions (f and g).</span></span> <span data-ttu-id="dc85d-106">Entrambe le funzioni sono di ordine N = 6.</span><span class="sxs-lookup"><span data-stu-id="dc85d-106">Both functions are of order N = 6.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc85d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc85d-107">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply6(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="dc85d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc85d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc85d-109">*broncio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc85d-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc85d-110">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc85d-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dc85d-111">Puntatore ai coefficienti SH di output: la funzione di base *Y* LM è archiviata in corrispondenza di l ² + *m* + l.</span><span class="sxs-lookup"><span data-stu-id="dc85d-111">Pointer to the output SH coefficients — the basis function *Y* ₗₘ is stored at l² + *m* + l.</span></span> <span data-ttu-id="dc85d-112">L'ordine *N* determina la lunghezza della matrice, in cui devono essere sempre presenti coefficienti *n*².</span><span class="sxs-lookup"><span data-stu-id="dc85d-112">The order *N* determines the length of the array, where there should always be *N*² coefficients.</span></span>

</dd> <dt>

<span data-ttu-id="dc85d-113">*PF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc85d-113">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc85d-114">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="dc85d-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dc85d-115">Coefficienti SH di input per la prima funzione.</span><span class="sxs-lookup"><span data-stu-id="dc85d-115">Input SH coefficients for first function.</span></span>

</dd> <dt>

<span data-ttu-id="dc85d-116">*PG* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc85d-116">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc85d-117">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="dc85d-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dc85d-118">Secondo set di coefficienti SH di input.</span><span class="sxs-lookup"><span data-stu-id="dc85d-118">Second set of input SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc85d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc85d-119">Return value</span></span>

<span data-ttu-id="dc85d-120">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc85d-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dc85d-121">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="dc85d-121">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc85d-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc85d-122">Remarks</span></span>

<span data-ttu-id="dc85d-123">Il prodotto di due funzioni SH dell'ordine N = 6 genera una funzione SH dell'ordine 2 × *N* -1 = 11, ma i risultati vengono troncati.</span><span class="sxs-lookup"><span data-stu-id="dc85d-123">The product of two SH functions of order N = 6 generates an SH function of order 2 × *N* - 1 = 11, but the results are truncated.</span></span> <span data-ttu-id="dc85d-124">Ciò significa che il prodotto si sposta ( *f* × *g*  =  *g* × *f* ) ma non associa ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).</span><span class="sxs-lookup"><span data-stu-id="dc85d-124">This means that the product commutes ( *f* × *g* = *g* × *f* ) but doesn't associate ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).</span></span>

<span data-ttu-id="dc85d-125">Questa funzione usa l'equazione seguente:</span><span class="sxs-lookup"><span data-stu-id="dc85d-125">This function uses the following equation:</span></span>


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



<span data-ttu-id="dc85d-126">dove y i \_ (s) è la funzione di base per i/o e dove f (s) e g (s) usano la funzione SH seguente:</span><span class="sxs-lookup"><span data-stu-id="dc85d-126">where y\_i(s) is the ith SH basis function, and where f(s) and g(s) use the following SH function:</span></span>


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a><span data-ttu-id="dc85d-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc85d-127">Requirements</span></span>



| <span data-ttu-id="dc85d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc85d-128">Requirement</span></span> | <span data-ttu-id="dc85d-129">Valore</span><span class="sxs-lookup"><span data-stu-id="dc85d-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc85d-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc85d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="dc85d-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc85d-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="dc85d-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="dc85d-132">Library</span></span><br/> | <dl> <span data-ttu-id="dc85d-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc85d-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dc85d-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc85d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc85d-135">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="dc85d-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
