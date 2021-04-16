---
description: Esegue l'interpolazione tra quaternioni usando l'interpolazione quadrangolare sferica.
ms.assetid: ba953731-4372-4b32-942b-23abfe479704
title: Funzione D3DXQuaternionSquad (D3DX10Math. h)
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
ms.openlocfilehash: af2bb582909cf09a4044b293f3f298a5da2335a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530997"
---
# <a name="d3dxquaternionsquad-function-d3dx10mathh"></a><span data-ttu-id="910c5-103">Funzione D3DXQuaternionSquad (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="910c5-103">D3DXQuaternionSquad function (D3DX10Math.h)</span></span>

<span data-ttu-id="910c5-104">Esegue l'interpolazione tra quaternioni usando l'interpolazione quadrangolare sferica.</span><span class="sxs-lookup"><span data-stu-id="910c5-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="910c5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="910c5-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="910c5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="910c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="910c5-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="910c5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="910c5-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="910c5-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="910c5-109">Puntatore a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="910c5-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="910c5-110">*pQ1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="910c5-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="910c5-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="910c5-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="910c5-112">Puntatore a una struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="910c5-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="910c5-113">*PA* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="910c5-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="910c5-114">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="910c5-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="910c5-115">Puntatore a una struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="910c5-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="910c5-116">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="910c5-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="910c5-117">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="910c5-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="910c5-118">Puntatore a una struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="910c5-118">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="910c5-119">*computer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="910c5-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="910c5-120">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="910c5-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="910c5-121">Puntatore a una struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="910c5-121">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="910c5-122">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="910c5-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="910c5-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="910c5-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="910c5-124">Parametro che indica la distanza di interpolazione tra i quaternioni.</span><span class="sxs-lookup"><span data-stu-id="910c5-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="910c5-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="910c5-125">Return value</span></span>

<span data-ttu-id="910c5-126">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="910c5-126">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="910c5-127">Puntatore a una struttura D3DXQUATERNION che è il risultato dell'interpolazione quadrangolare sferica.</span><span class="sxs-lookup"><span data-stu-id="910c5-127">Pointer to a D3DXQUATERNION structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="910c5-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="910c5-128">Remarks</span></span>

<span data-ttu-id="910c5-129">Questa funzione usa la sequenza di operazioni di interpolazione lineare sferica seguente:</span><span class="sxs-lookup"><span data-stu-id="910c5-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="910c5-130">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="910c5-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="910c5-131">In questo modo, la funzione D3DXQuaternionSquad può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="910c5-131">In this way, the D3DXQuaternionSquad function can be used as a parameter for another function.</span></span>

<span data-ttu-id="910c5-132">Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="910c5-132">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="910c5-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="910c5-133">Requirements</span></span>



| <span data-ttu-id="910c5-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="910c5-134">Requirement</span></span> | <span data-ttu-id="910c5-135">Valore</span><span class="sxs-lookup"><span data-stu-id="910c5-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="910c5-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="910c5-136">Header</span></span><br/>  | <dl> <span data-ttu-id="910c5-137"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="910c5-137"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="910c5-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="910c5-138">Library</span></span><br/> | <dl> <span data-ttu-id="910c5-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="910c5-139"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="910c5-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="910c5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="910c5-141">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="910c5-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
