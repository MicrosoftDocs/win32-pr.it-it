---
description: 'Funzione D3DXSphereBoundProbe (D3DX9Mesh.h): determina se un raggio interseca il volume del rettangolo di selezione di una sfera.'
ms.assetid: fa2e9ecf-7905-4a62-ba48-774bd522525a
title: Funzione D3DXSphereBoundProbe (D3DX9Mesh.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2d3ea263d7ad8bc50b936fd1010c352c0c01783
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093849"
---
# <a name="d3dxsphereboundprobe-function-d3dx9meshh"></a><span data-ttu-id="29b85-103">Funzione D3DXSphereBoundProbe (D3DX9Mesh.h)</span><span class="sxs-lookup"><span data-stu-id="29b85-103">D3DXSphereBoundProbe function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="29b85-104">Determina se un raggio interseca il volume del rettangolo di selezione di una sfera.</span><span class="sxs-lookup"><span data-stu-id="29b85-104">Determines if a ray intersects the volume of a sphere's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="29b85-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29b85-105">Syntax</span></span>


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="29b85-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="29b85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29b85-107">*pCenter* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="29b85-107">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29b85-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="29b85-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="29b85-109">Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che specifica la coordinata centrale della sfera.</span><span class="sxs-lookup"><span data-stu-id="29b85-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the center coordinate of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="29b85-110">*Raggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="29b85-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29b85-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="29b85-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="29b85-112">Raggio della sfera.</span><span class="sxs-lookup"><span data-stu-id="29b85-112">Radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="29b85-113">*pRayPosition* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="29b85-113">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29b85-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="29b85-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="29b85-115">Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che specifica la coordinata di origine del raggio.</span><span class="sxs-lookup"><span data-stu-id="29b85-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="29b85-116">*pRayDirection* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="29b85-116">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29b85-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="29b85-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="29b85-118">Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che specifica la direzione del raggio.</span><span class="sxs-lookup"><span data-stu-id="29b85-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="29b85-119">Questo vettore non deve essere (0,0,0), ma non deve essere normalizzato.</span><span class="sxs-lookup"><span data-stu-id="29b85-119">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29b85-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29b85-120">Return value</span></span>

<span data-ttu-id="29b85-121">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="29b85-121">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="29b85-122">Restituisce **TRUE** se il raggio interseca il volume del rettangolo di selezione della sfera.</span><span class="sxs-lookup"><span data-stu-id="29b85-122">Returns **TRUE** if the ray intersects the volume of the sphere's bounding box.</span></span> <span data-ttu-id="29b85-123">In caso contrario, **restituisce FALSE.**</span><span class="sxs-lookup"><span data-stu-id="29b85-123">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="29b85-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="29b85-124">Remarks</span></span>

<span data-ttu-id="29b85-125">**D3DXSphereBoundProbe** determina se il raggio interseca il volume del rettangolo di selezione della sfera, non solo la superficie della sfera.</span><span class="sxs-lookup"><span data-stu-id="29b85-125">**D3DXSphereBoundProbe** determines if the ray intersects the volume of the sphere's bounding box, not just the surface of the sphere.</span></span>

## <a name="requirements"></a><span data-ttu-id="29b85-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29b85-126">Requirements</span></span>



| <span data-ttu-id="29b85-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="29b85-127">Requirement</span></span> | <span data-ttu-id="29b85-128">Valore</span><span class="sxs-lookup"><span data-stu-id="29b85-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29b85-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29b85-129">Header</span></span><br/>  | <dl> <span data-ttu-id="29b85-130"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="29b85-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="29b85-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="29b85-131">Library</span></span><br/> | <dl> <span data-ttu-id="29b85-132"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="29b85-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="29b85-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29b85-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29b85-134">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="29b85-134">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
