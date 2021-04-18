---
description: Restituisce il componente z prendendo il prodotto incrociato di due vettori 2D.
ms.assetid: daec19f2-cd0f-4a68-affc-9a42bda8912c
title: Funzione D3DXVec2CCW (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CCW
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71c6e14171a9e7d12d86c30f05885cecf50ce973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322565"
---
# <a name="d3dxvec2ccw-function"></a><span data-ttu-id="e1922-103">D3DXVec2CCW (funzione)</span><span class="sxs-lookup"><span data-stu-id="e1922-103">D3DXVec2CCW function</span></span>

<span data-ttu-id="e1922-104">Restituisce il componente z prendendo il prodotto incrociato di due vettori 2D.</span><span class="sxs-lookup"><span data-stu-id="e1922-104">Returns the z-component by taking the cross product of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1922-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1922-105">Syntax</span></span>


```C++
FLOAT D3DXVec2CCW(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="e1922-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1922-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1922-107">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1922-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1922-108">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="e1922-108">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e1922-109">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="e1922-109">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e1922-110">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1922-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1922-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="e1922-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e1922-112">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="e1922-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1922-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1922-113">Return value</span></span>

<span data-ttu-id="e1922-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1922-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1922-115">Componente z.</span><span class="sxs-lookup"><span data-stu-id="e1922-115">The z-component.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1922-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1922-116">Remarks</span></span>

<span data-ttu-id="e1922-117">Questa funzione determina il componente z determinando il prodotto incrociato in base alla formula seguente: ((x1, Y1, 0) Cross (X2, Y2, 0)).</span><span class="sxs-lookup"><span data-stu-id="e1922-117">This function determines the z-component by determining the cross-product based on the following formula: ((x1,y1,0) cross (x2,y2,0)).</span></span> <span data-ttu-id="e1922-118">O come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="e1922-118">Or as shown in the following example.</span></span>


```
pV1->x * pV2->y - pV1->y * pV2->x
```



<span data-ttu-id="e1922-119">Se il valore del componente z è positivo, il vettore V2 è in senso antiorario rispetto al vettore v1.</span><span class="sxs-lookup"><span data-stu-id="e1922-119">If the value of the z-component is positive, the vector V2 is counterclockwise from the vector V1.</span></span> <span data-ttu-id="e1922-120">Queste informazioni sono utili per l'abbattimento del back-face.</span><span class="sxs-lookup"><span data-stu-id="e1922-120">This information is useful for back-face culling.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1922-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1922-121">Requirements</span></span>



| <span data-ttu-id="e1922-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1922-122">Requirement</span></span> | <span data-ttu-id="e1922-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e1922-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1922-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1922-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e1922-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1922-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e1922-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="e1922-126">Library</span></span><br/> | <dl> <span data-ttu-id="e1922-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1922-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e1922-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1922-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1922-129">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="e1922-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e1922-130">**D3DXVec2Dot**</span><span class="sxs-lookup"><span data-stu-id="e1922-130">**D3DXVec2Dot**</span></span>](d3dxvec2dot.md)
</dt> </dl>

 

 
