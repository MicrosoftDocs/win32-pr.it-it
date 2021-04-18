---
description: Esegue l'interpolazione tra quaternioni usando l'interpolazione quadrangolare sferica.
ms.assetid: afce9afb-64cc-4059-90f5-7ed1aca9b3cb
title: Funzione D3DXQuaternionSquad (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e4fa980d551ac43f66035c1dcaa46d1c1c590a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322486"
---
# <a name="d3dxquaternionsquad-function-d3dx9mathh"></a><span data-ttu-id="ce3aa-103">Funzione D3DXQuaternionSquad (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="ce3aa-103">D3DXQuaternionSquad function (D3dx9math.h)</span></span>

<span data-ttu-id="ce3aa-104">Esegue l'interpolazione tra quaternioni usando l'interpolazione quadrangolare sferica.</span><span class="sxs-lookup"><span data-stu-id="ce3aa-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce3aa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce3aa-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="ce3aa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce3aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce3aa-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ce3aa-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce3aa-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ce3aa-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ce3aa-109">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ce3aa-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ce3aa-110">*pQ1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce3aa-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce3aa-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ce3aa-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ce3aa-112">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="ce3aa-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ce3aa-113">*PA* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce3aa-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce3aa-114">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ce3aa-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ce3aa-115">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="ce3aa-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ce3aa-116">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce3aa-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce3aa-117">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ce3aa-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ce3aa-118">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="ce3aa-118">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ce3aa-119">*computer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce3aa-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce3aa-120">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ce3aa-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ce3aa-121">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="ce3aa-121">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ce3aa-122">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce3aa-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce3aa-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce3aa-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce3aa-124">Parametro che indica la distanza di interpolazione tra i quaternioni.</span><span class="sxs-lookup"><span data-stu-id="ce3aa-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce3aa-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce3aa-125">Return value</span></span>

<span data-ttu-id="ce3aa-126">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ce3aa-126">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ce3aa-127">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) che è il risultato dell'interpolazione quadrangolare sferica.</span><span class="sxs-lookup"><span data-stu-id="ce3aa-127">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce3aa-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce3aa-128">Remarks</span></span>

<span data-ttu-id="ce3aa-129">Questa funzione usa la sequenza di operazioni di interpolazione lineare sferica seguente:</span><span class="sxs-lookup"><span data-stu-id="ce3aa-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="ce3aa-130">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="ce3aa-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ce3aa-131">In questo modo, la funzione **D3DXQuaternionSquad** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="ce3aa-131">In this way, the **D3DXQuaternionSquad** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ce3aa-132">Per un esempio di interpolazione tra quaternioni, vedere l'esempio SkinnedMesh.</span><span class="sxs-lookup"><span data-stu-id="ce3aa-132">For an example of interpolating between quaternions, see the SkinnedMesh Sample.</span></span> <span data-ttu-id="ce3aa-133">È possibile ottenere questo esempio e ottenere informazioni su di esso da DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="ce3aa-133">You can get this sample and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="ce3aa-134">Per informazioni su DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="ce3aa-134">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="ce3aa-135">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="ce3aa-135">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce3aa-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce3aa-136">Requirements</span></span>



| <span data-ttu-id="ce3aa-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce3aa-137">Requirement</span></span> | <span data-ttu-id="ce3aa-138">Valore</span><span class="sxs-lookup"><span data-stu-id="ce3aa-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce3aa-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce3aa-139">Header</span></span><br/>  | <dl> <span data-ttu-id="ce3aa-140"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce3aa-140"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ce3aa-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="ce3aa-141">Library</span></span><br/> | <dl> <span data-ttu-id="ce3aa-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce3aa-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ce3aa-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce3aa-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce3aa-144">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="ce3aa-144">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ce3aa-145">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="ce3aa-145">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="ce3aa-146">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="ce3aa-146">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
</dt> <dt>

[<span data-ttu-id="ce3aa-147">**D3DXQuaternionSquadSetup**</span><span class="sxs-lookup"><span data-stu-id="ce3aa-147">**D3DXQuaternionSquadSetup**</span></span>](d3dxquaternionsquadsetup.md)
</dt> </dl>

 

 
