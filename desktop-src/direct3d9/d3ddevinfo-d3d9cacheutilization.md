---
description: Misurare le prestazioni della percentuale di riscontri nella cache per le trame e i vertici indicizzati.
ms.assetid: 70bc4e93-0a34-485b-bdcc-028c24b52f62
title: Struttura D3DDEVINFO_D3D9CACHEUTILIZATION (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9CACHEUTILIZATION
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 94f77549d0ea2a9c59d7de8367a6133085cc2771
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530865"
---
# <a name="d3ddevinfo_d3d9cacheutilization-structure"></a><span data-ttu-id="81894-103">\_Struttura D3DDEVINFO D3D9CACHEUTILIZATION</span><span class="sxs-lookup"><span data-stu-id="81894-103">D3DDEVINFO\_D3D9CACHEUTILIZATION structure</span></span>

<span data-ttu-id="81894-104">Misurare le prestazioni della percentuale di riscontri nella cache per le trame e i vertici indicizzati.</span><span class="sxs-lookup"><span data-stu-id="81894-104">Measure the cache hit rate performance for textures and indexed vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="81894-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81894-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9CACHEUTILIZATION {
  FLOAT TextureCacheHitRate;
  FLOAT PostTransformVertexCacheHitRate;
} D3DDEVINFO_D3D9CACHEUTILIZATION, *LPD3DDEVINFO_D3D9CACHEUTILIZATION;
```



## <a name="members"></a><span data-ttu-id="81894-106">Members</span><span class="sxs-lookup"><span data-stu-id="81894-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="81894-107">**TextureCacheHitRate**</span><span class="sxs-lookup"><span data-stu-id="81894-107">**TextureCacheHitRate**</span></span>
</dt> <dd>

<span data-ttu-id="81894-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81894-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="81894-109">Percentuale di riscontri per la ricerca di una trama nella cache di trama.</span><span class="sxs-lookup"><span data-stu-id="81894-109">The hit rate for finding a texture in the texture cache.</span></span> <span data-ttu-id="81894-110">Si presuppone che esista una cache di trama.</span><span class="sxs-lookup"><span data-stu-id="81894-110">This assumes there is a texture cache.</span></span> <span data-ttu-id="81894-111">L'aumento della distorsione del livello di dettaglio per usare la trama più dettagliata, l'uso di molte trame di grandi dimensioni o la creazione di un modello di accesso a trama quasi casuale in trame di grandi dimensioni con codice shader personalizzato può influenzare significativamente la percentuale di riscontri nella cache della trama.</span><span class="sxs-lookup"><span data-stu-id="81894-111">Increasing the level-of-detail bias to use the most detailed texture, using many large textures, or producing a near random texture access pattern on large textures with custom shader code can dramatically affect the texture cache hit rate.</span></span>

</dd> <dt>

<span data-ttu-id="81894-112">**PostTransformVertexCacheHitRate**</span><span class="sxs-lookup"><span data-stu-id="81894-112">**PostTransformVertexCacheHitRate**</span></span>
</dt> <dd>

<span data-ttu-id="81894-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81894-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="81894-114">Percentuale di riscontri per trovare i vertici trasformati nella cache dei vertici.</span><span class="sxs-lookup"><span data-stu-id="81894-114">The hit rate for finding transformed vertices in the vertex cache.</span></span> <span data-ttu-id="81894-115">La GPU è progettata per trasformare i vertici indicizzati e può archiviarli in una cache dei vertici.</span><span class="sxs-lookup"><span data-stu-id="81894-115">The GPU is designed to transform indexed vertices and may store them in a vertex cache.</span></span> <span data-ttu-id="81894-116">Se si usano mesh, [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) o [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) può comportare un migliore utilizzo della cache del vertice.</span><span class="sxs-lookup"><span data-stu-id="81894-116">If you are using meshes, [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) or [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) may result in better vertex cache utilization.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81894-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="81894-117">Remarks</span></span>

<span data-ttu-id="81894-118">Una cache efficiente è in genere più vicina a una percentuale di riscontri del 90% e una cache inefficiente è in genere più vicina a una percentuale di riscontri del 10% (anche se una percentuale bassa non è necessariamente un problema).</span><span class="sxs-lookup"><span data-stu-id="81894-118">An efficient cache is typically closer to a 90 percent hit rate, and an inefficient cache is typically closer to a 10 percent hit rate (although a low percentage is not necessarily a problem).</span></span>

## <a name="requirements"></a><span data-ttu-id="81894-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81894-119">Requirements</span></span>



| <span data-ttu-id="81894-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="81894-120">Requirement</span></span> | <span data-ttu-id="81894-121">Valore</span><span class="sxs-lookup"><span data-stu-id="81894-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81894-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81894-122">Header</span></span><br/> | <dl> <span data-ttu-id="81894-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="81894-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81894-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81894-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81894-125">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="81894-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="81894-126">**GetData**</span><span class="sxs-lookup"><span data-stu-id="81894-126">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
