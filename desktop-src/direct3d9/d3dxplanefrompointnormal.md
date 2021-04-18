---
description: Costruisce un piano da un punto e da un normale.
ms.assetid: af396bbb-09b7-492f-a25f-9c950da7e605
title: Funzione D3DXPlaneFromPointNormal (D3dx9math. h)
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
ms.openlocfilehash: 8eeb8ea3a1725e0bf615be888d8e862c97730a2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322099"
---
# <a name="d3dxplanefrompointnormal-function-d3dx9mathh"></a><span data-ttu-id="829ec-103">Funzione D3DXPlaneFromPointNormal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="829ec-103">D3DXPlaneFromPointNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="829ec-104">Costruisce un piano da un punto e da un normale.</span><span class="sxs-lookup"><span data-stu-id="829ec-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="829ec-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="829ec-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="829ec-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="829ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="829ec-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="829ec-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="829ec-108">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="829ec-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="829ec-109">Puntatore alla struttura [**D3DXPLANE**](d3dxplane.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="829ec-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="829ec-110">*pPoint* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="829ec-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="829ec-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="829ec-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="829ec-112">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che definisce il punto usato per costruire il piano.</span><span class="sxs-lookup"><span data-stu-id="829ec-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="829ec-113">*pNormal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="829ec-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="829ec-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="829ec-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="829ec-115">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che definisce il normale utilizzato per costruire il piano.</span><span class="sxs-lookup"><span data-stu-id="829ec-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="829ec-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="829ec-116">Return value</span></span>

<span data-ttu-id="829ec-117">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="829ec-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="829ec-118">Puntatore alla struttura [**D3DXPLANE**](d3dxplane.md) costruita dal punto e dal normale.</span><span class="sxs-lookup"><span data-stu-id="829ec-118">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="829ec-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="829ec-119">Remarks</span></span>

<span data-ttu-id="829ec-120">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="829ec-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="829ec-121">In questo modo, la funzione **D3DXPlaneFromPointNormal** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="829ec-121">In this way, the **D3DXPlaneFromPointNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="829ec-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="829ec-122">Requirements</span></span>



| <span data-ttu-id="829ec-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="829ec-123">Requirement</span></span> | <span data-ttu-id="829ec-124">Valore</span><span class="sxs-lookup"><span data-stu-id="829ec-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="829ec-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="829ec-125">Header</span></span><br/>  | <dl> <span data-ttu-id="829ec-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="829ec-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="829ec-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="829ec-127">Library</span></span><br/> | <dl> <span data-ttu-id="829ec-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="829ec-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="829ec-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="829ec-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="829ec-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="829ec-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="829ec-131">**D3DXPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="829ec-131">**D3DXPlaneFromPoints**</span></span>](d3dxplanefrompoints.md)
</dt> </dl>

 

 




