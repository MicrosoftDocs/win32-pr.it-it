---
description: Calcola il prodotto trasposto di due matrici.
ms.assetid: 43927500-9413-41a4-a6ee-974d85dd1054
title: Funzione D3DXMatrixMultiplyTranspose (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiplyTranspose
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b599453ae108a5a8bab8ee896858760c85799948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322128"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx9mathh"></a><span data-ttu-id="cb6e7-103">Funzione D3DXMatrixMultiplyTranspose (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="cb6e7-103">D3DXMatrixMultiplyTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="cb6e7-104">Calcola il prodotto trasposto di due matrici.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb6e7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb6e7-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="cb6e7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb6e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb6e7-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="cb6e7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb6e7-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="cb6e7-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cb6e7-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="cb6e7-110">*pM1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb6e7-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb6e7-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="cb6e7-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cb6e7-112">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cb6e7-113">*pM2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb6e7-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb6e7-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="cb6e7-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cb6e7-115">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb6e7-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb6e7-116">Return value</span></span>

<span data-ttu-id="cb6e7-117">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="cb6e7-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cb6e7-118">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che è il prodotto di due matrici.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb6e7-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb6e7-119">Remarks</span></span>

<span data-ttu-id="cb6e7-120">Il risultato è l'oggetto trasposto dal prodotto di due matrici di trasformazione, out = T (M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="cb6e7-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="cb6e7-121">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="cb6e7-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="cb6e7-122">In questo modo, la funzione **D3DXMatrixMultiplyTranspose** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-122">In this way, the **D3DXMatrixMultiplyTranspose** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="cb6e7-123">Questa funzione è utile per impostare matrici come costanti per i vertex e i pixel shader.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb6e7-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb6e7-124">Requirements</span></span>



| <span data-ttu-id="cb6e7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb6e7-125">Requirement</span></span> | <span data-ttu-id="cb6e7-126">Valore</span><span class="sxs-lookup"><span data-stu-id="cb6e7-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb6e7-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb6e7-127">Header</span></span><br/>  | <dl> <span data-ttu-id="cb6e7-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb6e7-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="cb6e7-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="cb6e7-129">Library</span></span><br/> | <dl> <span data-ttu-id="cb6e7-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb6e7-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cb6e7-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb6e7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb6e7-132">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="cb6e7-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="cb6e7-133">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="cb6e7-133">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> <dt>

[<span data-ttu-id="cb6e7-134">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="cb6e7-134">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




