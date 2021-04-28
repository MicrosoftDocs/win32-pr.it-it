---
description: "Funzione D3DXQuaternionSquad (D3DX10Math.h): interpola tra quaternioni, usando l'interpolazione quadrangolare sferica."
ms.assetid: ba953731-4372-4b32-942b-23abfe479704
title: Funzione D3DXQuaternionSquad (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9671b2a161124228c264da7eac0a2aa3a915ff95
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108759"
---
# <a name="d3dxquaternionsquad-function-d3dx10mathh"></a><span data-ttu-id="e10eb-103">Funzione D3DXQuaternionSquad (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="e10eb-103">D3DXQuaternionSquad function (D3DX10Math.h)</span></span>

<span data-ttu-id="e10eb-104">Interpola tra quaternioni, usando l'interpolazione quadrangolare sferica.</span><span class="sxs-lookup"><span data-stu-id="e10eb-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e10eb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e10eb-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="e10eb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e10eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e10eb-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e10eb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e10eb-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e10eb-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e10eb-109">Puntatore [**all'oggetto D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e10eb-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e10eb-110">*pQ1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e10eb-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e10eb-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e10eb-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e10eb-112">Puntatore a una struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="e10eb-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="e10eb-113">*pA* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e10eb-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e10eb-114">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e10eb-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e10eb-115">Puntatore a una struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="e10eb-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="e10eb-116">*pB* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e10eb-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e10eb-117">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e10eb-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e10eb-118">Puntatore a una struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="e10eb-118">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="e10eb-119">*pC* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e10eb-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e10eb-120">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e10eb-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e10eb-121">Puntatore a una struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="e10eb-121">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="e10eb-122">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e10eb-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e10eb-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e10eb-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e10eb-124">Parametro che indica la distanza da interpolare tra i quaternioni.</span><span class="sxs-lookup"><span data-stu-id="e10eb-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e10eb-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e10eb-125">Return value</span></span>

<span data-ttu-id="e10eb-126">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e10eb-126">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e10eb-127">Puntatore a una struttura D3DXQUATERNION che è il risultato dell'interpolazione quadrangolare sferica.</span><span class="sxs-lookup"><span data-stu-id="e10eb-127">Pointer to a D3DXQUATERNION structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="e10eb-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="e10eb-128">Remarks</span></span>

<span data-ttu-id="e10eb-129">Questa funzione usa la sequenza seguente di operazioni di interpolazione lineare sferica:</span><span class="sxs-lookup"><span data-stu-id="e10eb-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="e10eb-130">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="e10eb-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e10eb-131">In questo modo, la funzione D3DXQuaternionSquad può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="e10eb-131">In this way, the D3DXQuaternionSquad function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e10eb-132">Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="e10eb-132">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="e10eb-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e10eb-133">Requirements</span></span>



| <span data-ttu-id="e10eb-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e10eb-134">Requirement</span></span> | <span data-ttu-id="e10eb-135">Valore</span><span class="sxs-lookup"><span data-stu-id="e10eb-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e10eb-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e10eb-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e10eb-137"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="e10eb-137"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="e10eb-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="e10eb-138">Library</span></span><br/> | <dl> <span data-ttu-id="e10eb-139"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e10eb-139"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e10eb-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e10eb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e10eb-141">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="e10eb-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
