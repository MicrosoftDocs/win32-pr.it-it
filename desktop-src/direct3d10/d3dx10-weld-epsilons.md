---
description: 'D3DX10_WELD_EPSILONS struttura : specifica i valori di tolleranza per ogni componente vertice durante il confronto dei vertici per determinare se sono sufficientemente simili da essere uniti.'
ms.assetid: b28a17bd-5d5b-41b3-86d9-327f5497fc94
title: D3DX10_WELD_EPSILONS struttura (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_WELD_EPSILONS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 720a10dbe4b22b69910d88d3c03cea9ded768f1b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105429"
---
# <a name="d3dx10_weld_epsilons-structure"></a><span data-ttu-id="62e96-103">Struttura \_ EPSILONS D3DX10 WELD \_</span><span class="sxs-lookup"><span data-stu-id="62e96-103">D3DX10\_WELD\_EPSILONS structure</span></span>

<span data-ttu-id="62e96-104">Specifica i valori di tolleranza per ogni componente vertice durante il confronto dei vertici per determinare se sono sufficientemente simili da essere uniti.</span><span class="sxs-lookup"><span data-stu-id="62e96-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="62e96-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62e96-105">Syntax</span></span>


```C++
typedef struct D3DX10_WELD_EPSILONS {
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
} D3DX10_WELD_EPSILONS, *LPD3DX10_WELD_EPSILONS;
```



## <a name="members"></a><span data-ttu-id="62e96-106">Members</span><span class="sxs-lookup"><span data-stu-id="62e96-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="62e96-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="62e96-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="62e96-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62e96-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="62e96-109">Posizione</span><span class="sxs-lookup"><span data-stu-id="62e96-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="62e96-110">**BlendWeights**</span><span class="sxs-lookup"><span data-stu-id="62e96-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="62e96-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62e96-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="62e96-112">Spessore di blend</span><span class="sxs-lookup"><span data-stu-id="62e96-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="62e96-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="62e96-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="62e96-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62e96-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="62e96-115">Normale</span><span class="sxs-lookup"><span data-stu-id="62e96-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="62e96-116">**PSize**</span><span class="sxs-lookup"><span data-stu-id="62e96-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="62e96-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62e96-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="62e96-118">Valore delle dimensioni in punti</span><span class="sxs-lookup"><span data-stu-id="62e96-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="62e96-119">**Speculare**</span><span class="sxs-lookup"><span data-stu-id="62e96-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="62e96-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62e96-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="62e96-121">Valore di illuminazione speculare</span><span class="sxs-lookup"><span data-stu-id="62e96-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="62e96-122">**Diffusa**</span><span class="sxs-lookup"><span data-stu-id="62e96-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="62e96-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62e96-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="62e96-124">Valore di illuminazione diffusa</span><span class="sxs-lookup"><span data-stu-id="62e96-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="62e96-125">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="62e96-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="62e96-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62e96-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="62e96-127">Otto coordinate di trama</span><span class="sxs-lookup"><span data-stu-id="62e96-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="62e96-128">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="62e96-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="62e96-129">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62e96-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="62e96-130">Tangente</span><span class="sxs-lookup"><span data-stu-id="62e96-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="62e96-131">**Binormale**</span><span class="sxs-lookup"><span data-stu-id="62e96-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="62e96-132">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62e96-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="62e96-133">Binormale</span><span class="sxs-lookup"><span data-stu-id="62e96-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="62e96-134">**TessFactor**</span><span class="sxs-lookup"><span data-stu-id="62e96-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="62e96-135">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62e96-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="62e96-136">Fattore a tessellazione</span><span class="sxs-lookup"><span data-stu-id="62e96-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62e96-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="62e96-137">Remarks</span></span>

<span data-ttu-id="62e96-138">Il tipo LPD3DXWeldEpsilons è definito come puntatore alla struttura D3DXWeldEpsilons.</span><span class="sxs-lookup"><span data-stu-id="62e96-138">The LPD3DXWeldEpsilons type is defined as a pointer to the D3DXWeldEpsilons structure.</span></span>


```
typedef D3DX_WELD_EPSILONS *LPD3DX_WELD_EPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="62e96-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62e96-139">Requirements</span></span>



| <span data-ttu-id="62e96-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="62e96-140">Requirement</span></span> | <span data-ttu-id="62e96-141">Valore</span><span class="sxs-lookup"><span data-stu-id="62e96-141">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="62e96-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62e96-142">Header</span></span><br/> | <dl> <span data-ttu-id="62e96-143"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="62e96-143"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62e96-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62e96-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62e96-145">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="62e96-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
