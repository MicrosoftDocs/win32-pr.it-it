---
description: Restituisce la versione normalizzata di un vettore 4D.
ms.assetid: e12d5dc7-b26f-41dd-b89d-1df9ba23077a
title: Funzione D3DXVec4Normalize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 38d97f337711375d1d414eb78fb317672bc7c5cb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058701"
---
# <a name="d3dxvec4normalize-function-d3dx9mathh"></a><span data-ttu-id="6239d-103">Funzione D3DXVec4Normalize (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="6239d-103">D3DXVec4Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="6239d-104">Restituisce la versione normalizzata di un vettore 4D.</span><span class="sxs-lookup"><span data-stu-id="6239d-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="6239d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6239d-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="6239d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6239d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6239d-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6239d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6239d-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="6239d-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6239d-109">Puntatore alla struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6239d-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6239d-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6239d-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6239d-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="6239d-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6239d-112">Puntatore alla struttura [**D3DXVECTOR4**](d3dxvector4.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="6239d-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6239d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6239d-113">Return value</span></span>

<span data-ttu-id="6239d-114">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="6239d-114">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6239d-115">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta la versione normalizzata del vettore.</span><span class="sxs-lookup"><span data-stu-id="6239d-115">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="6239d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6239d-116">Remarks</span></span>

<span data-ttu-id="6239d-117">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="6239d-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6239d-118">In questo modo, la funzione **D3DXVec4Normalize** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="6239d-118">In this way, the **D3DXVec4Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6239d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6239d-119">Requirements</span></span>



| <span data-ttu-id="6239d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6239d-120">Requirement</span></span> | <span data-ttu-id="6239d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="6239d-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6239d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6239d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6239d-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6239d-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6239d-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="6239d-124">Library</span></span><br/> | <dl> <span data-ttu-id="6239d-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6239d-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6239d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6239d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6239d-127">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="6239d-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




