---
description: Restituisce la versione normalizzata di un vettore 3D.
ms.assetid: 420321a2-0c3b-419c-9620-acf184e7b4f0
title: Funzione D3DXVec3Normalize (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 413b807c53e0b46b115af2aa283e4902a45f5979
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886310"
---
# <a name="d3dxvec3normalize-function-d3dx10mathh"></a><span data-ttu-id="5a23c-103">Funzione D3DXVec3Normalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="5a23c-103">D3DXVec3Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="5a23c-104">Restituisce la versione normalizzata di un vettore 3D.</span><span class="sxs-lookup"><span data-stu-id="5a23c-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a23c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a23c-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="5a23c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a23c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a23c-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5a23c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a23c-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a23c-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5a23c-109">Puntatore a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5a23c-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5a23c-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a23c-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a23c-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5a23c-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5a23c-112">Puntatore alla struttura D3DXVECTOR3 di origine.</span><span class="sxs-lookup"><span data-stu-id="5a23c-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a23c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a23c-113">Return value</span></span>

<span data-ttu-id="5a23c-114">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a23c-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5a23c-115">Puntatore a una struttura D3DXVECTOR3 che rappresenta la versione normalizzata del vettore specificato.</span><span class="sxs-lookup"><span data-stu-id="5a23c-115">Pointer to a D3DXVECTOR3 structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a23c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a23c-116">Remarks</span></span>

<span data-ttu-id="5a23c-117">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="5a23c-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="5a23c-118">In questo modo, la funzione D3DXVec3Normalize può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="5a23c-118">In this way, the D3DXVec3Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a23c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a23c-119">Requirements</span></span>



| <span data-ttu-id="5a23c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a23c-120">Requirement</span></span> | <span data-ttu-id="5a23c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5a23c-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a23c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a23c-122">Header</span></span><br/> | <dl> <span data-ttu-id="5a23c-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a23c-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a23c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a23c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a23c-125">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="5a23c-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
