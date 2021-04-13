---
description: Specifica il tipo di ottimizzazione mesh da eseguire.
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: Enumerazione D3DX10_MESHOPT (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESHOPT
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: c8ccb13da1549b7e2eeeb67ebf7899c2187be363
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355559"
---
# <a name="d3dx10_meshopt-enumeration"></a><span data-ttu-id="c1bef-103">\_Enumerazione d3dx10 MESHOPT</span><span class="sxs-lookup"><span data-stu-id="c1bef-103">D3DX10\_MESHOPT enumeration</span></span>

<span data-ttu-id="c1bef-104">Specifica il tipo di ottimizzazione mesh da eseguire.</span><span class="sxs-lookup"><span data-stu-id="c1bef-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1bef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1bef-105">Syntax</span></span>


```C++
typedef enum D3DX10_MESHOPT { 
  D3DX10_MESHOPT_COMPACT             = 0x01000000,
  D3DX10_MESHOPT_ATTR_SORT           = 0x02000000,
  D3DX10_MESHOPT_VERTEX_CACHE        = 0x04000000,
  D3DX10_MESHOPT_STRIP_REORDER       = 0x08000000,
  D3DX10_MESHOPT_IGNORE_VERTS        = 0x10000000,
  D3DX10_MESHOPT_DO_NOT_SPLIT        = 0x20000000,
  D3DX10_MESHOPT_DEVICE_INDEPENDENT  = 0x00400000
} D3DX10_MESHOPT, *LPD3DX10_MESHOPT;
```



## <a name="constants"></a><span data-ttu-id="c1bef-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="c1bef-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c1bef-107"><span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10 \_ MESHOPT \_ Compact**</span><span class="sxs-lookup"><span data-stu-id="c1bef-107"><span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10\_MESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="c1bef-108">Riordina i visi per rimuovere i vertici e i visi inutilizzati.</span><span class="sxs-lookup"><span data-stu-id="c1bef-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="c1bef-109"><span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10 \_ MESHOPT \_ attr \_ Sort**</span><span class="sxs-lookup"><span data-stu-id="c1bef-109"><span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10\_MESHOPT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="c1bef-110">Riordina i visi per ottimizzare le modifiche dello stato del bundle di attributi e le prestazioni DrawSubset migliorate.</span><span class="sxs-lookup"><span data-stu-id="c1bef-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced DrawSubset performance.</span></span>

</dd> <dt>

<span data-ttu-id="c1bef-111"><span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10 \_ MESHOPT \_ Vertex \_ cache**</span><span class="sxs-lookup"><span data-stu-id="c1bef-111"><span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10\_MESHOPT\_VERTEX\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="c1bef-112">Riordina i visi per aumentare la percentuale di riscontri nella cache delle cache dei vertici.</span><span class="sxs-lookup"><span data-stu-id="c1bef-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="c1bef-113"><span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**Riordino della \_ striscia MESHOPT d3dx10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c1bef-113"><span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**D3DX10\_MESHOPT\_STRIP\_REORDER**</span></span>
</dt> <dd>

<span data-ttu-id="c1bef-114">Riordina i visi per ottimizzare la lunghezza dei triangoli adiacenti.</span><span class="sxs-lookup"><span data-stu-id="c1bef-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="c1bef-115"><span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10 \_ MESHOPT \_ Ignora i \_ vertici**</span><span class="sxs-lookup"><span data-stu-id="c1bef-115"><span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10\_MESHOPT\_IGNORE\_VERTS**</span></span>
</dt> <dd>

<span data-ttu-id="c1bef-116">Ottimizza solo le facce; non ottimizzare i vertici.</span><span class="sxs-lookup"><span data-stu-id="c1bef-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="c1bef-117"><span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**\_MESHOPT d3dx10 \_ \_ non \_ suddivise**</span><span class="sxs-lookup"><span data-stu-id="c1bef-117"><span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10\_MESHOPT\_DO\_NOT\_SPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="c1bef-118">Durante l'ordinamento degli attributi, non suddividere i vertici condivisi tra gruppi di attributi.</span><span class="sxs-lookup"><span data-stu-id="c1bef-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="c1bef-119"><span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10 \_ MESHOPT \_ dispositivo \_ indipendente**</span><span class="sxs-lookup"><span data-stu-id="c1bef-119"><span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10\_MESHOPT\_DEVICE\_INDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="c1bef-120">Influiscono sulle dimensioni della cache dei vertici.</span><span class="sxs-lookup"><span data-stu-id="c1bef-120">Affects the vertex cache size.</span></span> <span data-ttu-id="c1bef-121">L'uso di questo flag specifica una dimensione predefinita della cache Vertex che funziona correttamente nell'hardware legacy.</span><span class="sxs-lookup"><span data-stu-id="c1bef-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1bef-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1bef-122">Remarks</span></span>

<span data-ttu-id="c1bef-123">I \_ flag di ottimizzazione D3DXMESHOPT STRIPREORDER e D3DXMESHOPT \_ VERTEXCACHE si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="c1bef-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="c1bef-124">Il \_ flag SHAREVB di D3DXMESHOPT è stato rimosso da questa enumerazione.</span><span class="sxs-lookup"><span data-stu-id="c1bef-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="c1bef-125">Usare \_ invece D3DXMESH VB \_ share, in D3DXMESH.</span><span class="sxs-lookup"><span data-stu-id="c1bef-125">Use D3DXMESH\_VB\_SHARE instead, in D3DXMESH.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1bef-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1bef-126">Requirements</span></span>



| <span data-ttu-id="c1bef-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1bef-127">Requirement</span></span> | <span data-ttu-id="c1bef-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c1bef-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1bef-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1bef-129">Header</span></span><br/> | <dl> <span data-ttu-id="c1bef-130"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1bef-130"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1bef-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1bef-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1bef-132">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="c1bef-132">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




