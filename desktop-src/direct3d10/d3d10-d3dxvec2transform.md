---
description: 'Funzione D3DXVec2Transform (D3DX10Math.h): trasforma un vettore 2D da una determinata matrice.'
ms.assetid: 4b57eb7f-fae9-48ac-a806-510da75d25a6
title: Funzione D3DXVec2Transform (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b1d8eed447b56e6f379ffe96cbbcb4820fbdaf14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108359"
---
# <a name="d3dxvec2transform-function-d3dx10mathh"></a><span data-ttu-id="455c5-103">Funzione D3DXVec2Transform (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="455c5-103">D3DXVec2Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="455c5-104">Trasforma un vettore 2D in base a una determinata matrice.</span><span class="sxs-lookup"><span data-stu-id="455c5-104">Transforms a 2D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="455c5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="455c5-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="455c5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="455c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="455c5-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="455c5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="455c5-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="455c5-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="455c5-109">Puntatore alla [**struttura D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="455c5-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="455c5-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="455c5-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="455c5-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="455c5-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="455c5-112">Puntatore all'oggetto [**D3DXVECTOR2 di origine.**](d3d10-d3dxvector2.md)</span><span class="sxs-lookup"><span data-stu-id="455c5-112">Pointer to the source [**D3DXVECTOR2**](d3d10-d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="455c5-113">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="455c5-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="455c5-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="455c5-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="455c5-115">Puntatore alla struttura [**D3DXMATRIX di**](d3d10-d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="455c5-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="455c5-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="455c5-116">Return value</span></span>

<span data-ttu-id="455c5-117">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="455c5-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="455c5-118">Puntatore a una struttura D3DXVECTOR4 che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="455c5-118">Pointer to a D3DXVECTOR4 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="455c5-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="455c5-119">Remarks</span></span>

<span data-ttu-id="455c5-120">Questa funzione trasforma il vettore pV (x, y, 0, 1) dalla matrice pM.</span><span class="sxs-lookup"><span data-stu-id="455c5-120">This function transforms the vector pV (x, y, 0, 1) by the matrix pM.</span></span>

<span data-ttu-id="455c5-121">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="455c5-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="455c5-122">In questo modo, la funzione D3DXVec2Transform può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="455c5-122">In this way, the D3DXVec2Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="455c5-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="455c5-123">Requirements</span></span>



| <span data-ttu-id="455c5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="455c5-124">Requirement</span></span> | <span data-ttu-id="455c5-125">Valore</span><span class="sxs-lookup"><span data-stu-id="455c5-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="455c5-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="455c5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="455c5-127"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="455c5-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="455c5-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="455c5-128">Library</span></span><br/> | <dl> <span data-ttu-id="455c5-129"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="455c5-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="455c5-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="455c5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="455c5-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="455c5-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
