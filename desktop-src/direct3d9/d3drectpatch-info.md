---
description: Descrive una patch di ordine superiore rettangolare.
ms.assetid: 5f195009-d047-4dc0-a386-e1a434914e34
title: Struttura D3DRECTPATCH_INFO (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECTPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a2b7fedbaac2cc9c204d4691828d31794cea1f47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322915"
---
# <a name="d3drectpatch_info-structure"></a><span data-ttu-id="b4604-103">Struttura delle informazioni di D3DRECTPATCH \_</span><span class="sxs-lookup"><span data-stu-id="b4604-103">D3DRECTPATCH\_INFO structure</span></span>

<span data-ttu-id="b4604-104">Descrive una patch di ordine superiore rettangolare.</span><span class="sxs-lookup"><span data-stu-id="b4604-104">Describes a rectangular high-order patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4604-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4604-105">Syntax</span></span>


```C++
typedef struct D3DRECTPATCH_INFO {
  UINT          StartVertexOffsetWidth;
  UINT          StartVertexOffsetHeight;
  UINT          Width;
  UINT          Height;
  UINT          Stride;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DRECTPATCH_INFO, *LPD3DRECTPATCH_INFO;
```



## <a name="members"></a><span data-ttu-id="b4604-106">Members</span><span class="sxs-lookup"><span data-stu-id="b4604-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b4604-107">**StartVertexOffsetWidth**</span><span class="sxs-lookup"><span data-stu-id="b4604-107">**StartVertexOffsetWidth**</span></span>
</dt> <dd>

<span data-ttu-id="b4604-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4604-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4604-109">Spessore iniziale dell'offset del vertice, in numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="b4604-109">Starting vertex offset width, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="b4604-110">**StartVertexOffsetHeight**</span><span class="sxs-lookup"><span data-stu-id="b4604-110">**StartVertexOffsetHeight**</span></span>
</dt> <dd>

<span data-ttu-id="b4604-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4604-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4604-112">Altezza dell'offset del vertice iniziale, in numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="b4604-112">Starting vertex offset height, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="b4604-113">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="b4604-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="b4604-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4604-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4604-115">Larghezza di ogni vertice, in numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="b4604-115">Width of each vertex, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="b4604-116">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="b4604-116">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="b4604-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4604-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4604-118">Altezza di ogni vertice, in numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="b4604-118">Height of each vertex, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="b4604-119">**Stride**</span><span class="sxs-lookup"><span data-stu-id="b4604-119">**Stride**</span></span>
</dt> <dd>

<span data-ttu-id="b4604-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4604-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4604-121">Larghezza della matrice di vertici bidimensionali immaginaria, che occupa lo stesso spazio del buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="b4604-121">Width of the imaginary two-dimensional vertex array, which occupies the same space as the vertex buffer.</span></span> <span data-ttu-id="b4604-122">Per un esempio, vedere il diagramma riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="b4604-122">For an example, see the diagram below.</span></span>

</dd> <dt>

<span data-ttu-id="b4604-123">**Basis**</span><span class="sxs-lookup"><span data-stu-id="b4604-123">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="b4604-124">Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="b4604-124">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4604-125">Membro del tipo enumerato [**D3DBASISTYPE**](./d3dbasistype.md) , che definisce il tipo di base per la patch di ordine superiore rettangolare.</span><span class="sxs-lookup"><span data-stu-id="b4604-125">Member of the [**D3DBASISTYPE**](./d3dbasistype.md) enumerated type, defining the basis type for the rectangular high-order patch.</span></span>



| <span data-ttu-id="b4604-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b4604-126">Value</span></span>                 | <span data-ttu-id="b4604-127">Ordine supportato</span><span class="sxs-lookup"><span data-stu-id="b4604-127">Order supported</span></span>            | <span data-ttu-id="b4604-128">Larghezza e altezza</span><span class="sxs-lookup"><span data-stu-id="b4604-128">Width and height</span></span>                  |
|-----------------------|----------------------------|-----------------------------------|
| <span data-ttu-id="b4604-129">D3DBASIS \_ Bezier</span><span class="sxs-lookup"><span data-stu-id="b4604-129">D3DBASIS\_BEZIER</span></span>      | <span data-ttu-id="b4604-130">Lineare, cubica e Quinta</span><span class="sxs-lookup"><span data-stu-id="b4604-130">Linear, cubic, and quintic</span></span> | <span data-ttu-id="b4604-131">Width = Height = (DWORD) Order + 1</span><span class="sxs-lookup"><span data-stu-id="b4604-131">Width = height = (DWORD)order + 1</span></span> |
| <span data-ttu-id="b4604-132">\_Perequazione BSpline D3DBASIS</span><span class="sxs-lookup"><span data-stu-id="b4604-132">D3DBASIS\_BSPLINE</span></span>     | <span data-ttu-id="b4604-133">Lineare, cubica e Quinta</span><span class="sxs-lookup"><span data-stu-id="b4604-133">Linear, cubic, and quintic</span></span> | <span data-ttu-id="b4604-134">Width = ordine altezza > (DWORD)</span><span class="sxs-lookup"><span data-stu-id="b4604-134">Width = height > (DWORD)order</span></span>  |
| <span data-ttu-id="b4604-135">\_Interpolazione D3DBASIS</span><span class="sxs-lookup"><span data-stu-id="b4604-135">D3DBASIS\_INTERPOLATE</span></span> | <span data-ttu-id="b4604-136">Cubi</span><span class="sxs-lookup"><span data-stu-id="b4604-136">Cubic</span></span>                      | <span data-ttu-id="b4604-137">Width = ordine altezza > (DWORD)</span><span class="sxs-lookup"><span data-stu-id="b4604-137">Width = height > (DWORD)order</span></span>  |



 

</dd> <dt>

<span data-ttu-id="b4604-138">**Gradi**</span><span class="sxs-lookup"><span data-stu-id="b4604-138">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="b4604-139">Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="b4604-139">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4604-140">Membro del tipo enumerato [**D3DDEGREETYPE**](./d3ddegreetype.md) , che definisce il grado per la patch rettangolare.</span><span class="sxs-lookup"><span data-stu-id="b4604-140">Member of the [**D3DDEGREETYPE**](./d3ddegreetype.md) enumerated type, defining the degree for the rectangular patch.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4604-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4604-141">Remarks</span></span>

<span data-ttu-id="b4604-142">Il diagramma seguente identifica i parametri che specificano una patch rettangolo.</span><span class="sxs-lookup"><span data-stu-id="b4604-142">The following diagram identifies the parameters that specify a rectangle patch.</span></span>

![diagramma di una patch di ordine superiore rettangolare e dei parametri che lo specificano](images/hop-rectpatch.png)

<span data-ttu-id="b4604-144">Ognuno dei vertici nel buffer del vertice viene visualizzato come un punto nero.</span><span class="sxs-lookup"><span data-stu-id="b4604-144">Each of the vertices in the vertex buffer is shown as a black dot.</span></span> <span data-ttu-id="b4604-145">In questo caso, il buffer dei vertici contiene 20 vertici, 16 dei quali si trovano nella patch del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="b4604-145">In this case, the vertex buffer has 20 vertices in it, 16 of which are in the rectangle patch.</span></span> <span data-ttu-id="b4604-146">Lo stride è il numero di vertici nella larghezza del buffer dei vertici, in questo caso cinque.</span><span class="sxs-lookup"><span data-stu-id="b4604-146">The stride is the number of vertices in the width of the vertex buffer, in this case five.</span></span> <span data-ttu-id="b4604-147">L'offset x al primo vertice è denominato StartIndexVertexWidth ed è in questo caso 1.</span><span class="sxs-lookup"><span data-stu-id="b4604-147">The x offset to the first vertex is called the StartIndexVertexWidth and is in this case 1.</span></span> <span data-ttu-id="b4604-148">L'offset y per il primo vertice della patch viene chiamato StartIndexVertexHeight ed è in questo caso 0.</span><span class="sxs-lookup"><span data-stu-id="b4604-148">The y offset to the first patch vertex is called the StartIndexVertexHeight and is in this case 0.</span></span>

<span data-ttu-id="b4604-149">Per eseguire il rendering di un flusso di singole patch rettangolari (non mosaico), è necessario interpretare la geometria come patch rettangolare lunga (1 x N).</span><span class="sxs-lookup"><span data-stu-id="b4604-149">To render a stream of individual rectangular patches (non-mosaic), you should interpret your geometry as a long narrow (1 x N) rectangular patch.</span></span> <span data-ttu-id="b4604-150">La struttura delle **\_ informazioni di D3DRECTPATCH** per tale striscia (Bézier cubica) viene configurata nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="b4604-150">The **D3DRECTPATCH\_INFO** structure for such a strip (cubic Bézier) would be set up in the following manner.</span></span>


```
    
D3DRECTPATCH_INFO RectInfo;

RectInfo.Width = 4;
RectInfo.Height = 4;
RectInfo.Stride = 4;
RectInfo.Basis = D3DBASIS_BEZIER;
RectInfo.Order = D3DORDER_CUBIC;
RectInfo.StartVertexOffsetWidth = 0;
RectInfo.StartVertexOffsetHeight = 4*i;  // The variable i is the index of the 
//   patch you want to render.
```



## <a name="requirements"></a><span data-ttu-id="b4604-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4604-151">Requirements</span></span>



| <span data-ttu-id="b4604-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4604-152">Requirement</span></span> | <span data-ttu-id="b4604-153">Valore</span><span class="sxs-lookup"><span data-stu-id="b4604-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4604-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4604-154">Header</span></span><br/> | <dl> <span data-ttu-id="b4604-155"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4604-155"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4604-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4604-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4604-157">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="b4604-157">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="b4604-158">**DrawRectPatch**</span><span class="sxs-lookup"><span data-stu-id="b4604-158">**DrawRectPatch**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)
</dt> <dt>

[<span data-ttu-id="b4604-159">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="b4604-159">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
