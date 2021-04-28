---
description: 'Funzione D3DXVec3Transform (D3DX10Math.h): trasforma il vettore (x, y, z, 1) in base a una determinata matrice.'
ms.assetid: 88b26d94-2550-4126-bf91-b06391ec5c75
title: Funzione D3DXVec3Transform (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Transform
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 9b5cd69ce603f56e4837818cac6ee18fe3ab1e53
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108139"
---
# <a name="d3dxvec3transform-function-d3dx10mathh"></a><span data-ttu-id="08244-103">Funzione D3DXVec3Transform (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="08244-103">D3DXVec3Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="08244-104">Trasforma il vettore (x, y, z, 1) in base a una determinata matrice.</span><span class="sxs-lookup"><span data-stu-id="08244-104">Transforms vector (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="08244-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08244-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="08244-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="08244-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08244-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="08244-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="08244-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="08244-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="08244-109">Puntatore alla [**struttura D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="08244-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="08244-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="08244-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08244-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="08244-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="08244-112">Puntatore all'oggetto [**D3DXVECTOR3 di origine.**](d3d10-d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="08244-112">Pointer to the source [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="08244-113">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="08244-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08244-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="08244-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="08244-115">Puntatore alla struttura [**D3DXMATRIX di**](d3d10-d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="08244-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08244-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08244-116">Return value</span></span>

<span data-ttu-id="08244-117">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="08244-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="08244-118">Puntatore a una struttura D3DXVECTOR4 che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="08244-118">Pointer to a D3DXVECTOR4 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="08244-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="08244-119">Remarks</span></span>

<span data-ttu-id="08244-120">Questa funzione trasforma il vettore, pV (x, y, z, 1), in base alla matrice pM.</span><span class="sxs-lookup"><span data-stu-id="08244-120">This function transforms the vector, pV (x, y, z, 1), by the matrix pM.</span></span>

<span data-ttu-id="08244-121">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="08244-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="08244-122">In questo modo, la funzione D3DXVec3Transform può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="08244-122">In this way, the D3DXVec3Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="08244-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08244-123">Requirements</span></span>



| <span data-ttu-id="08244-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="08244-124">Requirement</span></span> | <span data-ttu-id="08244-125">Valore</span><span class="sxs-lookup"><span data-stu-id="08244-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08244-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08244-126">Header</span></span><br/> | <dl> <span data-ttu-id="08244-127"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="08244-127"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08244-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08244-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08244-129">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="08244-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
