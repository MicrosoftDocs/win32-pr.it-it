---
description: Archivia una voce della tabella degli attributi.
ms.assetid: b9f13b12-35ba-4e4c-93ac-3dd44d611b47
title: Struttura D3DXATTRIBUTERANGE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTERANGE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a842bbf41847f4b4e65c975e11f3e160cea1422d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322890"
---
# <a name="d3dxattributerange-structure"></a><span data-ttu-id="a4f36-103">Struttura D3DXATTRIBUTERANGE</span><span class="sxs-lookup"><span data-stu-id="a4f36-103">D3DXATTRIBUTERANGE structure</span></span>

<span data-ttu-id="a4f36-104">Archivia una voce della tabella degli attributi.</span><span class="sxs-lookup"><span data-stu-id="a4f36-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f36-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4f36-105">Syntax</span></span>


```C++
typedef struct D3DXATTRIBUTERANGE {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
} D3DXATTRIBUTERANGE, *LPD3DXATTRIBUTERANGE;
```



## <a name="members"></a><span data-ttu-id="a4f36-106">Members</span><span class="sxs-lookup"><span data-stu-id="a4f36-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a4f36-107">**AttribId**</span><span class="sxs-lookup"><span data-stu-id="a4f36-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="a4f36-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4f36-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4f36-109">Identificatore della tabella degli attributi.</span><span class="sxs-lookup"><span data-stu-id="a4f36-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a4f36-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="a4f36-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="a4f36-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4f36-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4f36-112">Faccia iniziale.</span><span class="sxs-lookup"><span data-stu-id="a4f36-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="a4f36-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="a4f36-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="a4f36-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4f36-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4f36-115">Conteggio delle facce.</span><span class="sxs-lookup"><span data-stu-id="a4f36-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="a4f36-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="a4f36-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="a4f36-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4f36-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4f36-118">Vertice iniziale.</span><span class="sxs-lookup"><span data-stu-id="a4f36-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="a4f36-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="a4f36-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="a4f36-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4f36-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4f36-121">Conteggio vertici.</span><span class="sxs-lookup"><span data-stu-id="a4f36-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4f36-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4f36-122">Remarks</span></span>

<span data-ttu-id="a4f36-123">Una tabella degli attributi viene utilizzata per identificare le aree della mesh che devono essere disegnate con trame, Stati di rendering, materiali e così via.</span><span class="sxs-lookup"><span data-stu-id="a4f36-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="a4f36-124">Inoltre, l'applicazione può usare la tabella attribute per nascondere parti di una mesh senza disegnare un identificatore di attributo specificato (AttribId) durante il disegno del frame.</span><span class="sxs-lookup"><span data-stu-id="a4f36-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="a4f36-125">Il tipo LPD3DXATTRIBUTERANGE è definito come un puntatore alla struttura **D3DXATTRIBUTERANGE** .</span><span class="sxs-lookup"><span data-stu-id="a4f36-125">The LPD3DXATTRIBUTERANGE type is defined as a pointer to the **D3DXATTRIBUTERANGE** structure.</span></span>


```
typedef D3DXATTRIBUTERANGE* LPD3DXATTRIBUTERANGE;
```



## <a name="requirements"></a><span data-ttu-id="a4f36-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4f36-126">Requirements</span></span>



| <span data-ttu-id="a4f36-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4f36-127">Requirement</span></span> | <span data-ttu-id="a4f36-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a4f36-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f36-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4f36-129">Header</span></span><br/> | <dl> <span data-ttu-id="a4f36-130"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4f36-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4f36-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4f36-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f36-132">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="a4f36-132">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
