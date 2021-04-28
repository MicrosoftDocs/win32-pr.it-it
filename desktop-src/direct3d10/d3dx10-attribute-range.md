---
description: 'D3DX10_ATTRIBUTE_RANGE struttura : archivia una voce della tabella degli attributi.'
ms.assetid: 81c77dc9-e078-46a1-a435-4b241e36ec13
title: D3DX10_ATTRIBUTE_RANGE struttura (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_RANGE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 3e2954483da53c77ebef57f9cf2de104734caba2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094369"
---
# <a name="d3dx10_attribute_range-structure"></a><span data-ttu-id="3d6fc-103">Struttura ATTRIBUTE RANGE D3DX10 \_ \_</span><span class="sxs-lookup"><span data-stu-id="3d6fc-103">D3DX10\_ATTRIBUTE\_RANGE structure</span></span>

<span data-ttu-id="3d6fc-104">Archivia una voce della tabella degli attributi.</span><span class="sxs-lookup"><span data-stu-id="3d6fc-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d6fc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d6fc-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_RANGE {
  UINT AttribId;
  UINT FaceStart;
  UINT FaceCount;
  UINT VertexStart;
  UINT VertexCount;
} D3DX10_ATTRIBUTE_RANGE, *LPD3DX10_ATTRIBUTE_RANGE;
```



## <a name="members"></a><span data-ttu-id="3d6fc-106">Members</span><span class="sxs-lookup"><span data-stu-id="3d6fc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3d6fc-107">**AttribId**</span><span class="sxs-lookup"><span data-stu-id="3d6fc-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="3d6fc-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3d6fc-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3d6fc-109">Identificatore della tabella degli attributi.</span><span class="sxs-lookup"><span data-stu-id="3d6fc-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="3d6fc-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="3d6fc-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="3d6fc-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3d6fc-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3d6fc-112">Viso iniziale.</span><span class="sxs-lookup"><span data-stu-id="3d6fc-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="3d6fc-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="3d6fc-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="3d6fc-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3d6fc-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3d6fc-115">Numero di viso.</span><span class="sxs-lookup"><span data-stu-id="3d6fc-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="3d6fc-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="3d6fc-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="3d6fc-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3d6fc-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3d6fc-118">Vertice iniziale.</span><span class="sxs-lookup"><span data-stu-id="3d6fc-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="3d6fc-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="3d6fc-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="3d6fc-120">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3d6fc-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3d6fc-121">Numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="3d6fc-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d6fc-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d6fc-122">Remarks</span></span>

<span data-ttu-id="3d6fc-123">Una tabella di attributi viene usata per identificare le aree della mesh che devono essere disegnate con trame, stati di rendering, materiali e così via diversi.</span><span class="sxs-lookup"><span data-stu-id="3d6fc-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="3d6fc-124">Inoltre, l'applicazione può usare la tabella degli attributi per nascondere parti di una mesh non disegnando un determinato identificatore di attributo (AttribId) durante il disegno del frame.</span><span class="sxs-lookup"><span data-stu-id="3d6fc-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="3d6fc-125">Il tipo LPD3DX ATTRIBUTE RANGE è definito come puntatore alla \_ \_ struttura ATTRIBUTE RANGE D3DX. \_ \_</span><span class="sxs-lookup"><span data-stu-id="3d6fc-125">The LPD3DX\_ATTRIBUTE\_RANGE type is defined as a pointer to the D3DX\_ATTRIBUTE\_RANGE structure.</span></span>


```
typedef D3DX_ATTRIBUTE_RANGE* LPD3DX_ATTRIBUTE_RANGE;
```



## <a name="requirements"></a><span data-ttu-id="3d6fc-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d6fc-126">Requirements</span></span>



| <span data-ttu-id="3d6fc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d6fc-127">Requirement</span></span> | <span data-ttu-id="3d6fc-128">Valore</span><span class="sxs-lookup"><span data-stu-id="3d6fc-128">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3d6fc-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d6fc-129">Header</span></span><br/> | <dl> <span data-ttu-id="3d6fc-130"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="3d6fc-130"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d6fc-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d6fc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d6fc-132">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="3d6fc-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
