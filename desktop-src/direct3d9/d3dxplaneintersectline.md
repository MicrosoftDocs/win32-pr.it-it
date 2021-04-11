---
description: Trova l'intersezione tra un piano e una linea.
ms.assetid: 2723cd3e-fdc3-4aab-a089-0089e5b14e3e
title: Funzione D3DXPlaneIntersectLine (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b4a91a4592d039510e11147ffb680c880c43ccec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234937"
---
# <a name="d3dxplaneintersectline-function-d3dx9mathh"></a><span data-ttu-id="05179-103">Funzione D3DXPlaneIntersectLine (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="05179-103">D3DXPlaneIntersectLine function (D3dx9math.h)</span></span>

<span data-ttu-id="05179-104">Trova l'intersezione tra un piano e una linea.</span><span class="sxs-lookup"><span data-stu-id="05179-104">Finds the intersection between a plane and a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="05179-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05179-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="05179-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="05179-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05179-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="05179-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="05179-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="05179-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="05179-109">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che identifica l'intersezione tra il piano e la linea specificati.</span><span class="sxs-lookup"><span data-stu-id="05179-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, identifying the intersection between the specified plane and line.</span></span>

</dd> <dt>

<span data-ttu-id="05179-110">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05179-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05179-111">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="05179-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="05179-112">Puntatore alla struttura [**D3DXPLANE**](d3dxplane.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="05179-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="05179-113">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05179-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05179-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="05179-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="05179-115">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine, che definisce un punto di partenza della riga.</span><span class="sxs-lookup"><span data-stu-id="05179-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, defining a line starting point.</span></span>

</dd> <dt>

<span data-ttu-id="05179-116">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05179-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05179-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="05179-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="05179-118">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine, che definisce un punto finale di riga.</span><span class="sxs-lookup"><span data-stu-id="05179-118">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, defining a line ending point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05179-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="05179-119">Return value</span></span>

<span data-ttu-id="05179-120">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="05179-120">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="05179-121">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta l'intersezione tra il piano e la linea specificati.</span><span class="sxs-lookup"><span data-stu-id="05179-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the intersection between the specified plane and line.</span></span>

## <a name="remarks"></a><span data-ttu-id="05179-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="05179-122">Remarks</span></span>

<span data-ttu-id="05179-123">Se la riga è parallela al piano, viene restituito **null** .</span><span class="sxs-lookup"><span data-stu-id="05179-123">If the line is parallel to the plane, **NULL** is returned.</span></span>

<span data-ttu-id="05179-124">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="05179-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="05179-125">In questo modo, la funzione **D3DXPlaneIntersectLine** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="05179-125">In this way, the **D3DXPlaneIntersectLine** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="05179-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05179-126">Requirements</span></span>



| <span data-ttu-id="05179-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="05179-127">Requirement</span></span> | <span data-ttu-id="05179-128">Valore</span><span class="sxs-lookup"><span data-stu-id="05179-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05179-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="05179-129">Header</span></span><br/>  | <dl> <span data-ttu-id="05179-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="05179-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="05179-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="05179-131">Library</span></span><br/> | <dl> <span data-ttu-id="05179-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05179-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="05179-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05179-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05179-134">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="05179-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




