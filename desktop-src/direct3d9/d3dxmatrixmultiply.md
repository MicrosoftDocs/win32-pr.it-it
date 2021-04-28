---
description: 'Funzione D3DXMatrixMultiply (D3dx9math.h): determina il prodotto di due matrici.'
ms.assetid: 160c801a-6589-4a0d-8e90-7e7a99fbd5f7
title: Funzione D3DXMatrixMultiply (D3dx9math.h)
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
ms.openlocfilehash: 3d183fc3c79797bab886d3a40211448ccf57d552
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107549"
---
# <a name="d3dxmatrixmultiply-function-d3dx9mathh"></a><span data-ttu-id="03699-103">Funzione D3DXMatrixMultiply (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="03699-103">D3DXMatrixMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="03699-104">Determina il prodotto di due matrici.</span><span class="sxs-lookup"><span data-stu-id="03699-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="03699-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03699-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="03699-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="03699-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03699-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="03699-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="03699-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="03699-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="03699-109">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che è il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="03699-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="03699-110">*pM1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="03699-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03699-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="03699-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="03699-112">Puntatore a una [**struttura D3DXMATRIX di**](d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="03699-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="03699-113">*pM2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="03699-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03699-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="03699-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="03699-115">Puntatore a una [**struttura D3DXMATRIX di**](d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="03699-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03699-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03699-116">Return value</span></span>

<span data-ttu-id="03699-117">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="03699-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="03699-118">Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che è il prodotto di due matrici.</span><span class="sxs-lookup"><span data-stu-id="03699-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="03699-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="03699-119">Remarks</span></span>

<span data-ttu-id="03699-120">Il risultato rappresenta la trasformazione M1 seguita dalla trasformazione M2 (Out = M1 \* M2).</span><span class="sxs-lookup"><span data-stu-id="03699-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="03699-121">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="03699-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="03699-122">In questo modo, la **funzione D3DXMatrixMultiply** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="03699-122">In this way, the **D3DXMatrixMultiply** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="03699-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03699-123">Requirements</span></span>



| <span data-ttu-id="03699-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="03699-124">Requirement</span></span> | <span data-ttu-id="03699-125">Valore</span><span class="sxs-lookup"><span data-stu-id="03699-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03699-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03699-126">Header</span></span><br/>  | <dl> <span data-ttu-id="03699-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="03699-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="03699-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="03699-128">Library</span></span><br/> | <dl> <span data-ttu-id="03699-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="03699-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="03699-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03699-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03699-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="03699-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="03699-132">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="03699-132">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




