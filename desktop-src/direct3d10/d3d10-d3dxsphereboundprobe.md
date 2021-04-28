---
description: 'Funzione D3DXSphereBoundProbe (D3DX10math.h): determina se un raggio interseca il volume del rettangolo di selezione di una sfera.'
ms.assetid: 5984a1a6-d36c-4a05-8c74-0ece7443356c
title: Funzione D3DXSphereBoundProbe (D3DX10math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSphereBoundProbe
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fb5a329e39631dff626ff1c7945ad4b05f9dcd58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108469"
---
# <a name="d3dxsphereboundprobe-function-d3dx10mathh"></a><span data-ttu-id="0f400-103">Funzione D3DXSphereBoundProbe (D3DX10math.h)</span><span class="sxs-lookup"><span data-stu-id="0f400-103">D3DXSphereBoundProbe function (D3DX10math.h)</span></span>

<span data-ttu-id="0f400-104">Determina se un raggio interseca il volume del rettangolo di selezione di una sfera.</span><span class="sxs-lookup"><span data-stu-id="0f400-104">Determines if a ray intersects the volume of a sphere's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f400-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f400-105">Syntax</span></span>


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="0f400-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f400-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f400-107">*pCenter* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0f400-107">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f400-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0f400-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0f400-109">Puntatore a [**una struttura D3DXVECTOR3,**](d3d10-d3dxvector3.md) che specifica la coordinata centrale della sfera.</span><span class="sxs-lookup"><span data-stu-id="0f400-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the center coordinate of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="0f400-110">*Raggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0f400-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f400-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f400-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0f400-112">Raggio della sfera.</span><span class="sxs-lookup"><span data-stu-id="0f400-112">Radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="0f400-113">*pRayPosition* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0f400-113">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f400-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0f400-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0f400-115">Puntatore a [**una struttura D3DXVECTOR3,**](d3d10-d3dxvector3.md) che specifica la coordinata di origine del raggio.</span><span class="sxs-lookup"><span data-stu-id="0f400-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="0f400-116">*pRayDirection* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0f400-116">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f400-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0f400-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0f400-118">Puntatore a [**una struttura D3DXVECTOR3,**](d3d10-d3dxvector3.md) che specifica la direzione del raggio.</span><span class="sxs-lookup"><span data-stu-id="0f400-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="0f400-119">Questo vettore non deve essere (0,0,0), ma non deve essere normalizzato.</span><span class="sxs-lookup"><span data-stu-id="0f400-119">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f400-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f400-120">Return value</span></span>

<span data-ttu-id="0f400-121">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f400-121">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0f400-122">Restituisce **TRUE** se il raggio interseca il volume del rettangolo di selezione della sfera.</span><span class="sxs-lookup"><span data-stu-id="0f400-122">Returns **TRUE** if the ray intersects the volume of the sphere's bounding box.</span></span> <span data-ttu-id="0f400-123">In caso contrario, **restituisce FALSE.**</span><span class="sxs-lookup"><span data-stu-id="0f400-123">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f400-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f400-124">Remarks</span></span>

<span data-ttu-id="0f400-125">**D3DXSphereBoundProbe** determina se il raggio interseca il volume del rettangolo di selezione della sfera, non solo la superficie della sfera.</span><span class="sxs-lookup"><span data-stu-id="0f400-125">**D3DXSphereBoundProbe** determines if the ray intersects the volume of the sphere's bounding box, not just the surface of the sphere.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f400-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f400-126">Requirements</span></span>



| <span data-ttu-id="0f400-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f400-127">Requirement</span></span> | <span data-ttu-id="0f400-128">Valore</span><span class="sxs-lookup"><span data-stu-id="0f400-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f400-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f400-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0f400-130"><dt>D3DX10math.h</dt></span><span class="sxs-lookup"><span data-stu-id="0f400-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="0f400-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="0f400-131">Library</span></span><br/> | <dl> <span data-ttu-id="0f400-132"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f400-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0f400-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f400-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f400-134">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="0f400-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
