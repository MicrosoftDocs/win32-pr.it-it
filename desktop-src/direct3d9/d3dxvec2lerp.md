---
description: Esegue un'interpolazione lineare tra due vettori 2D.
ms.assetid: f8e9e6be-9696-4a4a-a6c8-c021985decaa
title: Funzione D3DXVec2Lerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b08b767993143db3057985140b97854b9203d2b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322459"
---
# <a name="d3dxvec2lerp-function"></a><span data-ttu-id="a04d0-103">D3DXVec2Lerp (funzione)</span><span class="sxs-lookup"><span data-stu-id="a04d0-103">D3DXVec2Lerp function</span></span>

<span data-ttu-id="a04d0-104">Esegue un'interpolazione lineare tra due vettori 2D.</span><span class="sxs-lookup"><span data-stu-id="a04d0-104">Performs a linear interpolation between two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="a04d0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a04d0-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Lerp(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="a04d0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a04d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a04d0-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a04d0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a04d0-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="a04d0-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="a04d0-109">Puntatore alla struttura [**D3DXVECTOR2**](d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a04d0-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a04d0-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a04d0-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a04d0-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="a04d0-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="a04d0-112">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="a04d0-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a04d0-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a04d0-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a04d0-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="a04d0-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="a04d0-115">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="a04d0-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a04d0-116">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a04d0-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a04d0-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a04d0-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a04d0-118">Parametro che esegue l'interpolazione lineare tra i vettori.</span><span class="sxs-lookup"><span data-stu-id="a04d0-118">Parameter that linearly interpolates between the vectors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a04d0-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a04d0-119">Return value</span></span>

<span data-ttu-id="a04d0-120">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="a04d0-120">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="a04d0-121">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) che è il risultato dell'interpolazione lineare.</span><span class="sxs-lookup"><span data-stu-id="a04d0-121">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="a04d0-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="a04d0-122">Remarks</span></span>

<span data-ttu-id="a04d0-123">Questa funzione esegue l'interpolazione lineare in base alla formula seguente: V1 + s (v2-v1).</span><span class="sxs-lookup"><span data-stu-id="a04d0-123">This function performs the linear interpolation based on the following formula: V1 + s(V2-V1).</span></span>

<span data-ttu-id="a04d0-124">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="a04d0-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a04d0-125">In questo modo, la funzione **D3DXVec2Lerp** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="a04d0-125">In this way, the **D3DXVec2Lerp** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a04d0-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a04d0-126">Requirements</span></span>



| <span data-ttu-id="a04d0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a04d0-127">Requirement</span></span> | <span data-ttu-id="a04d0-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a04d0-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a04d0-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a04d0-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a04d0-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a04d0-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a04d0-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="a04d0-131">Library</span></span><br/> | <dl> <span data-ttu-id="a04d0-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a04d0-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a04d0-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a04d0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a04d0-134">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="a04d0-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
