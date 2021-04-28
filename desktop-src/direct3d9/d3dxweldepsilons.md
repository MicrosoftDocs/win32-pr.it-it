---
description: 'Struttura D3DXWELDEPSILONS: specifica i valori di tolleranza per ogni componente vertice durante il confronto dei vertici per determinare se sono abbastanza simili da essere uniti.'
ms.assetid: 534903da-ff65-4629-9be9-66c9daed6ef5
title: Struttura D3DXWELDEPSILONS (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWELDEPSILONS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: bb11e6f5481b1adf7cc1bac58edf40d4ac770e92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115499"
---
# <a name="d3dxweldepsilons-structure"></a><span data-ttu-id="e6e88-103">Struttura D3DXWELDEPSILONS</span><span class="sxs-lookup"><span data-stu-id="e6e88-103">D3DXWELDEPSILONS structure</span></span>

<span data-ttu-id="e6e88-104">Specifica i valori di tolleranza per ogni componente vertice durante il confronto dei vertici per determinare se sono sufficientemente simili da essere uniti.</span><span class="sxs-lookup"><span data-stu-id="e6e88-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e88-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6e88-105">Syntax</span></span>


```C++
typedef struct _D3DXWELDEPSILONS {
  FLOAT Position;
  FLOAT BlendWeights;
  FLOAT Normal;
  FLOAT PSize;
  FLOAT Specular;
  FLOAT Diffuse;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
  FLOAT TessFactor;
} D3DXWELDEPSILONS, *LPD3DXWELDEPSILONS;
```



## <a name="members"></a><span data-ttu-id="e6e88-106">Members</span><span class="sxs-lookup"><span data-stu-id="e6e88-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e6e88-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="e6e88-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="e6e88-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6e88-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e6e88-109">Posizione</span><span class="sxs-lookup"><span data-stu-id="e6e88-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="e6e88-110">**BlendWeights**</span><span class="sxs-lookup"><span data-stu-id="e6e88-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="e6e88-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6e88-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e6e88-112">Spessore di blend</span><span class="sxs-lookup"><span data-stu-id="e6e88-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="e6e88-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="e6e88-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="e6e88-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6e88-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e6e88-115">Normale</span><span class="sxs-lookup"><span data-stu-id="e6e88-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="e6e88-116">**PSize**</span><span class="sxs-lookup"><span data-stu-id="e6e88-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="e6e88-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6e88-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e6e88-118">Valore delle dimensioni in punti</span><span class="sxs-lookup"><span data-stu-id="e6e88-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="e6e88-119">**Speculare**</span><span class="sxs-lookup"><span data-stu-id="e6e88-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="e6e88-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6e88-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e6e88-121">Valore di illuminazione speculare</span><span class="sxs-lookup"><span data-stu-id="e6e88-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="e6e88-122">**Diffusa**</span><span class="sxs-lookup"><span data-stu-id="e6e88-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="e6e88-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6e88-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e6e88-124">Valore di illuminazione diffusa</span><span class="sxs-lookup"><span data-stu-id="e6e88-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="e6e88-125">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="e6e88-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="e6e88-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6e88-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e6e88-127">Otto coordinate di trama</span><span class="sxs-lookup"><span data-stu-id="e6e88-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="e6e88-128">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="e6e88-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="e6e88-129">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6e88-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e6e88-130">Tangente</span><span class="sxs-lookup"><span data-stu-id="e6e88-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="e6e88-131">**Binormale**</span><span class="sxs-lookup"><span data-stu-id="e6e88-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="e6e88-132">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6e88-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e6e88-133">Binormale</span><span class="sxs-lookup"><span data-stu-id="e6e88-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="e6e88-134">**TessFactor**</span><span class="sxs-lookup"><span data-stu-id="e6e88-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="e6e88-135">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6e88-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e6e88-136">Fattore a tessellazione</span><span class="sxs-lookup"><span data-stu-id="e6e88-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6e88-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6e88-137">Remarks</span></span>

<span data-ttu-id="e6e88-138">Il tipo LPD3DXWELDEPSILONS viene definito come puntatore alla **struttura D3DXWELDEPSILONS.**</span><span class="sxs-lookup"><span data-stu-id="e6e88-138">The LPD3DXWELDEPSILONS type is defined as a pointer to the **D3DXWELDEPSILONS** structure.</span></span>


```
typedef D3DXWELDEPSILONS *LPD3DXWELDEPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="e6e88-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6e88-139">Requirements</span></span>



| <span data-ttu-id="e6e88-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6e88-140">Requirement</span></span> | <span data-ttu-id="e6e88-141">Valore</span><span class="sxs-lookup"><span data-stu-id="e6e88-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e88-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6e88-142">Header</span></span><br/> | <dl> <span data-ttu-id="e6e88-143"><dt>D3dx9mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="e6e88-143"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6e88-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6e88-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e88-145">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="e6e88-145">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="e6e88-146">**D3DXWeldVertices**</span><span class="sxs-lookup"><span data-stu-id="e6e88-146">**D3DXWeldVertices**</span></span>](d3dxweldvertices.md)
</dt> </dl>

 

 
