---
description: 'Funzione D3DXVec2Transform (D3dx9math.h): trasforma un vettore 2D in base a una determinata matrice.'
ms.assetid: ccde9e34-2d99-4112-a8ed-3820d018b547
title: Funzione D3DXVec2Transform (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9b9b0f5ae0e3fda05cd8bdd92ee73b826f81b970
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097949"
---
# <a name="d3dxvec2transform-function-d3dx9mathh"></a><span data-ttu-id="f325b-103">Funzione D3DXVec2Transform (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="f325b-103">D3DXVec2Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="f325b-104">Trasforma un vettore 2D in base a una determinata matrice.</span><span class="sxs-lookup"><span data-stu-id="f325b-104">Transforms a 2D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f325b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f325b-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="f325b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f325b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f325b-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f325b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f325b-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="f325b-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f325b-109">Puntatore alla [**struttura D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f325b-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f325b-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f325b-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f325b-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="f325b-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f325b-112">Puntatore alla struttura [**D3DXVECTOR2 di**](d3dxvector2.md) origine.</span><span class="sxs-lookup"><span data-stu-id="f325b-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f325b-113">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f325b-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f325b-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f325b-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f325b-115">Puntatore alla struttura [**D3DXMATRIX di**](d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="f325b-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f325b-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f325b-116">Return value</span></span>

<span data-ttu-id="f325b-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="f325b-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f325b-118">Puntatore a [**una struttura D3DXVECTOR4**](d3dxvector4.md) che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="f325b-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="f325b-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="f325b-119">Remarks</span></span>

<span data-ttu-id="f325b-120">Questa funzione trasforma il vettore *pV* (x, y, 0, 1) dalla matrice *pM*.</span><span class="sxs-lookup"><span data-stu-id="f325b-120">This function transforms the vector *pV* (x, y, 0, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="f325b-121">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="f325b-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f325b-122">In questo modo, la **funzione D3DXVec2Transform** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="f325b-122">In this way, the **D3DXVec2Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f325b-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f325b-123">Requirements</span></span>



| <span data-ttu-id="f325b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f325b-124">Requirement</span></span> | <span data-ttu-id="f325b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f325b-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f325b-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f325b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f325b-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="f325b-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f325b-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="f325b-128">Library</span></span><br/> | <dl> <span data-ttu-id="f325b-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f325b-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f325b-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f325b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f325b-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="f325b-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f325b-132">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="f325b-132">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> <dt>

[<span data-ttu-id="f325b-133">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="f325b-133">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




