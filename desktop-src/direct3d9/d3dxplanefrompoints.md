---
description: Costruisce un piano da tre punti.
ms.assetid: 13d5ce6b-0046-441b-b826-f34f4fe16979
title: Funzione D3DXPlaneFromPoints (D3dx9math. h)
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
ms.openlocfilehash: c537915c56cdbbfb33228b0c5a5ea3f2acc2baff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322100"
---
# <a name="d3dxplanefrompoints-function-d3dx9mathh"></a><span data-ttu-id="10d16-103">Funzione D3DXPlaneFromPoints (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="10d16-103">D3DXPlaneFromPoints function (D3dx9math.h)</span></span>

<span data-ttu-id="10d16-104">Costruisce un piano da tre punti.</span><span class="sxs-lookup"><span data-stu-id="10d16-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="10d16-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10d16-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="10d16-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="10d16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10d16-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="10d16-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="10d16-108">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="10d16-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="10d16-109">Puntatore alla struttura [**D3DXPLANE**](d3dxplane.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="10d16-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="10d16-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10d16-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10d16-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="10d16-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="10d16-112">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che definisce uno dei punti usati per costruire il piano.</span><span class="sxs-lookup"><span data-stu-id="10d16-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="10d16-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10d16-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10d16-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="10d16-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="10d16-115">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che definisce uno dei punti usati per costruire il piano.</span><span class="sxs-lookup"><span data-stu-id="10d16-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="10d16-116">*pV3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10d16-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10d16-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="10d16-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="10d16-118">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che definisce uno dei punti usati per costruire il piano.</span><span class="sxs-lookup"><span data-stu-id="10d16-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10d16-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10d16-119">Return value</span></span>

<span data-ttu-id="10d16-120">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="10d16-120">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="10d16-121">Puntatore alla struttura [**D3DXPLANE**](d3dxplane.md) costruita dai punti specificati.</span><span class="sxs-lookup"><span data-stu-id="10d16-121">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="10d16-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="10d16-122">Remarks</span></span>

<span data-ttu-id="10d16-123">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="10d16-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="10d16-124">In questo modo, la funzione **D3DXPlaneFromPoints** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="10d16-124">In this way, the **D3DXPlaneFromPoints** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="10d16-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10d16-125">Requirements</span></span>



| <span data-ttu-id="10d16-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="10d16-126">Requirement</span></span> | <span data-ttu-id="10d16-127">Valore</span><span class="sxs-lookup"><span data-stu-id="10d16-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10d16-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10d16-128">Header</span></span><br/>  | <dl> <span data-ttu-id="10d16-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="10d16-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="10d16-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="10d16-130">Library</span></span><br/> | <dl> <span data-ttu-id="10d16-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10d16-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="10d16-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10d16-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d16-133">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="10d16-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="10d16-134">**D3DXPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="10d16-134">**D3DXPlaneFromPointNormal**</span></span>](d3dxplanefrompointnormal.md)
</dt> </dl>

 

 




