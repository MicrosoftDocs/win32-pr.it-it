---
description: "Funzione D3DXQuaternionSlerp (D3DX10Math.h): interpola tra due quaternioni usando l'interpolazione lineare sferica."
ms.assetid: 487e1df1-bf20-49cb-ad14-61fcf1300904
title: Funzione D3DXQuaternionSlerp (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 04cd3d82e4ca4e3f3357ab0114b57602f7e8a543
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103119"
---
# <a name="d3dxquaternionslerp-function-d3dx10mathh"></a><span data-ttu-id="27b6d-103">Funzione D3DXQuaternionSlerp (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="27b6d-103">D3DXQuaternionSlerp function (D3DX10Math.h)</span></span>

<span data-ttu-id="27b6d-104">Esegue l'interpolazione tra due quaternioni usando l'interpolazione lineare sferica.</span><span class="sxs-lookup"><span data-stu-id="27b6d-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="27b6d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27b6d-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="27b6d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="27b6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27b6d-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="27b6d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="27b6d-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="27b6d-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="27b6d-109">Puntatore [**all'oggetto D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="27b6d-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="27b6d-110">*pQ1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="27b6d-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27b6d-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="27b6d-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="27b6d-112">Puntatore a una struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="27b6d-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="27b6d-113">*pQ2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="27b6d-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27b6d-114">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="27b6d-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="27b6d-115">Puntatore a una struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="27b6d-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="27b6d-116">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27b6d-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27b6d-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27b6d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="27b6d-118">Parametro che indica la distanza da interpolare tra i quaternioni.</span><span class="sxs-lookup"><span data-stu-id="27b6d-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27b6d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27b6d-119">Return value</span></span>

<span data-ttu-id="27b6d-120">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="27b6d-120">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="27b6d-121">Puntatore a una struttura D3DXQUATERNION che è il risultato dell'interpolazione.</span><span class="sxs-lookup"><span data-stu-id="27b6d-121">Pointer to a D3DXQUATERNION structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="27b6d-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="27b6d-122">Remarks</span></span>

<span data-ttu-id="27b6d-123">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="27b6d-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="27b6d-124">In questo modo, la funzione D3DXQuaternionSlerp può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="27b6d-124">In this way, the D3DXQuaternionSlerp function can be used as a parameter for another function.</span></span>

<span data-ttu-id="27b6d-125">Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="27b6d-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="27b6d-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27b6d-126">Requirements</span></span>



| <span data-ttu-id="27b6d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="27b6d-127">Requirement</span></span> | <span data-ttu-id="27b6d-128">Valore</span><span class="sxs-lookup"><span data-stu-id="27b6d-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27b6d-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27b6d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="27b6d-130"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="27b6d-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="27b6d-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="27b6d-131">Library</span></span><br/> | <dl> <span data-ttu-id="27b6d-132"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="27b6d-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="27b6d-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27b6d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27b6d-134">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="27b6d-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
