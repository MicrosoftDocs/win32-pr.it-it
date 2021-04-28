---
description: 'Funzione D3DXMatrixMultiplyTranspose (D3dx9math.h): calcola il prodotto trasposto di due matrici.'
ms.assetid: 43927500-9413-41a4-a6ee-974d85dd1054
title: Funzione D3DXMatrixMultiplyTranspose (D3dx9math.h)
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
ms.openlocfilehash: 87aaa45e7a7a16884d17ab340f0bf1efeccd93bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107539"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx9mathh"></a><span data-ttu-id="db88f-103">Funzione D3DXMatrixMultiplyTranspose (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="db88f-103">D3DXMatrixMultiplyTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="db88f-104">Calcola il prodotto trasposto di due matrici.</span><span class="sxs-lookup"><span data-stu-id="db88f-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="db88f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db88f-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="db88f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="db88f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db88f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="db88f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="db88f-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="db88f-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="db88f-109">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="db88f-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="db88f-110">*pM1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="db88f-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db88f-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="db88f-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="db88f-112">Puntatore a una [**struttura D3DXMATRIX di**](d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="db88f-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="db88f-113">*pM2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="db88f-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db88f-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="db88f-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="db88f-115">Puntatore a una [**struttura D3DXMATRIX di**](d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="db88f-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db88f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db88f-116">Return value</span></span>

<span data-ttu-id="db88f-117">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="db88f-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="db88f-118">Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che è il prodotto di due matrici.</span><span class="sxs-lookup"><span data-stu-id="db88f-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="db88f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="db88f-119">Remarks</span></span>

<span data-ttu-id="db88f-120">Il risultato è il prodotto trasposto di due matrici di trasformazione, Out = T(M1 \* M2).</span><span class="sxs-lookup"><span data-stu-id="db88f-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="db88f-121">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="db88f-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="db88f-122">In questo modo, la **funzione D3DXMatrixMultiplyTranspose** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="db88f-122">In this way, the **D3DXMatrixMultiplyTranspose** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="db88f-123">Questa funzione è utile per impostare le matrici come costanti per vertici e pixel shader.</span><span class="sxs-lookup"><span data-stu-id="db88f-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="db88f-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db88f-124">Requirements</span></span>



| <span data-ttu-id="db88f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="db88f-125">Requirement</span></span> | <span data-ttu-id="db88f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="db88f-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db88f-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db88f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="db88f-128"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="db88f-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="db88f-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="db88f-129">Library</span></span><br/> | <dl> <span data-ttu-id="db88f-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="db88f-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="db88f-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db88f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db88f-132">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="db88f-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="db88f-133">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="db88f-133">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> <dt>

[<span data-ttu-id="db88f-134">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="db88f-134">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




