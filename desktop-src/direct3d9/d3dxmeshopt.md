---
description: 'Enumerazione D3DXMESHOPT: specifica il tipo di ottimizzazione della mesh da eseguire.'
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: Enumerazione D3DXMESHOPT (D3dx9mesh.h)
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
ms.openlocfilehash: db7c2a2411d1c846c7369fc1d925a8e5569df3b1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114349"
---
# <a name="d3dxmeshopt-enumeration"></a><span data-ttu-id="47621-103">Enumerazione D3DXMESHOPT</span><span class="sxs-lookup"><span data-stu-id="47621-103">D3DXMESHOPT enumeration</span></span>

<span data-ttu-id="47621-104">Specifica il tipo di ottimizzazione della mesh da eseguire.</span><span class="sxs-lookup"><span data-stu-id="47621-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="47621-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47621-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="47621-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="47621-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="47621-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ COMPACT**</span><span class="sxs-lookup"><span data-stu-id="47621-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="47621-108">Riordina i visi per rimuovere i vertici e i visi inutilizzati.</span><span class="sxs-lookup"><span data-stu-id="47621-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="47621-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ ATTRSORT**</span><span class="sxs-lookup"><span data-stu-id="47621-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT\_ATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="47621-110">Riordina i visi per ottimizzare un minor numero di modifiche dello stato del bundle di attributi e migliorare le prestazioni [**di ID3DXBaseMesh::D rawSubset.**](id3dxbasemesh--drawsubset.md)</span><span class="sxs-lookup"><span data-stu-id="47621-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced [**ID3DXBaseMesh::DrawSubset**](id3dxbasemesh--drawsubset.md) performance.</span></span>

</dd> <dt>

<span data-ttu-id="47621-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ VERTEXCACHE**</span><span class="sxs-lookup"><span data-stu-id="47621-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT\_VERTEXCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="47621-112">Riordina i visi per aumentare la frequenza di riscontri nella cache delle cache dei vertici.</span><span class="sxs-lookup"><span data-stu-id="47621-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="47621-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ STRIPREORDER**</span><span class="sxs-lookup"><span data-stu-id="47621-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT\_STRIPREORDER**</span></span>
</dt> <dd>

<span data-ttu-id="47621-114">Riordina i visi per ottimizzare la lunghezza dei triangoli adiacenti.</span><span class="sxs-lookup"><span data-stu-id="47621-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="47621-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ IGNOREVERTS**</span><span class="sxs-lookup"><span data-stu-id="47621-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT\_IGNOREVERTS**</span></span>
</dt> <dd>

<span data-ttu-id="47621-116">Ottimizzare solo i visi; non ottimizzare i vertici.</span><span class="sxs-lookup"><span data-stu-id="47621-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="47621-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ DONOTSPLIT**</span><span class="sxs-lookup"><span data-stu-id="47621-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT\_DONOTSPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="47621-118">Durante l'ordinamento degli attributi, non dividere i vertici condivisi tra gruppi di attributi.</span><span class="sxs-lookup"><span data-stu-id="47621-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="47621-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**DISPOSITIVO D3DXMESHOPTINDEPENDENT \_**</span><span class="sxs-lookup"><span data-stu-id="47621-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT\_DEVICEINDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="47621-120">Influisce sulle dimensioni della cache dei vertici.</span><span class="sxs-lookup"><span data-stu-id="47621-120">Affects the vertex cache size.</span></span> <span data-ttu-id="47621-121">L'uso di questo flag specifica una dimensione predefinita della cache dei vertici che funziona correttamente nell'hardware legacy.</span><span class="sxs-lookup"><span data-stu-id="47621-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47621-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="47621-122">Remarks</span></span>

<span data-ttu-id="47621-123">I flag di ottimizzazione D3DXMESHOPT \_ STRIPREORDER e D3DXMESHOPT \_ VERTEXCACHE si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="47621-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="47621-124">Il flag SHAREVB D3DXMESHOPT \_ è stato rimosso da questa enumerazione.</span><span class="sxs-lookup"><span data-stu-id="47621-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="47621-125">In alternativa, usare D3DXMESH \_ VB \_ SHARE, in [**D3DXMESH.**](./d3dxmesh.md)</span><span class="sxs-lookup"><span data-stu-id="47621-125">Use D3DXMESH\_VB\_SHARE instead, in [**D3DXMESH**](./d3dxmesh.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="47621-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47621-126">Requirements</span></span>



| <span data-ttu-id="47621-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="47621-127">Requirement</span></span> | <span data-ttu-id="47621-128">Valore</span><span class="sxs-lookup"><span data-stu-id="47621-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47621-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47621-129">Header</span></span><br/> | <dl> <span data-ttu-id="47621-130"><dt>D3dx9mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="47621-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47621-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47621-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47621-132">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="47621-132">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
