---
description: La funzione D3DXBoxBoundProbe (D3DX10math. h) determina se un raggio interseca il volume del rettangolo di delimitazione di una casella.
ms.assetid: d3cdcf89-461b-44b0-b5d0-ca2e3869a5ad
title: Funzione D3DXBoxBoundProbe (D3DX10math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e1a8d1a7b879814cff43e31b060cc2af53167818
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334338"
---
# <a name="d3dxboxboundprobe-function-d3dx10mathh"></a><span data-ttu-id="2b794-103">Funzione D3DXBoxBoundProbe (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="2b794-103">D3DXBoxBoundProbe function (D3DX10math.h)</span></span>

<span data-ttu-id="2b794-104">Determina se un raggio interseca il volume del rettangolo di delimitazione di una casella.</span><span class="sxs-lookup"><span data-stu-id="2b794-104">Determines whether a ray intersects the volume of a box's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b794-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b794-105">Syntax</span></span>


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="2b794-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b794-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b794-107">*pMin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b794-107">*pMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b794-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b794-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2b794-109">Puntatore a un [**D3DXVECTOR3**](d3d10-d3dxvector3.md)che descrive l'angolo inferiore sinistro del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="2b794-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), describing the lower-left corner of the bounding box.</span></span> <span data-ttu-id="2b794-110">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="2b794-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2b794-111">*pMax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b794-111">*pMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b794-112">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b794-112">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2b794-113">Puntatore a una struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che descrive l'angolo superiore destro del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="2b794-113">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the upper-right corner of the bounding box.</span></span> <span data-ttu-id="2b794-114">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="2b794-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2b794-115">*pRayPosition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b794-115">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b794-116">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b794-116">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2b794-117">Puntatore a una struttura D3DXVECTOR3, che specifica la coordinata di origine del raggio.</span><span class="sxs-lookup"><span data-stu-id="2b794-117">Pointer to a D3DXVECTOR3 structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="2b794-118">*pRayDirection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b794-118">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b794-119">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b794-119">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2b794-120">Puntatore a una struttura D3DXVECTOR3, che specifica la direzione del raggio.</span><span class="sxs-lookup"><span data-stu-id="2b794-120">Pointer to a D3DXVECTOR3 structure, specifying the direction of the ray.</span></span> <span data-ttu-id="2b794-121">Questo vettore non deve essere (0, 0, 0) ma non deve essere normalizzato.</span><span class="sxs-lookup"><span data-stu-id="2b794-121">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b794-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b794-122">Return value</span></span>

<span data-ttu-id="2b794-123">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b794-123">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b794-124">Restituisce **true** se il raggio interseca il volume del rettangolo di delimitazione della casella.</span><span class="sxs-lookup"><span data-stu-id="2b794-124">Returns **TRUE** if the ray intersects the volume of the box's bounding box.</span></span> <span data-ttu-id="2b794-125">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="2b794-125">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b794-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b794-126">Remarks</span></span>

<span data-ttu-id="2b794-127">**D3DXBoxBoundProbe** determina se il raggio interseca il volume del rettangolo di delimitazione della casella, non solo la superficie della casella.</span><span class="sxs-lookup"><span data-stu-id="2b794-127">**D3DXBoxBoundProbe** determines if the ray intersects the volume of the box's bounding box, not just the surface of the box.</span></span>

<span data-ttu-id="2b794-128">I valori passati a **D3DXBoxBoundProbe** sono xmin, Xmax, ymin, ymax, zmin e Zmax.</span><span class="sxs-lookup"><span data-stu-id="2b794-128">The values passed to **D3DXBoxBoundProbe** are xmin, xmax, ymin, ymax, zmin, and zmax.</span></span> <span data-ttu-id="2b794-129">Pertanto, di seguito vengono definiti gli angoli del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="2b794-129">Thus, the following defines the corners of the bounding box.</span></span>


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



<span data-ttu-id="2b794-130">La profondità del rettangolo di delimitazione nella direzione z è zmax-zmin, nella direzione y è ymax-ymin e nella direzione x è xmax-xmin.</span><span class="sxs-lookup"><span data-stu-id="2b794-130">The depth of the bounding box in the z direction is zmax - zmin, in the y direction is ymax - ymin, and in the x direction is xmax - xmin.</span></span> <span data-ttu-id="2b794-131">Con i vettori minimi e massimi seguenti, ad esempio, min (-1,-1,-1) e Max (1, 1, 1), il rettangolo di delimitazione viene definito nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="2b794-131">For example, with the following minimum and maximum vectors, min (-1, -1, -1) and max (1, 1, 1), the bounding box is defined in the following manner.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2b794-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b794-132">Requirements</span></span>



| <span data-ttu-id="2b794-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b794-133">Requirement</span></span> | <span data-ttu-id="2b794-134">Valore</span><span class="sxs-lookup"><span data-stu-id="2b794-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b794-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b794-135">Header</span></span>  | <span data-ttu-id="2b794-136">D3DX10math. h</span><span class="sxs-lookup"><span data-stu-id="2b794-136">D3DX10math.h</span></span> |
| <span data-ttu-id="2b794-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="2b794-137">Library</span></span> | <span data-ttu-id="2b794-138">D3DX10. lib</span><span class="sxs-lookup"><span data-stu-id="2b794-138">D3DX10.lib</span></span>  |



## <a name="see-also"></a><span data-ttu-id="2b794-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b794-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b794-140">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="2b794-140">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
