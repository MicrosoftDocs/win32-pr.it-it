---
description: Specifica il tipo di ottimizzazione mesh da eseguire.
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: Enumerazione D3DXMESHOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: e7d4f9f4ae36cec74ea86fcb50a194ac66d0add7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322630"
---
# <a name="d3dxmeshopt-enumeration"></a><span data-ttu-id="5b6ae-103">Enumerazione D3DXMESHOPT</span><span class="sxs-lookup"><span data-stu-id="5b6ae-103">D3DXMESHOPT enumeration</span></span>

<span data-ttu-id="5b6ae-104">Specifica il tipo di ottimizzazione mesh da eseguire.</span><span class="sxs-lookup"><span data-stu-id="5b6ae-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b6ae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b6ae-105">Syntax</span></span>


```C++
enum _D3DXMESHOPT {
  D3DXMESHOPT_COMPACT            = 0x01000000, 
  D3DXMESHOPT_ATTRSORT           = 0x02000000, 
  D3DXMESHOPT_VERTEXCACHE        = 0x04000000, 
  D3DXMESHOPT_STRIPREORDER       = 0x08000000, 
  D3DXMESHOPT_IGNOREVERTS        = 0x10000000, 
  D3DXMESHOPT_DONOTSPLIT         = 0x20000000, 
  D3DXMESHOPT_DEVICEINDEPENDENT  = 0x40000000 

};
```



## <a name="constants"></a><span data-ttu-id="5b6ae-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="5b6ae-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5b6ae-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ Compact**</span><span class="sxs-lookup"><span data-stu-id="5b6ae-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="5b6ae-108">Riordina i visi per rimuovere i vertici e i visi inutilizzati.</span><span class="sxs-lookup"><span data-stu-id="5b6ae-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="5b6ae-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**\_ATTRSORT D3DXMESHOPT**</span><span class="sxs-lookup"><span data-stu-id="5b6ae-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT\_ATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="5b6ae-110">Riordina i visi per ottimizzare il minor numero di modifiche di stato del bundle di attributi e [**ID3DXBaseMesh avanzata::D rawsubset**](id3dxbasemesh--drawsubset.md) prestazioni.</span><span class="sxs-lookup"><span data-stu-id="5b6ae-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced [**ID3DXBaseMesh::DrawSubset**](id3dxbasemesh--drawsubset.md) performance.</span></span>

</dd> <dt>

<span data-ttu-id="5b6ae-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**\_VERTEXCACHE D3DXMESHOPT**</span><span class="sxs-lookup"><span data-stu-id="5b6ae-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT\_VERTEXCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="5b6ae-112">Riordina i visi per aumentare la percentuale di riscontri nella cache delle cache dei vertici.</span><span class="sxs-lookup"><span data-stu-id="5b6ae-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="5b6ae-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**\_STRIPREORDER D3DXMESHOPT**</span><span class="sxs-lookup"><span data-stu-id="5b6ae-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT\_STRIPREORDER**</span></span>
</dt> <dd>

<span data-ttu-id="5b6ae-114">Riordina i visi per ottimizzare la lunghezza dei triangoli adiacenti.</span><span class="sxs-lookup"><span data-stu-id="5b6ae-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="5b6ae-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**\_IGNOREVERTS D3DXMESHOPT**</span><span class="sxs-lookup"><span data-stu-id="5b6ae-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT\_IGNOREVERTS**</span></span>
</dt> <dd>

<span data-ttu-id="5b6ae-116">Ottimizza solo le facce; non ottimizzare i vertici.</span><span class="sxs-lookup"><span data-stu-id="5b6ae-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="5b6ae-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**\_DONOTSPLIT D3DXMESHOPT**</span><span class="sxs-lookup"><span data-stu-id="5b6ae-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT\_DONOTSPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="5b6ae-118">Durante l'ordinamento degli attributi, non suddividere i vertici condivisi tra gruppi di attributi.</span><span class="sxs-lookup"><span data-stu-id="5b6ae-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="5b6ae-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**\_DEVICEINDEPENDENT D3DXMESHOPT**</span><span class="sxs-lookup"><span data-stu-id="5b6ae-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT\_DEVICEINDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="5b6ae-120">Influiscono sulle dimensioni della cache dei vertici.</span><span class="sxs-lookup"><span data-stu-id="5b6ae-120">Affects the vertex cache size.</span></span> <span data-ttu-id="5b6ae-121">L'uso di questo flag specifica una dimensione predefinita della cache Vertex che funziona correttamente nell'hardware legacy.</span><span class="sxs-lookup"><span data-stu-id="5b6ae-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b6ae-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b6ae-122">Remarks</span></span>

<span data-ttu-id="5b6ae-123">I \_ flag di ottimizzazione D3DXMESHOPT STRIPREORDER e D3DXMESHOPT \_ VERTEXCACHE si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="5b6ae-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="5b6ae-124">Il \_ flag SHAREVB di D3DXMESHOPT è stato rimosso da questa enumerazione.</span><span class="sxs-lookup"><span data-stu-id="5b6ae-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="5b6ae-125">Usare \_ invece D3DXMESH VB \_ share, in [**D3DXMESH**](./d3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="5b6ae-125">Use D3DXMESH\_VB\_SHARE instead, in [**D3DXMESH**](./d3dxmesh.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b6ae-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b6ae-126">Requirements</span></span>



| <span data-ttu-id="5b6ae-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b6ae-127">Requirement</span></span> | <span data-ttu-id="5b6ae-128">Valore</span><span class="sxs-lookup"><span data-stu-id="5b6ae-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6ae-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b6ae-129">Header</span></span><br/> | <dl> <span data-ttu-id="5b6ae-130"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b6ae-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b6ae-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b6ae-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b6ae-132">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="5b6ae-132">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
