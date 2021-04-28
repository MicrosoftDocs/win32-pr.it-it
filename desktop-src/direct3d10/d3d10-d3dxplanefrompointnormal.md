---
description: 'Funzione D3DXPlaneFromPointNormal (D3DX10Math.h): costruisce un piano da un punto e da un normale.'
ms.assetid: 93c644d2-ab8c-47a1-9a3b-8b9c6a13178b
title: Funzione D3DXPlaneFromPointNormal (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 519ce82a8d5a8c6adaf22b69047a8d365bd777ac
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108839"
---
# <a name="d3dxplanefrompointnormal-function-d3dx10mathh"></a><span data-ttu-id="c4833-103">Funzione D3DXPlaneFromPointNormal (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="c4833-103">D3DXPlaneFromPointNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="c4833-104">Costruisce un piano da un punto e da un normale.</span><span class="sxs-lookup"><span data-stu-id="c4833-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4833-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4833-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="c4833-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4833-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4833-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c4833-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4833-108">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="c4833-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="c4833-109">Puntatore [**all'oggetto D3DXPLANE**](d3d10-d3dxplane.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c4833-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c4833-110">*pPoint* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c4833-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4833-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c4833-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c4833-112">Puntatore a [**un oggetto D3DXVECTOR3,**](d3d10-d3dxvector3.md)che definisce il punto usato per costruire il piano.</span><span class="sxs-lookup"><span data-stu-id="c4833-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="c4833-113">*pNormal* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c4833-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4833-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c4833-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c4833-115">Puntatore a una struttura D3DXVECTOR3, che definisce la normale usata per costruire il piano.</span><span class="sxs-lookup"><span data-stu-id="c4833-115">Pointer to a D3DXVECTOR3 structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4833-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4833-116">Return value</span></span>

<span data-ttu-id="c4833-117">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="c4833-117">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="c4833-118">Puntatore alla struttura D3DXPLANE costruita dal punto e dalla normale.</span><span class="sxs-lookup"><span data-stu-id="c4833-118">Pointer to the D3DXPLANE structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4833-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4833-119">Remarks</span></span>

<span data-ttu-id="c4833-120">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="c4833-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c4833-121">In questo modo, la funzione D3DXPlaneFromPointNormal può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="c4833-121">In this way, the D3DXPlaneFromPointNormal function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4833-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4833-122">Requirements</span></span>



| <span data-ttu-id="c4833-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4833-123">Requirement</span></span> | <span data-ttu-id="c4833-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c4833-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4833-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4833-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c4833-126"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c4833-126"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="c4833-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4833-127">Library</span></span><br/> | <dl> <span data-ttu-id="c4833-128"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4833-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c4833-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4833-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4833-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="c4833-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
