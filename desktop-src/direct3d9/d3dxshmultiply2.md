---
description: Calcola il prodotto di due funzioni rappresentate mediante SH (f e g).
ms.assetid: 632400a4-2ac9-438d-85f7-869101f350c8
title: Funzione D3DXSHMultiply2 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
- D3DXSHMultiply3
- D3DXSHMultiply4
- D3DXSHMultiply5
- D3DXSHMultiply6
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: f7b9adaf5caf7b4b2d35035fd5c2a916298b0c8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322474"
---
# <a name="d3dxshmultiply2-function-d3dx9mathh"></a><span data-ttu-id="8447c-103">Funzione D3DXSHMultiply2 (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="8447c-103">D3DXSHMultiply2 function (D3dx9math.h)</span></span>

<span data-ttu-id="8447c-104">Calcola il prodotto di due funzioni rappresentate mediante SH (f e g).</span><span class="sxs-lookup"><span data-stu-id="8447c-104">Computes the product of two functions represented using SH (f and g).</span></span>

## <a name="syntax"></a><span data-ttu-id="8447c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8447c-105">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply2(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="8447c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8447c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8447c-107">*broncio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8447c-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8447c-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8447c-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8447c-109">Puntatore ai coefficienti SH di output. la funzione di base YLM è archiviata a l \* l + m + l.</span><span class="sxs-lookup"><span data-stu-id="8447c-109">Pointer to the output SH coefficients - basis function Ylm is stored at l\*l + m+l.</span></span>

</dd> <dt>

<span data-ttu-id="8447c-110">*PF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8447c-110">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8447c-111">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="8447c-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8447c-112">Input SH coeffs per la prima funzione.</span><span class="sxs-lookup"><span data-stu-id="8447c-112">Input SH coeffs for first function.</span></span>

</dd> <dt>

<span data-ttu-id="8447c-113">*PG* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8447c-113">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8447c-114">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="8447c-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8447c-115">Secondo set di input SH coeffs.</span><span class="sxs-lookup"><span data-stu-id="8447c-115">Second set of input SH coeffs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8447c-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8447c-116">Return value</span></span>

<span data-ttu-id="8447c-117">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8447c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8447c-118">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="8447c-118">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="8447c-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="8447c-119">Remarks</span></span>

<span data-ttu-id="8447c-120">L'ordine è un numero compreso tra 2 e 6 inclusi.</span><span class="sxs-lookup"><span data-stu-id="8447c-120">The order is a number between 2 and 6 inclusive.</span></span> <span data-ttu-id="8447c-121">Quindi, in questa pagina vengono effettivamente documentate diverse funzioni: D3DXSHMultiply2, D3DXSHMultiply3,... D3DXSHMultiply6.</span><span class="sxs-lookup"><span data-stu-id="8447c-121">So this page actually documents several functions: D3DXSHMultiply2, D3DXSHMultiply3, ... D3DXSHMultiply6.</span></span>

<span data-ttu-id="8447c-122">Calcola il prodotto di due funzioni rappresentate usando SH (f e g), dove *broncio* \[ i \] = int (y \_ i (s) f/s) \* \* , dove y \_ i/o è la funzione di base SH, f (s) e g/s sono funzioni SH (Sum \_ i (y i \_ \* \_ /sec)).</span><span class="sxs-lookup"><span data-stu-id="8447c-122">Computes the product of two functions represented using SH (f and g), where *pOut*\[i\] = int(y\_i(s) \* f(s) \* g(s)), where y\_i(s) is the ith SH basis function, f(s) and g(s) are SH functions (sum\_i(y\_i(s)\*c\_i)).</span></span> <span data-ttu-id="8447c-123">L'ordine O determina le lunghezze delle matrici, in cui devono essere sempre presenti coefficienti O ^ 2.</span><span class="sxs-lookup"><span data-stu-id="8447c-123">The order O determines the lengths of the arrays, where there should always be O^2 coefficients.</span></span> <span data-ttu-id="8447c-124">In generale, il prodotto di due funzioni SH dell'ordine O genera una funzione SH dell'ordine 2 \* O-1, ma i risultati vengono troncati.</span><span class="sxs-lookup"><span data-stu-id="8447c-124">In general the product of two SH functions of order O generates an SH function of order 2\*O - 1, but the results are truncated.</span></span> <span data-ttu-id="8447c-125">Ciò significa che il prodotto si sposta (f \* g = = g \* f) ma non associa (f \* (g \* h)! = (f \* g) \* h.</span><span class="sxs-lookup"><span data-stu-id="8447c-125">This means that the product commutes (f\*g == g\*f) but doesn't associate (f\*(g\*h) != (f\*g)\*h.</span></span>

## <a name="requirements"></a><span data-ttu-id="8447c-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8447c-126">Requirements</span></span>



| <span data-ttu-id="8447c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8447c-127">Requirement</span></span> | <span data-ttu-id="8447c-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8447c-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8447c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8447c-129">Header</span></span><br/> | <dl> <span data-ttu-id="8447c-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8447c-130"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8447c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8447c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8447c-132">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="8447c-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
