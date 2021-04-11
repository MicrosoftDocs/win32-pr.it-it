---
description: Determina se un raggio interseca il volume del rettangolo di delimitazione di una casella.
ms.assetid: 45ff8540-ed5c-4f54-b3b7-3385087a6863
title: Funzione D3DXBoxBoundProbe (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBoxBoundProbe
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 707ab21a3babe7d9a93f776f438cbaab7137849b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132354"
---
# <a name="d3dxboxboundprobe-function"></a><span data-ttu-id="ad05e-103">D3DXBoxBoundProbe (funzione)</span><span class="sxs-lookup"><span data-stu-id="ad05e-103">D3DXBoxBoundProbe function</span></span>

<span data-ttu-id="ad05e-104">Determina se un raggio interseca il volume del rettangolo di delimitazione di una casella.</span><span class="sxs-lookup"><span data-stu-id="ad05e-104">Determines whether a ray intersects the volume of a box's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad05e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad05e-105">Syntax</span></span>


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="ad05e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad05e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad05e-107">*pMin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad05e-107">*pMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad05e-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad05e-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ad05e-109">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che descrive l'angolo inferiore sinistro del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="ad05e-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the lower-left corner of the bounding box.</span></span> <span data-ttu-id="ad05e-110">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ad05e-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ad05e-111">*pMax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad05e-111">*pMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad05e-112">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad05e-112">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ad05e-113">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che descrive l'angolo superiore destro del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="ad05e-113">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the upper-right corner of the bounding box.</span></span> <span data-ttu-id="ad05e-114">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ad05e-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ad05e-115">*pRayPosition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad05e-115">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad05e-116">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad05e-116">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ad05e-117">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica la coordinata di origine del raggio.</span><span class="sxs-lookup"><span data-stu-id="ad05e-117">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="ad05e-118">*pRayDirection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad05e-118">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad05e-119">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad05e-119">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ad05e-120">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica la direzione del raggio.</span><span class="sxs-lookup"><span data-stu-id="ad05e-120">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="ad05e-121">Questo vettore non deve essere (0, 0, 0) ma non deve essere normalizzato.</span><span class="sxs-lookup"><span data-stu-id="ad05e-121">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad05e-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad05e-122">Return value</span></span>

<span data-ttu-id="ad05e-123">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad05e-123">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad05e-124">Restituisce **true** se il raggio interseca il volume del rettangolo di delimitazione della casella.</span><span class="sxs-lookup"><span data-stu-id="ad05e-124">Returns **TRUE** if the ray intersects the volume of the box's bounding box.</span></span> <span data-ttu-id="ad05e-125">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="ad05e-125">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad05e-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad05e-126">Remarks</span></span>

<span data-ttu-id="ad05e-127">**D3DXboxBoundProbe** determina se il raggio interseca il volume del rettangolo di delimitazione della casella, non solo la superficie della casella.</span><span class="sxs-lookup"><span data-stu-id="ad05e-127">**D3DXboxBoundProbe** determines if the ray intersects the volume of the box's bounding box, not just the surface of the box.</span></span>

<span data-ttu-id="ad05e-128">I valori passati a **D3DXboxBoundProbe** sono xmin, Xmax, ymin, ymax, zmin e Zmax.</span><span class="sxs-lookup"><span data-stu-id="ad05e-128">The values passed to **D3DXboxBoundProbe** are xmin, xmax, ymin, ymax, zmin, and zmax.</span></span> <span data-ttu-id="ad05e-129">Pertanto, di seguito vengono definiti gli angoli del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="ad05e-129">Thus, the following defines the corners of the bounding box.</span></span>


```
xmax, ymax, zmax
xmax, ymax, zmin
xmax, ymin, zmax
xmax, ymin, zmin
xmin, ymax, zmax
xmin, ymax, zmin
xmin, ymin, zmax
xmin, ymin, zmin
```



<span data-ttu-id="ad05e-130">La profondità del rettangolo di delimitazione nella direzione z è zmax-zmin, nella direzione y è ymax-ymin e nella direzione x è xmax-xmin.</span><span class="sxs-lookup"><span data-stu-id="ad05e-130">The depth of the bounding box in the z direction is zmax - zmin, in the y direction is ymax - ymin, and in the x direction is xmax - xmin.</span></span> <span data-ttu-id="ad05e-131">Con i vettori minimi e massimi seguenti, ad esempio, min (-1,-1,-1) e Max (1, 1, 1), il rettangolo di delimitazione viene definito nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="ad05e-131">For example, with the following minimum and maximum vectors, min (-1, -1, -1) and max (1, 1, 1), the bounding box is defined in the following manner.</span></span>


```
 1,  1,  1
 1,  1, -1
 1, -1,  1
 1, -1, -1
-1,  1,  1
-1,  1, -1
-1, -1,  1
-1, -1, -l
```



## <a name="requirements"></a><span data-ttu-id="ad05e-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad05e-132">Requirements</span></span>



| <span data-ttu-id="ad05e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad05e-133">Requirement</span></span> | <span data-ttu-id="ad05e-134">Valore</span><span class="sxs-lookup"><span data-stu-id="ad05e-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad05e-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad05e-135">Header</span></span><br/>  | <dl> <span data-ttu-id="ad05e-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad05e-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ad05e-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="ad05e-137">Library</span></span><br/> | <dl> <span data-ttu-id="ad05e-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad05e-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ad05e-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad05e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad05e-140">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="ad05e-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="ad05e-141">**D3DXComputeBoundingBox**</span><span class="sxs-lookup"><span data-stu-id="ad05e-141">**D3DXComputeBoundingBox**</span></span>](d3dxcomputeboundingbox.md)
</dt> </dl>

 

 
