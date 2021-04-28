---
description: "Funzione D3DXPlaneIntersectLine (D3DX10Math.h): trova l'intersezione tra un piano e una linea."
ms.assetid: aea1c4e1-f8c0-46df-bb33-2b517396d69e
title: Funzione D3DXPlaneIntersectLine (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1d32bb312c97b793f492f7a29bebe11529b79cf9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108809"
---
# <a name="d3dxplaneintersectline-function-d3dx10mathh"></a><span data-ttu-id="a0297-103">Funzione D3DXPlaneIntersectLine (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="a0297-103">D3DXPlaneIntersectLine function (D3DX10Math.h)</span></span>

<span data-ttu-id="a0297-104">Trova l'intersezione tra un piano e una linea.</span><span class="sxs-lookup"><span data-stu-id="a0297-104">Finds the intersection between a plane and a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0297-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0297-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="a0297-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0297-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0297-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a0297-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0297-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0297-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a0297-109">Puntatore a [**un oggetto D3DXVECTOR3**](d3d10-d3dxvector3.md)che identifica l'intersezione tra il piano e la linea specificati.</span><span class="sxs-lookup"><span data-stu-id="a0297-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identifying the intersection between the specified plane and line.</span></span>

</dd> <dt>

<span data-ttu-id="a0297-110">*pP* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a0297-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0297-111">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="a0297-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="a0297-112">Puntatore [**all'oggetto D3DXPLANE di origine.**](d3d10-d3dxplane.md)</span><span class="sxs-lookup"><span data-stu-id="a0297-112">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0297-113">*pV1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a0297-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0297-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a0297-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a0297-115">Puntatore a una struttura D3DXVECTOR3 di origine, che definisce un punto di partenza della linea.</span><span class="sxs-lookup"><span data-stu-id="a0297-115">Pointer to a source D3DXVECTOR3 structure, defining a line starting point.</span></span>

</dd> <dt>

<span data-ttu-id="a0297-116">*pV2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a0297-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0297-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a0297-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a0297-118">Puntatore a una struttura D3DXVECTOR3 di origine, che definisce un punto finale della riga.</span><span class="sxs-lookup"><span data-stu-id="a0297-118">Pointer to a source D3DXVECTOR3 structure, defining a line ending point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0297-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0297-119">Return value</span></span>

<span data-ttu-id="a0297-120">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0297-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a0297-121">Puntatore a una struttura D3DXVECTOR3 che rappresenta l'intersezione tra il piano e la linea specificati.</span><span class="sxs-lookup"><span data-stu-id="a0297-121">Pointer to a D3DXVECTOR3 structure that is the intersection between the specified plane and line.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0297-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0297-122">Remarks</span></span>

<span data-ttu-id="a0297-123">Se la linea è parallela al piano, **viene restituito NULL.**</span><span class="sxs-lookup"><span data-stu-id="a0297-123">If the line is parallel to the plane, **NULL** is returned.</span></span>

<span data-ttu-id="a0297-124">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="a0297-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a0297-125">In questo modo, la funzione D3DXPlaneIntersectLine può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="a0297-125">In this way, the D3DXPlaneIntersectLine function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0297-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0297-126">Requirements</span></span>



| <span data-ttu-id="a0297-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0297-127">Requirement</span></span> | <span data-ttu-id="a0297-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a0297-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0297-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0297-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a0297-130"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="a0297-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="a0297-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0297-131">Library</span></span><br/> | <dl> <span data-ttu-id="a0297-132"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0297-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a0297-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0297-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0297-134">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="a0297-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
