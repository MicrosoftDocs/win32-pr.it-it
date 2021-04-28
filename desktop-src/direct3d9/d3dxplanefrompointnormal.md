---
description: 'Funzione D3DXPlaneFromPointNormal (D3dx9math.h): costruisce un piano da un punto e da un normale.'
ms.assetid: af396bbb-09b7-492f-a25f-9c950da7e605
title: Funzione D3DXPlaneFromPointNormal (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e34765d150932d6a7b3b0293e603237ffb2b45ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098089"
---
# <a name="d3dxplanefrompointnormal-function-d3dx9mathh"></a><span data-ttu-id="ec2f3-103">Funzione D3DXPlaneFromPointNormal (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="ec2f3-103">D3DXPlaneFromPointNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="ec2f3-104">Costruisce un piano da un punto e da un normale.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec2f3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec2f3-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="ec2f3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec2f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec2f3-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ec2f3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2f3-108">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="ec2f3-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="ec2f3-109">Puntatore alla [**struttura D3DXPLANE**](d3dxplane.md) che è il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ec2f3-110">*pPoint* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="ec2f3-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2f3-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ec2f3-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ec2f3-112">Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che definisce il punto usato per costruire il piano.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="ec2f3-113">*pNormal* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="ec2f3-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2f3-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ec2f3-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ec2f3-115">Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che definisce la normale usata per costruire il piano.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec2f3-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec2f3-116">Return value</span></span>

<span data-ttu-id="ec2f3-117">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="ec2f3-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="ec2f3-118">Puntatore alla [**struttura D3DXPLANE**](d3dxplane.md) costruita dal punto e dalla normale.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-118">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec2f3-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec2f3-119">Remarks</span></span>

<span data-ttu-id="ec2f3-120">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="ec2f3-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ec2f3-121">In questo modo, la **funzione D3DXPlaneFromPointNormal** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-121">In this way, the **D3DXPlaneFromPointNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec2f3-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec2f3-122">Requirements</span></span>



| <span data-ttu-id="ec2f3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec2f3-123">Requirement</span></span> | <span data-ttu-id="ec2f3-124">Valore</span><span class="sxs-lookup"><span data-stu-id="ec2f3-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec2f3-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec2f3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ec2f3-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="ec2f3-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ec2f3-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="ec2f3-127">Library</span></span><br/> | <dl> <span data-ttu-id="ec2f3-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec2f3-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ec2f3-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec2f3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec2f3-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="ec2f3-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ec2f3-131">**D3DXPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="ec2f3-131">**D3DXPlaneFromPoints**</span></span>](d3dxplanefrompoints.md)
</dt> </dl>

 

 




