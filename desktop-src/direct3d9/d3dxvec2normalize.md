---
description: 'Funzione D3DXVec2Normalize (D3dx9math.h): restituisce la versione normalizzata di un vettore 2D.'
ms.assetid: 2796a5d1-cb1c-4093-87f2-a2ad43279d91
title: Funzione D3DXVec2Normalize (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3322981be5c266bee20a61e85302cb22538a7b0d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097969"
---
# <a name="d3dxvec2normalize-function-d3dx9mathh"></a><span data-ttu-id="a75d8-103">Funzione D3DXVec2Normalize (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="a75d8-103">D3DXVec2Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="a75d8-104">Restituisce la versione normalizzata di un vettore 2D.</span><span class="sxs-lookup"><span data-stu-id="a75d8-104">Returns the normalized version of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="a75d8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a75d8-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="a75d8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a75d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a75d8-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a75d8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a75d8-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="a75d8-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="a75d8-109">Puntatore alla [**struttura D3DXVECTOR2**](d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a75d8-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a75d8-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a75d8-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a75d8-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="a75d8-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="a75d8-112">Puntatore alla struttura [**D3DXVECTOR2 di**](d3dxvector2.md) origine.</span><span class="sxs-lookup"><span data-stu-id="a75d8-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a75d8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a75d8-113">Return value</span></span>

<span data-ttu-id="a75d8-114">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="a75d8-114">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="a75d8-115">Puntatore a [**una struttura D3DXVECTOR2**](d3dxvector2.md) che rappresenta la versione normalizzata del vettore.</span><span class="sxs-lookup"><span data-stu-id="a75d8-115">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="a75d8-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a75d8-116">Remarks</span></span>

<span data-ttu-id="a75d8-117">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="a75d8-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a75d8-118">In questo modo, la **funzione D3DXVec2Normalize** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="a75d8-118">In this way, the **D3DXVec2Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a75d8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a75d8-119">Requirements</span></span>



| <span data-ttu-id="a75d8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a75d8-120">Requirement</span></span> | <span data-ttu-id="a75d8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a75d8-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a75d8-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a75d8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a75d8-123"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="a75d8-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a75d8-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="a75d8-124">Library</span></span><br/> | <dl> <span data-ttu-id="a75d8-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a75d8-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a75d8-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a75d8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a75d8-127">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="a75d8-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




