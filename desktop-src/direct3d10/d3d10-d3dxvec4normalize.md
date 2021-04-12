---
description: Restituisce la versione normalizzata di un vettore 4D.
ms.assetid: ed3c48cf-4985-4ef3-b733-f8532e3ff6b5
title: Funzione D3DXVec4Normalize (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: ebedbdddbe558bfad71520b64aa0cf2ff4c2f451
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355294"
---
# <a name="d3dxvec4normalize-function-d3dx10mathh"></a><span data-ttu-id="68800-103">Funzione D3DXVec4Normalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="68800-103">D3DXVec4Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="68800-104">Restituisce la versione normalizzata di un vettore 4D.</span><span class="sxs-lookup"><span data-stu-id="68800-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="68800-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68800-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="68800-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="68800-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68800-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="68800-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="68800-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="68800-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="68800-109">Puntatore a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="68800-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="68800-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68800-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68800-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="68800-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="68800-112">Puntatore alla struttura D3DXVECTOR4 di origine.</span><span class="sxs-lookup"><span data-stu-id="68800-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68800-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68800-113">Return value</span></span>

<span data-ttu-id="68800-114">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="68800-114">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="68800-115">Puntatore a una struttura D3DXVECTOR4 che rappresenta la versione normalizzata del vettore.</span><span class="sxs-lookup"><span data-stu-id="68800-115">Pointer to a D3DXVECTOR4 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="68800-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="68800-116">Remarks</span></span>

<span data-ttu-id="68800-117">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="68800-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="68800-118">In questo modo, la funzione D3DXVec4Normalize può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="68800-118">In this way, the D3DXVec4Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="68800-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68800-119">Requirements</span></span>



| <span data-ttu-id="68800-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="68800-120">Requirement</span></span> | <span data-ttu-id="68800-121">Valore</span><span class="sxs-lookup"><span data-stu-id="68800-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68800-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68800-122">Header</span></span><br/> | <dl> <span data-ttu-id="68800-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="68800-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68800-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68800-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68800-125">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="68800-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
