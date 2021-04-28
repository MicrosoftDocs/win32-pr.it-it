---
description: 'Funzione D3DXVec4Cross (D3dx9math.h): determina il prodotto incrociato in quattro dimensioni.'
ms.assetid: 10b965c9-7ed7-450c-86a0-114f068c888f
title: Funzione D3DXVec4Cross (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e3630a486f6c8fcd456373445bd931d878fdc38e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097689"
---
# <a name="d3dxvec4cross-function-d3dx9mathh"></a><span data-ttu-id="3f23d-103">Funzione D3DXVec4Cross (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="3f23d-103">D3DXVec4Cross function (D3dx9math.h)</span></span>

<span data-ttu-id="3f23d-104">Determina il prodotto incrociato in quattro dimensioni.</span><span class="sxs-lookup"><span data-stu-id="3f23d-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f23d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f23d-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="3f23d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f23d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f23d-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3f23d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f23d-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f23d-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="3f23d-109">Puntatore alla [**struttura D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3f23d-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3f23d-110">*pV1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3f23d-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f23d-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="3f23d-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="3f23d-112">Puntatore a una [**struttura D3DXVECTOR4 di**](d3dxvector4.md) origine.</span><span class="sxs-lookup"><span data-stu-id="3f23d-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3f23d-113">*pV2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3f23d-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f23d-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="3f23d-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="3f23d-115">Puntatore a una [**struttura D3DXVECTOR4 di**](d3dxvector4.md) origine.</span><span class="sxs-lookup"><span data-stu-id="3f23d-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3f23d-116">*pV3* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3f23d-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f23d-117">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="3f23d-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="3f23d-118">Puntatore a una [**struttura D3DXVECTOR4 di**](d3dxvector4.md) origine.</span><span class="sxs-lookup"><span data-stu-id="3f23d-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f23d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f23d-119">Return value</span></span>

<span data-ttu-id="3f23d-120">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f23d-120">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="3f23d-121">Puntatore a [**una struttura D3DXVECTOR4**](d3dxvector4.md) che rappresenta il prodotto incrociato.</span><span class="sxs-lookup"><span data-stu-id="3f23d-121">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f23d-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f23d-122">Remarks</span></span>

<span data-ttu-id="3f23d-123">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="3f23d-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="3f23d-124">In questo modo, la **funzione D3DXVec4Cross** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="3f23d-124">In this way, the **D3DXVec4Cross** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f23d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f23d-125">Requirements</span></span>



| <span data-ttu-id="3f23d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f23d-126">Requirement</span></span> | <span data-ttu-id="3f23d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="3f23d-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f23d-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f23d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3f23d-129"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="3f23d-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3f23d-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="3f23d-130">Library</span></span><br/> | <dl> <span data-ttu-id="3f23d-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f23d-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3f23d-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f23d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f23d-133">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="3f23d-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="3f23d-134">**D3DXVec4Dot**</span><span class="sxs-lookup"><span data-stu-id="3f23d-134">**D3DXVec4Dot**</span></span>](d3dxvec4dot.md)
</dt> </dl>

 

 




