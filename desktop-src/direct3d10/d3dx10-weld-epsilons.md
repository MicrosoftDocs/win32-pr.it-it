---
description: Specifica i valori di tolleranza per ogni componente vertex quando si confrontano i vertici per determinare se sono abbastanza simili per essere saldati insieme.
ms.assetid: b28a17bd-5d5b-41b3-86d9-327f5497fc94
title: Struttura D3DX10_WELD_EPSILONS (D3DX10. h)
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
ms.openlocfilehash: c72f63e3ecef1fdb193fcaec9220f9768204d099
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322984"
---
# <a name="d3dx10_weld_epsilons-structure"></a><span data-ttu-id="4ebcb-103">\_Struttura di \_ Epsilon d3dx10 Weld</span><span class="sxs-lookup"><span data-stu-id="4ebcb-103">D3DX10\_WELD\_EPSILONS structure</span></span>

<span data-ttu-id="4ebcb-104">Specifica i valori di tolleranza per ogni componente vertex quando si confrontano i vertici per determinare se sono abbastanza simili per essere saldati insieme.</span><span class="sxs-lookup"><span data-stu-id="4ebcb-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ebcb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ebcb-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="4ebcb-106">Members</span><span class="sxs-lookup"><span data-stu-id="4ebcb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4ebcb-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="4ebcb-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4ebcb-109">Posizione</span><span class="sxs-lookup"><span data-stu-id="4ebcb-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="4ebcb-110">**BlendWeights**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="4ebcb-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4ebcb-112">Spessore di Blend</span><span class="sxs-lookup"><span data-stu-id="4ebcb-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="4ebcb-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="4ebcb-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4ebcb-115">Normale</span><span class="sxs-lookup"><span data-stu-id="4ebcb-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="4ebcb-116">**PSize**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="4ebcb-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4ebcb-118">Valore dimensioni punto</span><span class="sxs-lookup"><span data-stu-id="4ebcb-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="4ebcb-119">**Speculare**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="4ebcb-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4ebcb-121">Valore di illuminazione speculare</span><span class="sxs-lookup"><span data-stu-id="4ebcb-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="4ebcb-122">**Diffusa**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="4ebcb-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4ebcb-124">Valore di illuminazione diffusa</span><span class="sxs-lookup"><span data-stu-id="4ebcb-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="4ebcb-125">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="4ebcb-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4ebcb-127">Otto coordinate di trama</span><span class="sxs-lookup"><span data-stu-id="4ebcb-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="4ebcb-128">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="4ebcb-129">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4ebcb-130">Tangente</span><span class="sxs-lookup"><span data-stu-id="4ebcb-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="4ebcb-131">**Binormale**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="4ebcb-132">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4ebcb-133">Binormale</span><span class="sxs-lookup"><span data-stu-id="4ebcb-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="4ebcb-134">**TessFactor**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="4ebcb-135">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ebcb-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4ebcb-136">Fattore a mosaico</span><span class="sxs-lookup"><span data-stu-id="4ebcb-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ebcb-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ebcb-137">Remarks</span></span>

<span data-ttu-id="4ebcb-138">Il tipo LPD3DXWeldEpsilons è definito come un puntatore alla struttura D3DXWeldEpsilons.</span><span class="sxs-lookup"><span data-stu-id="4ebcb-138">The LPD3DXWeldEpsilons type is defined as a pointer to the D3DXWeldEpsilons structure.</span></span>


```
typedef D3DX_WELD_EPSILONS *LPD3DX_WELD_EPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="4ebcb-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ebcb-139">Requirements</span></span>



| <span data-ttu-id="4ebcb-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ebcb-140">Requirement</span></span> | <span data-ttu-id="4ebcb-141">Valore</span><span class="sxs-lookup"><span data-stu-id="4ebcb-141">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4ebcb-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ebcb-142">Header</span></span><br/> | <dl> <span data-ttu-id="4ebcb-143"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ebcb-143"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ebcb-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ebcb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ebcb-145">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="4ebcb-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
