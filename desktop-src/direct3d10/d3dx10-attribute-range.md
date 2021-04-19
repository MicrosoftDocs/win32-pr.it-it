---
description: Archivia una voce della tabella degli attributi.
ms.assetid: 81c77dc9-e078-46a1-a435-4b241e36ec13
title: Struttura D3DX10_ATTRIBUTE_RANGE (D3DX10. h)
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
ms.openlocfilehash: ddf7f10882e08232467130b3abbc6fb723a843ed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323324"
---
# <a name="d3dx10_attribute_range-structure"></a><span data-ttu-id="636e5-103">Struttura dell'intervallo di \_ attributi d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="636e5-103">D3DX10\_ATTRIBUTE\_RANGE structure</span></span>

<span data-ttu-id="636e5-104">Archivia una voce della tabella degli attributi.</span><span class="sxs-lookup"><span data-stu-id="636e5-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="636e5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="636e5-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_RANGE {
  UINT AttribId;
  UINT FaceStart;
  UINT FaceCount;
  UINT VertexStart;
  UINT VertexCount;
} D3DX10_ATTRIBUTE_RANGE, *LPD3DX10_ATTRIBUTE_RANGE;
```



## <a name="members"></a><span data-ttu-id="636e5-106">Members</span><span class="sxs-lookup"><span data-stu-id="636e5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="636e5-107">**AttribId**</span><span class="sxs-lookup"><span data-stu-id="636e5-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="636e5-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="636e5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="636e5-109">Identificatore della tabella degli attributi.</span><span class="sxs-lookup"><span data-stu-id="636e5-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="636e5-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="636e5-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="636e5-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="636e5-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="636e5-112">Faccia iniziale.</span><span class="sxs-lookup"><span data-stu-id="636e5-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="636e5-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="636e5-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="636e5-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="636e5-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="636e5-115">Conteggio delle facce.</span><span class="sxs-lookup"><span data-stu-id="636e5-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="636e5-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="636e5-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="636e5-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="636e5-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="636e5-118">Vertice iniziale.</span><span class="sxs-lookup"><span data-stu-id="636e5-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="636e5-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="636e5-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="636e5-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="636e5-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="636e5-121">Conteggio vertici.</span><span class="sxs-lookup"><span data-stu-id="636e5-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="636e5-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="636e5-122">Remarks</span></span>

<span data-ttu-id="636e5-123">Una tabella degli attributi viene utilizzata per identificare le aree della mesh che devono essere disegnate con trame, Stati di rendering, materiali e così via.</span><span class="sxs-lookup"><span data-stu-id="636e5-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="636e5-124">Inoltre, l'applicazione può usare la tabella attribute per nascondere parti di una mesh senza disegnare un identificatore di attributo specificato (AttribId) durante il disegno del frame.</span><span class="sxs-lookup"><span data-stu-id="636e5-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="636e5-125">Il \_ \_ tipo di intervallo dell'attributo LPD3DX è definito come un puntatore alla \_ struttura dell'intervallo di attributi di D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="636e5-125">The LPD3DX\_ATTRIBUTE\_RANGE type is defined as a pointer to the D3DX\_ATTRIBUTE\_RANGE structure.</span></span>


```
typedef D3DX_ATTRIBUTE_RANGE* LPD3DX_ATTRIBUTE_RANGE;
```



## <a name="requirements"></a><span data-ttu-id="636e5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="636e5-126">Requirements</span></span>



| <span data-ttu-id="636e5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="636e5-127">Requirement</span></span> | <span data-ttu-id="636e5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="636e5-128">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="636e5-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="636e5-129">Header</span></span><br/> | <dl> <span data-ttu-id="636e5-130"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="636e5-130"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="636e5-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="636e5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="636e5-132">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="636e5-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
