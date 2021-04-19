---
description: Determina il prodotto di due matrici.
ms.assetid: 160c801a-6589-4a0d-8e90-7e7a99fbd5f7
title: Funzione D3DXMatrixMultiply (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiply
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ea578f54d3f690f01d9280e840cb9ee039d0cdf0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322131"
---
# <a name="d3dxmatrixmultiply-function-d3dx9mathh"></a><span data-ttu-id="fc16c-103">Funzione D3DXMatrixMultiply (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="fc16c-103">D3DXMatrixMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="fc16c-104">Determina il prodotto di due matrici.</span><span class="sxs-lookup"><span data-stu-id="fc16c-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc16c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc16c-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="fc16c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc16c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc16c-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="fc16c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc16c-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc16c-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fc16c-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="fc16c-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fc16c-110">*pM1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc16c-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc16c-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fc16c-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fc16c-112">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="fc16c-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fc16c-113">*pM2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc16c-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc16c-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fc16c-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fc16c-115">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="fc16c-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc16c-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc16c-116">Return value</span></span>

<span data-ttu-id="fc16c-117">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc16c-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fc16c-118">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che è il prodotto di due matrici.</span><span class="sxs-lookup"><span data-stu-id="fc16c-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc16c-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc16c-119">Remarks</span></span>

<span data-ttu-id="fc16c-120">Il risultato rappresenta la trasformazione M1 seguita dalla trasformazione m2 (out = M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="fc16c-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="fc16c-121">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="fc16c-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fc16c-122">In questo modo, la funzione **D3DXMatrixMultiply** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="fc16c-122">In this way, the **D3DXMatrixMultiply** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc16c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc16c-123">Requirements</span></span>



| <span data-ttu-id="fc16c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc16c-124">Requirement</span></span> | <span data-ttu-id="fc16c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="fc16c-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc16c-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc16c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="fc16c-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc16c-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fc16c-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="fc16c-128">Library</span></span><br/> | <dl> <span data-ttu-id="fc16c-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc16c-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fc16c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc16c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc16c-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="fc16c-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fc16c-132">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="fc16c-132">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




