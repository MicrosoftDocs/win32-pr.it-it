---
description: Usa un'analisi efficiente del raggio nelle simulazioni del trasferimento di luminosità pre-calcolate (PRT) per determinare se un raggio interseca una mesh. Viene in genere utilizzato per determinare se un punto specificato è ombreggiato.
ms.assetid: fcd53a0f-80e8-4013-8efd-125e38f4ccd0
title: 'Metodo ID3DXPRTEngine:: ShadowRayIntersects (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ShadowRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 701aa4c89ee6a9d657721d872565c9b2056bb435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058629"
---
# <a name="id3dxprtengineshadowrayintersects-method"></a><span data-ttu-id="24a3b-104">Metodo ID3DXPRTEngine:: ShadowRayIntersects</span><span class="sxs-lookup"><span data-stu-id="24a3b-104">ID3DXPRTEngine::ShadowRayIntersects method</span></span>

<span data-ttu-id="24a3b-105">Usa un'analisi efficiente del raggio nelle simulazioni del trasferimento di luminosità pre-calcolate (PRT) per determinare se un raggio interseca una mesh.</span><span class="sxs-lookup"><span data-stu-id="24a3b-105">Uses efficient ray-tracing in precomputed radiance transfer (PRT) simulations to determine whether a ray intersects a mesh.</span></span> <span data-ttu-id="24a3b-106">Viene in genere utilizzato per determinare se un punto specificato è ombreggiato.</span><span class="sxs-lookup"><span data-stu-id="24a3b-106">Typically used to determine whether a given point is in shadow.</span></span>

## <a name="syntax"></a><span data-ttu-id="24a3b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24a3b-107">Syntax</span></span>


```C++
BOOL ShadowRayIntersects(
  [in] const D3DXVECTOR3 *pRayPos,
  [in] const D3DXVECTOR3 *pRayDir
);
```



## <a name="parameters"></a><span data-ttu-id="24a3b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="24a3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24a3b-109">*pRayPos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24a3b-109">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24a3b-110">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="24a3b-110">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="24a3b-111">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica il punto in cui inizia il raggio.</span><span class="sxs-lookup"><span data-stu-id="24a3b-111">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="24a3b-112">*pRayDir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24a3b-112">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24a3b-113">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="24a3b-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="24a3b-114">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica la direzione normalizzata del raggio.</span><span class="sxs-lookup"><span data-stu-id="24a3b-114">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the normalized direction of the ray.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24a3b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24a3b-115">Return value</span></span>

<span data-ttu-id="24a3b-116">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24a3b-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24a3b-117">Restituisce **true** se il raggio interseca la mesh corrente; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="24a3b-117">Returns **TRUE** if the ray intersects the current mesh; otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="24a3b-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="24a3b-118">Remarks</span></span>

<span data-ttu-id="24a3b-119">Usare [**ID3DXPRTEngine:: SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) per impostare le distanze minime e massime dell'intersezione con il raggio.</span><span class="sxs-lookup"><span data-stu-id="24a3b-119">Use [**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) to set minimum and maximum distances of intersection with the ray.</span></span>

<span data-ttu-id="24a3b-120">Questo metodo viene eseguito più velocemente di [**ID3DXPRTEngine:: ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md).</span><span class="sxs-lookup"><span data-stu-id="24a3b-120">This method executes faster than [**ID3DXPRTEngine::ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="24a3b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24a3b-121">Requirements</span></span>



| <span data-ttu-id="24a3b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="24a3b-122">Requirement</span></span> | <span data-ttu-id="24a3b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="24a3b-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24a3b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24a3b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="24a3b-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="24a3b-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="24a3b-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="24a3b-126">Library</span></span><br/> | <dl> <span data-ttu-id="24a3b-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24a3b-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="24a3b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24a3b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a3b-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="24a3b-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="24a3b-130">**ID3DXPRTEngine::ClosestRayIntersects**</span><span class="sxs-lookup"><span data-stu-id="24a3b-130">**ID3DXPRTEngine::ClosestRayIntersects**</span></span>](id3dxprtengine--closestrayintersects.md)
</dt> <dt>

[<span data-ttu-id="24a3b-131">**ID3DXPRTEngine::SetMinMaxIntersection**</span><span class="sxs-lookup"><span data-stu-id="24a3b-131">**ID3DXPRTEngine::SetMinMaxIntersection**</span></span>](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
