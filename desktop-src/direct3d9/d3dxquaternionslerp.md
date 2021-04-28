---
description: "Funzione D3DXQuaternionSlerp (D3dx9math.h): interpola tra due quaternioni, usando l'interpolazione lineare sferica."
ms.assetid: 94a989c8-fa6b-4852-9aa3-e55ad814ffd7
title: Funzione D3DXQuaternionSlerp (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSlerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fb9110da7fae4ebbf4609d361124dbbcdedfe59b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093939"
---
# <a name="d3dxquaternionslerp-function-d3dx9mathh"></a><span data-ttu-id="5a3b5-103">Funzione D3DXQuaternionSlerp (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="5a3b5-103">D3DXQuaternionSlerp function (D3dx9math.h)</span></span>

<span data-ttu-id="5a3b5-104">Esegue l'interpolazione tra due quaternioni usando l'interpolazione lineare sferica.</span><span class="sxs-lookup"><span data-stu-id="5a3b5-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a3b5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a3b5-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="5a3b5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a3b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a3b5-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5a3b5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a3b5-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a3b5-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="5a3b5-109">Puntatore alla [**struttura D3DXQUATERNION**](d3dxquaternion.md) che è il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5a3b5-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5a3b5-110">*pQ1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5a3b5-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a3b5-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="5a3b5-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="5a3b5-112">Puntatore a una [**struttura D3DXQUATERNION di**](d3dxquaternion.md) origine.</span><span class="sxs-lookup"><span data-stu-id="5a3b5-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5a3b5-113">*pQ2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5a3b5-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a3b5-114">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="5a3b5-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="5a3b5-115">Puntatore a una [**struttura D3DXQUATERNION di**](d3dxquaternion.md) origine.</span><span class="sxs-lookup"><span data-stu-id="5a3b5-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5a3b5-116">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a3b5-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a3b5-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a3b5-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a3b5-118">Parametro che indica la distanza da interpolare tra i quaternioni.</span><span class="sxs-lookup"><span data-stu-id="5a3b5-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a3b5-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a3b5-119">Return value</span></span>

<span data-ttu-id="5a3b5-120">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a3b5-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="5a3b5-121">Puntatore a [**una struttura D3DXQUATERNION**](d3dxquaternion.md) che è il risultato dell'interpolazione.</span><span class="sxs-lookup"><span data-stu-id="5a3b5-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a3b5-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a3b5-122">Remarks</span></span>

<span data-ttu-id="5a3b5-123">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="5a3b5-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="5a3b5-124">In questo modo, la **funzione D3DXQuaternionSlerp** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="5a3b5-124">In this way, the **D3DXQuaternionSlerp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="5a3b5-125">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="5a3b5-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a3b5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a3b5-126">Requirements</span></span>



| <span data-ttu-id="5a3b5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a3b5-127">Requirement</span></span> | <span data-ttu-id="5a3b5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="5a3b5-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a3b5-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a3b5-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5a3b5-130"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="5a3b5-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5a3b5-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="5a3b5-131">Library</span></span><br/> | <dl> <span data-ttu-id="5a3b5-132"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a3b5-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5a3b5-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a3b5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a3b5-134">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="5a3b5-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
