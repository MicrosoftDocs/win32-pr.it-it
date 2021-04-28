---
description: 'Funzione D3DXVec2Normalize (D3DX10Math.h): restituisce la versione normalizzata di un vettore 2D.'
ms.assetid: fac4f269-2778-4500-af9e-23a0112543b0
title: Funzione D3DXVec2Normalize (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Normalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: aaa7bde759b9023b69204d6cb39259f0905b9928
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108389"
---
# <a name="d3dxvec2normalize-function-d3dx10mathh"></a><span data-ttu-id="98bfa-103">Funzione D3DXVec2Normalize (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="98bfa-103">D3DXVec2Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="98bfa-104">Restituisce la versione normalizzata di un vettore 2D.</span><span class="sxs-lookup"><span data-stu-id="98bfa-104">Returns the normalized version of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="98bfa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98bfa-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="98bfa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="98bfa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98bfa-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="98bfa-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98bfa-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="98bfa-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="98bfa-109">Puntatore a [**D3DXVECTOR2**](d3d10-d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="98bfa-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="98bfa-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="98bfa-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98bfa-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="98bfa-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="98bfa-112">Puntatore alla struttura D3DXVECTOR2 di origine.</span><span class="sxs-lookup"><span data-stu-id="98bfa-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98bfa-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98bfa-113">Return value</span></span>

<span data-ttu-id="98bfa-114">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="98bfa-114">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="98bfa-115">Puntatore a una struttura D3DXVECTOR2 che rappresenta la versione normalizzata del vettore.</span><span class="sxs-lookup"><span data-stu-id="98bfa-115">Pointer to a D3DXVECTOR2 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="98bfa-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="98bfa-116">Remarks</span></span>

<span data-ttu-id="98bfa-117">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="98bfa-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="98bfa-118">In questo modo, la funzione D3DXVec2Normalize può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="98bfa-118">In this way, the D3DXVec2Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="98bfa-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98bfa-119">Requirements</span></span>



| <span data-ttu-id="98bfa-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="98bfa-120">Requirement</span></span> | <span data-ttu-id="98bfa-121">Valore</span><span class="sxs-lookup"><span data-stu-id="98bfa-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98bfa-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98bfa-122">Header</span></span><br/>  | <dl> <span data-ttu-id="98bfa-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="98bfa-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="98bfa-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="98bfa-124">Library</span></span><br/> | <dl> <span data-ttu-id="98bfa-125"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="98bfa-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="98bfa-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98bfa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98bfa-127">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="98bfa-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
