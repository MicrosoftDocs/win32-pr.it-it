---
description: Esegue un'interpolazione lineare tra due vettori 3D.
ms.assetid: f3f06f1b-8824-47f0-b2ed-c212fa4c3225
title: Funzione D3DXVec3Lerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed6905cc0b13908a4e60e221737e9b5dc5a627f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323626"
---
# <a name="d3dxvec3lerp-function"></a><span data-ttu-id="4dab3-103">D3DXVec3Lerp (funzione)</span><span class="sxs-lookup"><span data-stu-id="4dab3-103">D3DXVec3Lerp function</span></span>

<span data-ttu-id="4dab3-104">Esegue un'interpolazione lineare tra due vettori 3D.</span><span class="sxs-lookup"><span data-stu-id="4dab3-104">Performs a linear interpolation between two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dab3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4dab3-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Lerp(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="4dab3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4dab3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dab3-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="4dab3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4dab3-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="4dab3-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4dab3-109">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4dab3-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4dab3-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4dab3-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dab3-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4dab3-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4dab3-112">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="4dab3-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4dab3-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4dab3-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dab3-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4dab3-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4dab3-115">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="4dab3-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4dab3-116">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4dab3-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dab3-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4dab3-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4dab3-118">Parametro che esegue l'interpolazione lineare tra i vettori.</span><span class="sxs-lookup"><span data-stu-id="4dab3-118">Parameter that linearly interpolates between the vectors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dab3-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4dab3-119">Return value</span></span>

<span data-ttu-id="4dab3-120">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="4dab3-120">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4dab3-121">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che è il risultato dell'interpolazione lineare.</span><span class="sxs-lookup"><span data-stu-id="4dab3-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dab3-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="4dab3-122">Remarks</span></span>

<span data-ttu-id="4dab3-123">Questa funzione esegue l'interpolazione lineare in base alla formula seguente: V1 + s (v2-v1).</span><span class="sxs-lookup"><span data-stu-id="4dab3-123">This function performs the linear interpolation based on the following formula: V1 + s(V2-V1).</span></span>

<span data-ttu-id="4dab3-124">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="4dab3-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="4dab3-125">In questo modo, la funzione **D3DXVec3Lerp** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="4dab3-125">In this way, the **D3DXVec3Lerp** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dab3-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4dab3-126">Requirements</span></span>



| <span data-ttu-id="4dab3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dab3-127">Requirement</span></span> | <span data-ttu-id="4dab3-128">Valore</span><span class="sxs-lookup"><span data-stu-id="4dab3-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4dab3-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4dab3-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4dab3-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dab3-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4dab3-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="4dab3-131">Library</span></span><br/> | <dl> <span data-ttu-id="4dab3-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4dab3-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4dab3-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4dab3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dab3-134">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="4dab3-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
