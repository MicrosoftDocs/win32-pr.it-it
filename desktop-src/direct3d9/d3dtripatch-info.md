---
description: Descrive una patch di ordine superiore triangolare.
ms.assetid: 3f97120b-3b32-4f95-8614-7b263ff330db
title: Struttura D3DTRIPATCH_INFO (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRIPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b910d38025c44d6157a76aa3e3425ba46d628787
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323260"
---
# <a name="d3dtripatch_info-structure"></a><span data-ttu-id="c7452-103">Struttura delle informazioni di D3DTRIPATCH \_</span><span class="sxs-lookup"><span data-stu-id="c7452-103">D3DTRIPATCH\_INFO structure</span></span>

<span data-ttu-id="c7452-104">Descrive una patch di ordine superiore triangolare.</span><span class="sxs-lookup"><span data-stu-id="c7452-104">Describes a triangular high-order patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7452-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7452-105">Syntax</span></span>


```C++
typedef struct D3DTRIPATCH_INFO {
  UINT          StartVertexOffset;
  UINT          NumVertices;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DTRIPATCH_INFO, *LPD3DTRIPATCH_INFO;
```



## <a name="members"></a><span data-ttu-id="c7452-106">Members</span><span class="sxs-lookup"><span data-stu-id="c7452-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c7452-107">**StartVertexOffset**</span><span class="sxs-lookup"><span data-stu-id="c7452-107">**StartVertexOffset**</span></span>
</dt> <dd>

<span data-ttu-id="c7452-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7452-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7452-109">Offset del vertice iniziale, in numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="c7452-109">Starting vertex offset, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="c7452-110">**NumVertices**</span><span class="sxs-lookup"><span data-stu-id="c7452-110">**NumVertices**</span></span>
</dt> <dd>

<span data-ttu-id="c7452-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7452-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7452-112">Numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="c7452-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="c7452-113">**Basis**</span><span class="sxs-lookup"><span data-stu-id="c7452-113">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="c7452-114">Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="c7452-114">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7452-115">Membro del tipo enumerato [**D3DBASISTYPE**](./d3dbasistype.md) , che definisce il tipo di base per la patch di ordine superiore triangolare.</span><span class="sxs-lookup"><span data-stu-id="c7452-115">Member of the [**D3DBASISTYPE**](./d3dbasistype.md) enumerated type, which defines the basis type for the triangular high-order patch.</span></span> <span data-ttu-id="c7452-116">L'unico valore valido per questo membro è D3DBASIS \_ Bezier.</span><span class="sxs-lookup"><span data-stu-id="c7452-116">The only valid value for this member is D3DBASIS\_BEZIER.</span></span>

</dd> <dt>

<span data-ttu-id="c7452-117">**Gradi**</span><span class="sxs-lookup"><span data-stu-id="c7452-117">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="c7452-118">Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="c7452-118">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7452-119">Membro del tipo enumerato [**D3DDEGREETYPE**](./d3ddegreetype.md) , che definisce il tipo di grado per la patch di ordine superiore triangolare.</span><span class="sxs-lookup"><span data-stu-id="c7452-119">Member of the [**D3DDEGREETYPE**](./d3ddegreetype.md) enumerated type, defining the degree type for the triangular high-order patch.</span></span>



| <span data-ttu-id="c7452-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c7452-120">Value</span></span>                | <span data-ttu-id="c7452-121">Numero di vertici</span><span class="sxs-lookup"><span data-stu-id="c7452-121">Number of vertices</span></span> |
|----------------------|--------------------|
| <span data-ttu-id="c7452-122">\_Cubi D3DDEGREE</span><span class="sxs-lookup"><span data-stu-id="c7452-122">D3DDEGREE\_CUBIC</span></span>     | <span data-ttu-id="c7452-123">10</span><span class="sxs-lookup"><span data-stu-id="c7452-123">10</span></span>                 |
| <span data-ttu-id="c7452-124">D3DDEGREE \_ lineare</span><span class="sxs-lookup"><span data-stu-id="c7452-124">D3DDEGREE\_LINEAR</span></span>    | <span data-ttu-id="c7452-125">3</span><span class="sxs-lookup"><span data-stu-id="c7452-125">3</span></span>                  |
| <span data-ttu-id="c7452-126">D3DDEGREE \_ quadratico</span><span class="sxs-lookup"><span data-stu-id="c7452-126">D3DDEGREE\_QUADRATIC</span></span> | <span data-ttu-id="c7452-127">N/D</span><span class="sxs-lookup"><span data-stu-id="c7452-127">N/A</span></span>                |
| <span data-ttu-id="c7452-128">D3DDEGREE \_ quinte</span><span class="sxs-lookup"><span data-stu-id="c7452-128">D3DDEGREE\_QUINTIC</span></span>   | <span data-ttu-id="c7452-129">21</span><span class="sxs-lookup"><span data-stu-id="c7452-129">21</span></span>                 |



 

<span data-ttu-id="c7452-130">N/A: non disponibile.</span><span class="sxs-lookup"><span data-stu-id="c7452-130">N/A - Not available.</span></span> <span data-ttu-id="c7452-131">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="c7452-131">Not supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7452-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7452-132">Remarks</span></span>

<span data-ttu-id="c7452-133">Il diagramma seguente, ad esempio, identifica i numeri di ordine e di segmento dei vertici per una patch del triangolo di Bézier cubica.</span><span class="sxs-lookup"><span data-stu-id="c7452-133">For example, the following diagram identifies the vertex order and segment numbers for a cubic Bézier triangle patch.</span></span> <span data-ttu-id="c7452-134">L'ordine dei vertici determina i numeri di segmento usati da [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch).</span><span class="sxs-lookup"><span data-stu-id="c7452-134">The vertex order determines the segment numbers used by [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch).</span></span> <span data-ttu-id="c7452-135">L'offset è il numero di byte al primo vertice della patch del triangolo nel buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="c7452-135">The offset is the number of bytes to the first triangle patch vertex in the vertex buffer.</span></span>

![diagramma di una patch di ordine superiore triangolare con nove vertici](images/hop-tripatch-info.png)

## <a name="requirements"></a><span data-ttu-id="c7452-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7452-137">Requirements</span></span>



| <span data-ttu-id="c7452-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7452-138">Requirement</span></span> | <span data-ttu-id="c7452-139">Valore</span><span class="sxs-lookup"><span data-stu-id="c7452-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7452-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7452-140">Header</span></span><br/> | <dl> <span data-ttu-id="c7452-141"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7452-141"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7452-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7452-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7452-143">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="c7452-143">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="c7452-144">**DrawTriPatch**</span><span class="sxs-lookup"><span data-stu-id="c7452-144">**DrawTriPatch**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)
</dt> <dt>

[<span data-ttu-id="c7452-145">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="c7452-145">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
