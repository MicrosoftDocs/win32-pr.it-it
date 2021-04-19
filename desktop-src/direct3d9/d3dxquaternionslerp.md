---
description: Esegue l'interpolazione tra due quaternioni usando l'interpolazione lineare sferica.
ms.assetid: 94a989c8-fa6b-4852-9aa3-e55ad814ffd7
title: Funzione D3DXQuaternionSlerp (D3dx9math. h)
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
ms.openlocfilehash: f0f43e22ddc46007c6f589dfc5fd8b45aa885643
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322488"
---
# <a name="d3dxquaternionslerp-function-d3dx9mathh"></a><span data-ttu-id="ff71d-103">Funzione D3DXQuaternionSlerp (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="ff71d-103">D3DXQuaternionSlerp function (D3dx9math.h)</span></span>

<span data-ttu-id="ff71d-104">Esegue l'interpolazione tra due quaternioni usando l'interpolazione lineare sferica.</span><span class="sxs-lookup"><span data-stu-id="ff71d-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff71d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff71d-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="ff71d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ff71d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff71d-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ff71d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff71d-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ff71d-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ff71d-109">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ff71d-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ff71d-110">*pQ1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff71d-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff71d-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ff71d-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ff71d-112">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="ff71d-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ff71d-113">*pQ2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff71d-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff71d-114">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ff71d-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ff71d-115">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="ff71d-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ff71d-116">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff71d-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff71d-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff71d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff71d-118">Parametro che indica la distanza di interpolazione tra i quaternioni.</span><span class="sxs-lookup"><span data-stu-id="ff71d-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff71d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ff71d-119">Return value</span></span>

<span data-ttu-id="ff71d-120">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ff71d-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ff71d-121">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) che è il risultato dell'interpolazione.</span><span class="sxs-lookup"><span data-stu-id="ff71d-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff71d-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff71d-122">Remarks</span></span>

<span data-ttu-id="ff71d-123">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="ff71d-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ff71d-124">In questo modo, la funzione **D3DXQuaternionSlerp** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="ff71d-124">In this way, the **D3DXQuaternionSlerp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ff71d-125">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="ff71d-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff71d-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff71d-126">Requirements</span></span>



| <span data-ttu-id="ff71d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff71d-127">Requirement</span></span> | <span data-ttu-id="ff71d-128">Valore</span><span class="sxs-lookup"><span data-stu-id="ff71d-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff71d-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ff71d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ff71d-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff71d-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ff71d-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="ff71d-131">Library</span></span><br/> | <dl> <span data-ttu-id="ff71d-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff71d-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ff71d-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff71d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff71d-134">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="ff71d-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
