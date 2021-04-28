---
description: 'Funzione D3DXPlaneNormalize (D3DX10Math.h): normalizza i coefficienti del piano in modo che la normale del piano abbia lunghezza unità.'
ms.assetid: 52ae36a7-e37b-457a-9832-e62900a85bde
title: Funzione D3DXPlaneNormalize (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneNormalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8b3499297a008b0d8f5dc705080bbd1d5bbe3af4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103309"
---
# <a name="d3dxplanenormalize-function-d3dx10mathh"></a><span data-ttu-id="09bdc-103">Funzione D3DXPlaneNormalize (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="09bdc-103">D3DXPlaneNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="09bdc-104">Normalizza i coefficienti del piano in modo che la normale del piano abbia lunghezza unità.</span><span class="sxs-lookup"><span data-stu-id="09bdc-104">Normalizes the plane coefficients so that the plane normal has unit length.</span></span>

## <a name="syntax"></a><span data-ttu-id="09bdc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09bdc-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a><span data-ttu-id="09bdc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="09bdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09bdc-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="09bdc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="09bdc-108">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="09bdc-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="09bdc-109">Puntatore [**all'oggetto D3DXPLANE**](d3d10-d3dxplane.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="09bdc-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="09bdc-110">*pP* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="09bdc-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09bdc-111">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="09bdc-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="09bdc-112">Puntatore alla struttura D3DXPLANE di origine.</span><span class="sxs-lookup"><span data-stu-id="09bdc-112">Pointer to the source D3DXPLANE structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09bdc-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09bdc-113">Return value</span></span>

<span data-ttu-id="09bdc-114">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="09bdc-114">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="09bdc-115">Puntatore a una struttura D3DXPLANE che rappresenta la normale del piano.</span><span class="sxs-lookup"><span data-stu-id="09bdc-115">Pointer to a D3DXPLANE structure that represents the normal of the plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="09bdc-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="09bdc-116">Remarks</span></span>

<span data-ttu-id="09bdc-117">Questa funzione normalizza un piano in modo che \| a,b,c \| == 1.</span><span class="sxs-lookup"><span data-stu-id="09bdc-117">This function normalizes a plane so that \|a,b,c\| == 1.</span></span>

<span data-ttu-id="09bdc-118">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="09bdc-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="09bdc-119">In questo modo, questa funzione può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="09bdc-119">In this way, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="09bdc-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09bdc-120">Requirements</span></span>



| <span data-ttu-id="09bdc-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="09bdc-121">Requirement</span></span> | <span data-ttu-id="09bdc-122">Valore</span><span class="sxs-lookup"><span data-stu-id="09bdc-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09bdc-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09bdc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="09bdc-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="09bdc-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="09bdc-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="09bdc-125">Library</span></span><br/> | <dl> <span data-ttu-id="09bdc-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="09bdc-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="09bdc-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09bdc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09bdc-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="09bdc-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
