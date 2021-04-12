---
description: Struttura che contiene gli attributi di una mesh di patch.
ms.assetid: aaea69c9-2d33-46e8-bc26-95daf65abf50
title: Struttura D3DXPATCHINFO (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 8628cc27a0223580aa1f8072750f4c31a176533e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354144"
---
# <a name="d3dxpatchinfo-structure"></a><span data-ttu-id="a3e1d-103">Struttura D3DXPATCHINFO</span><span class="sxs-lookup"><span data-stu-id="a3e1d-103">D3DXPATCHINFO structure</span></span>

<span data-ttu-id="a3e1d-104">Struttura che contiene gli attributi di una mesh di patch.</span><span class="sxs-lookup"><span data-stu-id="a3e1d-104">Structure that contains the attributes of a patch mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e1d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3e1d-105">Syntax</span></span>


```C++
typedef struct D3DXPATCHINFO {
  D3DXPATCHMESHTYPE PatchType;
  D3DDEGREETYPE     Degree;
  D3DBASISTYPE      Basis;
} D3DXPATCHINFO, *LPD3DXPATCHINFO;
```



## <a name="members"></a><span data-ttu-id="a3e1d-106">Members</span><span class="sxs-lookup"><span data-stu-id="a3e1d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a3e1d-107">**PatchType**</span><span class="sxs-lookup"><span data-stu-id="a3e1d-107">**PatchType**</span></span>
</dt> <dd>

<span data-ttu-id="a3e1d-108">Tipo: **[ **D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**</span><span class="sxs-lookup"><span data-stu-id="a3e1d-108">Type: **[**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a3e1d-109">Tipo di patch.</span><span class="sxs-lookup"><span data-stu-id="a3e1d-109">The patch type.</span></span> <span data-ttu-id="a3e1d-110">Per informazioni sui tipi di patch, vedere [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).</span><span class="sxs-lookup"><span data-stu-id="a3e1d-110">For information about patch types, see [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3e1d-111">**Gradi**</span><span class="sxs-lookup"><span data-stu-id="a3e1d-111">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="a3e1d-112">Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="a3e1d-112">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a3e1d-113">Grado delle curve usate per costruire la patch.</span><span class="sxs-lookup"><span data-stu-id="a3e1d-113">Degree of the curves used to construct the patch.</span></span> <span data-ttu-id="a3e1d-114">Per informazioni sui gradi supportati, vedere [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="a3e1d-114">For information about the degrees supported, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3e1d-115">**Basis**</span><span class="sxs-lookup"><span data-stu-id="a3e1d-115">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="a3e1d-116">Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="a3e1d-116">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a3e1d-117">Tipo di curva utilizzata per costruire la patch.</span><span class="sxs-lookup"><span data-stu-id="a3e1d-117">Type of curve used to construct the patch.</span></span> <span data-ttu-id="a3e1d-118">Per informazioni sui tipi di base supportati, vedere [**D3DBASISTYPE**](./d3dbasistype.md).</span><span class="sxs-lookup"><span data-stu-id="a3e1d-118">For information about the basis types supported, see [**D3DBASISTYPE**](./d3dbasistype.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3e1d-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3e1d-119">Remarks</span></span>

<span data-ttu-id="a3e1d-120">Una mesh è un set di visi, ciascuno dei quali è descritto da un semplice poligono.</span><span class="sxs-lookup"><span data-stu-id="a3e1d-120">A mesh is a set of faces, each of which is described by a simple polygon.</span></span> <span data-ttu-id="a3e1d-121">È possibile creare oggetti connettendosi tra loro diverse mesh.</span><span class="sxs-lookup"><span data-stu-id="a3e1d-121">Objects can be created by connecting several meshes together.</span></span> <span data-ttu-id="a3e1d-122">Una mesh patch viene costruita dalle patch.</span><span class="sxs-lookup"><span data-stu-id="a3e1d-122">A patch mesh is constructed from patches.</span></span> <span data-ttu-id="a3e1d-123">Una patch è una parte di geometria a quattro lati costruita dalle curve.</span><span class="sxs-lookup"><span data-stu-id="a3e1d-123">A patch is a four-sided piece of geometry constructed from curves.</span></span> <span data-ttu-id="a3e1d-124">Il tipo di curva usato e l'ordine della curva possono essere variati in modo che l'area della patch possa adattarsi quasi a qualsiasi forma di superficie.</span><span class="sxs-lookup"><span data-stu-id="a3e1d-124">The type of curve used and the order of the curve can be varied so that the patch surface will fit almost any surface shape.</span></span>

<span data-ttu-id="a3e1d-125">Sono supportati i tipi di combinazioni di patch seguenti:</span><span class="sxs-lookup"><span data-stu-id="a3e1d-125">The following types of patch combinations are supported:</span></span>



| <span data-ttu-id="a3e1d-126">Tipo di patch</span><span class="sxs-lookup"><span data-stu-id="a3e1d-126">Patch Type</span></span> | <span data-ttu-id="a3e1d-127">Base</span><span class="sxs-lookup"><span data-stu-id="a3e1d-127">Basis</span></span>       | <span data-ttu-id="a3e1d-128">Gradi</span><span class="sxs-lookup"><span data-stu-id="a3e1d-128">Degree</span></span> |
|------------|-------------|--------|
| <span data-ttu-id="a3e1d-129">Rettangolo</span><span class="sxs-lookup"><span data-stu-id="a3e1d-129">Rectangle</span></span>  | <span data-ttu-id="a3e1d-130">Bézier</span><span class="sxs-lookup"><span data-stu-id="a3e1d-130">Bezier</span></span>      | <span data-ttu-id="a3e1d-131">2, 3, 5</span><span class="sxs-lookup"><span data-stu-id="a3e1d-131">2,3,5</span></span>  |
| <span data-ttu-id="a3e1d-132">Rettangolo</span><span class="sxs-lookup"><span data-stu-id="a3e1d-132">Rectangle</span></span>  | <span data-ttu-id="a3e1d-133">Spline B</span><span class="sxs-lookup"><span data-stu-id="a3e1d-133">B-Spline</span></span>    | <span data-ttu-id="a3e1d-134">2, 3, 5</span><span class="sxs-lookup"><span data-stu-id="a3e1d-134">2,3,5</span></span>  |
| <span data-ttu-id="a3e1d-135">Rettangolo</span><span class="sxs-lookup"><span data-stu-id="a3e1d-135">Rectangle</span></span>  | <span data-ttu-id="a3e1d-136">Catmull-Rom</span><span class="sxs-lookup"><span data-stu-id="a3e1d-136">Catmull-Rom</span></span> | <span data-ttu-id="a3e1d-137">3</span><span class="sxs-lookup"><span data-stu-id="a3e1d-137">3</span></span>      |
| <span data-ttu-id="a3e1d-138">Triangle</span><span class="sxs-lookup"><span data-stu-id="a3e1d-138">Triangle</span></span>   | <span data-ttu-id="a3e1d-139">Bézier</span><span class="sxs-lookup"><span data-stu-id="a3e1d-139">Bezier</span></span>      | <span data-ttu-id="a3e1d-140">2, 3, 5</span><span class="sxs-lookup"><span data-stu-id="a3e1d-140">2,3,5</span></span>  |
| <span data-ttu-id="a3e1d-141">N-patch</span><span class="sxs-lookup"><span data-stu-id="a3e1d-141">N-patch</span></span>    | <span data-ttu-id="a3e1d-142">N/D</span><span class="sxs-lookup"><span data-stu-id="a3e1d-142">N/A</span></span>         | <span data-ttu-id="a3e1d-143">3</span><span class="sxs-lookup"><span data-stu-id="a3e1d-143">3</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="a3e1d-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3e1d-144">Requirements</span></span>



| <span data-ttu-id="a3e1d-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3e1d-145">Requirement</span></span> | <span data-ttu-id="a3e1d-146">Valore</span><span class="sxs-lookup"><span data-stu-id="a3e1d-146">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e1d-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3e1d-147">Header</span></span><br/> | <dl> <span data-ttu-id="a3e1d-148"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3e1d-148"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3e1d-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3e1d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3e1d-150">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="a3e1d-150">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="a3e1d-151">**\_Informazioni D3DRECTPATCH**</span><span class="sxs-lookup"><span data-stu-id="a3e1d-151">**D3DRECTPATCH\_INFO**</span></span>](d3drectpatch-info.md)
</dt> <dt>

[<span data-ttu-id="a3e1d-152">**\_Informazioni D3DTRIPATCH**</span><span class="sxs-lookup"><span data-stu-id="a3e1d-152">**D3DTRIPATCH\_INFO**</span></span>](d3dtripatch-info.md)
</dt> <dt>

[<span data-ttu-id="a3e1d-153">**D3DXCreatePatchMesh**</span><span class="sxs-lookup"><span data-stu-id="a3e1d-153">**D3DXCreatePatchMesh**</span></span>](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
