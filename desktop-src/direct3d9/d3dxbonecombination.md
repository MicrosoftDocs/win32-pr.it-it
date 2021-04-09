---
description: Descrive un subset della mesh con lo stesso attributo e la stessa combinazione di osso.
ms.assetid: e6a4b3bb-d28d-44c2-a6df-f60f0412a70e
title: Struttura D3DXBONECOMBINATION (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBONECOMBINATION
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 3553ba37d0d9376fa5912143fb58849f03c5a83a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058625"
---
# <a name="d3dxbonecombination-structure"></a><span data-ttu-id="d040d-103">Struttura D3DXBONECOMBINATION</span><span class="sxs-lookup"><span data-stu-id="d040d-103">D3DXBONECOMBINATION structure</span></span>

<span data-ttu-id="d040d-104">Descrive un subset della mesh con lo stesso attributo e la stessa combinazione di osso.</span><span class="sxs-lookup"><span data-stu-id="d040d-104">Describes a subset of the mesh that has the same attribute and bone combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="d040d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d040d-105">Syntax</span></span>


```C++
typedef struct D3DXBONECOMBINATION {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
  DWORD *BoneId;
} D3DXBONECOMBINATION, *LPD3DXBONECOMBINATION;
```



## <a name="members"></a><span data-ttu-id="d040d-106">Members</span><span class="sxs-lookup"><span data-stu-id="d040d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d040d-107">**AttribId**</span><span class="sxs-lookup"><span data-stu-id="d040d-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="d040d-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d040d-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d040d-109">Identificatore della tabella degli attributi.</span><span class="sxs-lookup"><span data-stu-id="d040d-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d040d-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="d040d-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="d040d-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d040d-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d040d-112">Faccia iniziale.</span><span class="sxs-lookup"><span data-stu-id="d040d-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="d040d-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="d040d-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="d040d-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d040d-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d040d-115">Conteggio delle facce.</span><span class="sxs-lookup"><span data-stu-id="d040d-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="d040d-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="d040d-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="d040d-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d040d-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d040d-118">Vertice iniziale.</span><span class="sxs-lookup"><span data-stu-id="d040d-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="d040d-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="d040d-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="d040d-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d040d-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d040d-121">Conteggio vertici.</span><span class="sxs-lookup"><span data-stu-id="d040d-121">Vertex count.</span></span>

</dd> <dt>

<span data-ttu-id="d040d-122">**BoneId**</span><span class="sxs-lookup"><span data-stu-id="d040d-122">**BoneId**</span></span>
</dt> <dd>

<span data-ttu-id="d040d-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d040d-123">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="d040d-124">Puntatore a una matrice di valori che identificano ognuno degli ossicini che possono essere disegnati in una singola chiamata di disegno.</span><span class="sxs-lookup"><span data-stu-id="d040d-124">Pointer to an array of values that identify each of the bones that can be drawn in a single drawing call.</span></span> <span data-ttu-id="d040d-125">Si noti che la matrice può avere una lunghezza variabile per supportare combinazioni di lunghezza variabile di [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md).</span><span class="sxs-lookup"><span data-stu-id="d040d-125">Note that the array can be of variable length to accommodate variable length bone combinations of [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md).</span></span>

<span data-ttu-id="d040d-126">Le dimensioni della matrice variano in base al tipo di mesh generato.</span><span class="sxs-lookup"><span data-stu-id="d040d-126">The size of the array varies based on the type of mesh generated.</span></span> <span data-ttu-id="d040d-127">Una dimensione della matrice di mesh non indicizzata è uguale al numero di pesi per vertice (pMaxVertexInfl in [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="d040d-127">A non-indexed mesh array size is equal to the number of weights per vertex (pMaxVertexInfl in [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)).</span></span> <span data-ttu-id="d040d-128">Una dimensione della matrice di mesh indicizzata è uguale al numero di voci della tavolozza della matrice ossea (paletteSize in [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="d040d-128">An indexed mesh array size is equal to the number of bone matrix palette entries (paletteSize in [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d040d-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="d040d-129">Remarks</span></span>

<span data-ttu-id="d040d-130">È possibile eseguire il rendering del subset della mesh descritta da **D3DXBONECOMBINATION** in una singola chiamata di disegno.</span><span class="sxs-lookup"><span data-stu-id="d040d-130">The subset of the mesh described by **D3DXBONECOMBINATION** can be rendered in a single drawing call.</span></span>

## <a name="requirements"></a><span data-ttu-id="d040d-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d040d-131">Requirements</span></span>



| <span data-ttu-id="d040d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d040d-132">Requirement</span></span> | <span data-ttu-id="d040d-133">Valore</span><span class="sxs-lookup"><span data-stu-id="d040d-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d040d-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d040d-134">Header</span></span><br/> | <dl> <span data-ttu-id="d040d-135"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d040d-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d040d-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d040d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d040d-137">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="d040d-137">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
