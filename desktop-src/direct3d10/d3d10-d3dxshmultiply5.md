---
description: Calcola il prodotto di due funzioni di armonica sferica (f e g). Entrambe le funzioni sono di ordine N = 5.
ms.assetid: c72231a1-9db3-4701-b7ad-4509028ce508
title: Funzione D3DXSHMultiply5 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply5
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b43fb89bdd5d6f75a4adca86323786d4a2bddac1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355574"
---
# <a name="d3dxshmultiply5-function"></a><span data-ttu-id="68efe-104">D3DXSHMultiply5 (funzione)</span><span class="sxs-lookup"><span data-stu-id="68efe-104">D3DXSHMultiply5 function</span></span>

<span data-ttu-id="68efe-105">Calcola il prodotto di due funzioni di armonica sferica (f e g).</span><span class="sxs-lookup"><span data-stu-id="68efe-105">Computes the product of two spherical harmonics functions (f and g).</span></span> <span data-ttu-id="68efe-106">Entrambe le funzioni sono di ordine N = 5.</span><span class="sxs-lookup"><span data-stu-id="68efe-106">Both functions are of order N = 5.</span></span>

## <a name="syntax"></a><span data-ttu-id="68efe-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68efe-107">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply5(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="68efe-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="68efe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68efe-109">*broncio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68efe-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68efe-110">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="68efe-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="68efe-111">Puntatore ai coefficienti SH di output: la funzione di base *Y* LM è archiviata in corrispondenza di *l*² + *m* + l.</span><span class="sxs-lookup"><span data-stu-id="68efe-111">Pointer to the output SH coefficients — the basis function *Y* ₗₘ is stored at *l*² + *m* + l.</span></span> <span data-ttu-id="68efe-112">L'ordine N determina la lunghezza della matrice, in cui devono essere sempre presenti coefficienti *n*².</span><span class="sxs-lookup"><span data-stu-id="68efe-112">The order N determines the length of the array, where there should always be *N*² coefficients.</span></span>

</dd> <dt>

<span data-ttu-id="68efe-113">*PF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68efe-113">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68efe-114">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="68efe-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="68efe-115">Coefficienti SH di input per la prima funzione.</span><span class="sxs-lookup"><span data-stu-id="68efe-115">Input SH coefficients for first function.</span></span>

</dd> <dt>

<span data-ttu-id="68efe-116">*PG* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68efe-116">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68efe-117">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="68efe-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="68efe-118">Secondo set di coefficienti SH di input.</span><span class="sxs-lookup"><span data-stu-id="68efe-118">Second set of input SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68efe-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68efe-119">Return value</span></span>

<span data-ttu-id="68efe-120">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="68efe-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="68efe-121">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="68efe-121">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="68efe-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="68efe-122">Remarks</span></span>

<span data-ttu-id="68efe-123">Il prodotto di due funzioni SH di order N = 5 genera una funzione SH di Order 2 × *N* -1 = 9, ma i risultati vengono troncati.</span><span class="sxs-lookup"><span data-stu-id="68efe-123">The product of two SH functions of order N = 5 generates an SH function of order 2 × *N* - 1 = 9, but the results are truncated.</span></span> <span data-ttu-id="68efe-124">Ciò significa che il prodotto si sposta ( *f* × *g*  =  *g* × *f* ) ma non associa ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).</span><span class="sxs-lookup"><span data-stu-id="68efe-124">This means that the product commutes ( *f* × *g* = *g* × *f* ) but doesn't associate ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).</span></span>

<span data-ttu-id="68efe-125">Questa funzione usa l'equazione seguente:</span><span class="sxs-lookup"><span data-stu-id="68efe-125">This function uses the following equation:</span></span>


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



<span data-ttu-id="68efe-126">dove y i \_ (s) è la funzione di base per i/o e dove f (s) e g (s) usano la funzione SH seguente:</span><span class="sxs-lookup"><span data-stu-id="68efe-126">where y\_i(s) is the ith SH basis function, and where f(s) and g(s) use the following SH function:</span></span>


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a><span data-ttu-id="68efe-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68efe-127">Requirements</span></span>



| <span data-ttu-id="68efe-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="68efe-128">Requirement</span></span> | <span data-ttu-id="68efe-129">Valore</span><span class="sxs-lookup"><span data-stu-id="68efe-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68efe-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68efe-130">Header</span></span><br/>  | <dl> <span data-ttu-id="68efe-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="68efe-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="68efe-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="68efe-132">Library</span></span><br/> | <dl> <span data-ttu-id="68efe-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68efe-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="68efe-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68efe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68efe-135">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="68efe-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
