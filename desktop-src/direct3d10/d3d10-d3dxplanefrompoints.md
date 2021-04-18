---
description: Costruisce un piano da tre punti.
ms.assetid: 0e77af1b-cedf-482c-8398-10becb398a2c
title: Funzione D3DXPlaneFromPoints (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPoints
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eed4426492f05b2bfe3c762915edb8fdc21dc789
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323392"
---
# <a name="d3dxplanefrompoints-function-d3dx10mathh"></a><span data-ttu-id="27cdf-103">Funzione D3DXPlaneFromPoints (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="27cdf-103">D3DXPlaneFromPoints function (D3DX10Math.h)</span></span>

<span data-ttu-id="27cdf-104">Costruisce un piano da tre punti.</span><span class="sxs-lookup"><span data-stu-id="27cdf-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="27cdf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27cdf-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="27cdf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="27cdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27cdf-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="27cdf-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="27cdf-108">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="27cdf-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="27cdf-109">Puntatore a [**D3DXPLANE**](d3d10-d3dxplane.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="27cdf-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="27cdf-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27cdf-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27cdf-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="27cdf-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="27cdf-112">Puntatore a un [**D3DXVECTOR3**](d3d10-d3dxvector3.md), che definisce uno dei punti usati per costruire il piano.</span><span class="sxs-lookup"><span data-stu-id="27cdf-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="27cdf-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27cdf-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27cdf-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="27cdf-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="27cdf-115">Puntatore a una struttura D3DXVECTOR3, che definisce uno dei punti usati per costruire il piano.</span><span class="sxs-lookup"><span data-stu-id="27cdf-115">Pointer to a D3DXVECTOR3 structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="27cdf-116">*pV3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27cdf-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27cdf-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="27cdf-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="27cdf-118">Puntatore a una struttura D3DXVECTOR3, che definisce uno dei punti usati per costruire il piano.</span><span class="sxs-lookup"><span data-stu-id="27cdf-118">Pointer to a D3DXVECTOR3 structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27cdf-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27cdf-119">Return value</span></span>

<span data-ttu-id="27cdf-120">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="27cdf-120">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="27cdf-121">Puntatore alla struttura D3DXPLANE costruita dai punti specificati.</span><span class="sxs-lookup"><span data-stu-id="27cdf-121">Pointer to the D3DXPLANE structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="27cdf-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="27cdf-122">Remarks</span></span>

<span data-ttu-id="27cdf-123">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="27cdf-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="27cdf-124">In questo modo, la funzione D3DXPlaneFromPoints può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="27cdf-124">In this way, the D3DXPlaneFromPoints function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="27cdf-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27cdf-125">Requirements</span></span>



| <span data-ttu-id="27cdf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="27cdf-126">Requirement</span></span> | <span data-ttu-id="27cdf-127">Valore</span><span class="sxs-lookup"><span data-stu-id="27cdf-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27cdf-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27cdf-128">Header</span></span><br/>  | <dl> <span data-ttu-id="27cdf-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="27cdf-129"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="27cdf-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="27cdf-130">Library</span></span><br/> | <dl> <span data-ttu-id="27cdf-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27cdf-131"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="27cdf-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27cdf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27cdf-133">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="27cdf-133">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
