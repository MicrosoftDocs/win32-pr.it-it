---
description: 'Funzione D3DXVec4Normalize (D3DX10Math.h): restituisce la versione normalizzata di un vettore 4D.'
ms.assetid: ed3c48cf-4985-4ef3-b733-f8532e3ff6b5
title: Funzione D3DXVec4Normalize (D3DX10Math.h)
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
ms.openlocfilehash: 1577ff3109c2cc3ca547f68f7841ecebb2f03569
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102909"
---
# <a name="d3dxvec4normalize-function-d3dx10mathh"></a><span data-ttu-id="acdfe-103">Funzione D3DXVec4Normalize (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="acdfe-103">D3DXVec4Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="acdfe-104">Restituisce la versione normalizzata di un vettore 4D.</span><span class="sxs-lookup"><span data-stu-id="acdfe-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="acdfe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="acdfe-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="acdfe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="acdfe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acdfe-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="acdfe-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="acdfe-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="acdfe-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="acdfe-109">Puntatore [**all'oggetto D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="acdfe-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="acdfe-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="acdfe-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acdfe-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="acdfe-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="acdfe-112">Puntatore alla struttura D3DXVECTOR4 di origine.</span><span class="sxs-lookup"><span data-stu-id="acdfe-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acdfe-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="acdfe-113">Return value</span></span>

<span data-ttu-id="acdfe-114">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="acdfe-114">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="acdfe-115">Puntatore a una struttura D3DXVECTOR4 che rappresenta la versione normalizzata del vettore.</span><span class="sxs-lookup"><span data-stu-id="acdfe-115">Pointer to a D3DXVECTOR4 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="acdfe-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="acdfe-116">Remarks</span></span>

<span data-ttu-id="acdfe-117">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="acdfe-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="acdfe-118">In questo modo, la funzione D3DXVec4Normalize può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="acdfe-118">In this way, the D3DXVec4Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="acdfe-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="acdfe-119">Requirements</span></span>



| <span data-ttu-id="acdfe-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="acdfe-120">Requirement</span></span> | <span data-ttu-id="acdfe-121">Valore</span><span class="sxs-lookup"><span data-stu-id="acdfe-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acdfe-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="acdfe-122">Header</span></span><br/> | <dl> <span data-ttu-id="acdfe-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="acdfe-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acdfe-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="acdfe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acdfe-125">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="acdfe-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
