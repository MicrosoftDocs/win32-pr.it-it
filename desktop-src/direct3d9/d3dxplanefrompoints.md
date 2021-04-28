---
description: 'Funzione D3DXPlaneFromPoints (D3dx9math.h): costruisce un piano da tre punti.'
ms.assetid: 13d5ce6b-0046-441b-b826-f34f4fe16979
title: Funzione D3DXPlaneFromPoints (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0d945dff9c124f4c66cea4f9d61c490c6eaf7a66
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094159"
---
# <a name="d3dxplanefrompoints-function-d3dx9mathh"></a><span data-ttu-id="899bd-103">Funzione D3DXPlaneFromPoints (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="899bd-103">D3DXPlaneFromPoints function (D3dx9math.h)</span></span>

<span data-ttu-id="899bd-104">Costruisce un piano da tre punti.</span><span class="sxs-lookup"><span data-stu-id="899bd-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="899bd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="899bd-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="899bd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="899bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="899bd-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="899bd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="899bd-108">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="899bd-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="899bd-109">Puntatore alla [**struttura D3DXPLANE**](d3dxplane.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="899bd-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="899bd-110">*pV1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="899bd-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="899bd-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="899bd-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="899bd-112">Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che definisce uno dei punti usati per costruire il piano.</span><span class="sxs-lookup"><span data-stu-id="899bd-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="899bd-113">*pV2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="899bd-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="899bd-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="899bd-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="899bd-115">Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che definisce uno dei punti usati per costruire il piano.</span><span class="sxs-lookup"><span data-stu-id="899bd-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="899bd-116">*pV3* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="899bd-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="899bd-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="899bd-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="899bd-118">Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che definisce uno dei punti usati per costruire il piano.</span><span class="sxs-lookup"><span data-stu-id="899bd-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="899bd-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="899bd-119">Return value</span></span>

<span data-ttu-id="899bd-120">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="899bd-120">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="899bd-121">Puntatore alla [**struttura D3DXPLANE**](d3dxplane.md) costruita dai punti dati.</span><span class="sxs-lookup"><span data-stu-id="899bd-121">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="899bd-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="899bd-122">Remarks</span></span>

<span data-ttu-id="899bd-123">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="899bd-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="899bd-124">In questo modo, la **funzione D3DXPlaneFromPoints** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="899bd-124">In this way, the **D3DXPlaneFromPoints** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="899bd-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="899bd-125">Requirements</span></span>



| <span data-ttu-id="899bd-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="899bd-126">Requirement</span></span> | <span data-ttu-id="899bd-127">Valore</span><span class="sxs-lookup"><span data-stu-id="899bd-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="899bd-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="899bd-128">Header</span></span><br/>  | <dl> <span data-ttu-id="899bd-129"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="899bd-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="899bd-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="899bd-130">Library</span></span><br/> | <dl> <span data-ttu-id="899bd-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="899bd-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="899bd-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="899bd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="899bd-133">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="899bd-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="899bd-134">**D3DXPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="899bd-134">**D3DXPlaneFromPointNormal**</span></span>](d3dxplanefrompointnormal.md)
</dt> </dl>

 

 




