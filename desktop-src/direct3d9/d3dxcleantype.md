---
description: Definisce le operazioni da eseguire sui vertici in preparazione alla pulizia della rete.
ms.assetid: f222acaa-fa82-4591-b7c2-b520cb648ed5
title: Enumerazione D3DXCLEANTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCLEANTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: b38578d0f50521def552b8bd6608c2696b405d0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235061"
---
# <a name="d3dxcleantype-enumeration"></a><span data-ttu-id="e4859-103">Enumerazione D3DXCLEANTYPE</span><span class="sxs-lookup"><span data-stu-id="e4859-103">D3DXCLEANTYPE enumeration</span></span>

<span data-ttu-id="e4859-104">Definisce le operazioni da eseguire sui vertici in preparazione alla pulizia della rete.</span><span class="sxs-lookup"><span data-stu-id="e4859-104">Defines operations to perform on vertices in preparation for mesh cleaning.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4859-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4859-105">Syntax</span></span>


```C++
typedef enum D3DXCLEANTYPE { 
  D3DXCLEAN_BACKFACING      = 1,
  D3DXCLEAN_BOWTIES         = 2,
  D3DXCLEAN_SKINNING        = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_OPTIMIZATION    = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_SIMPLIFICATION  = D3DXCLEAN_BACKFACING | D3DXCLEAN_BOWTIES
} D3DXCLEANTYPE, *LPD3DXCLEANTYPE;
```



## <a name="constants"></a><span data-ttu-id="e4859-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="e4859-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e4859-107"><span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN \_ BACKfacing**</span><span class="sxs-lookup"><span data-stu-id="e4859-107"><span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN\_BACKFACING**</span></span>
</dt> <dd>

<span data-ttu-id="e4859-108">Unisci triangoli che condividono gli stessi indici di vertice ma hanno normali facciali che puntano in direzioni opposte (triangoli rivolti verso il retro).</span><span class="sxs-lookup"><span data-stu-id="e4859-108">Merge triangles that share the same vertex indices but have face normals pointing in opposite directions (back-facing triangles).</span></span> <span data-ttu-id="e4859-109">A meno che i triangoli non vengano divisi aggiungendo un vertice replicato, i dati di adiacenza mesh dei due triangoli potrebbero essere in conflitto.</span><span class="sxs-lookup"><span data-stu-id="e4859-109">Unless the triangles are not split by adding a replicated vertex, mesh adjacency data from the two triangles may conflict.</span></span>

</dd> <dt>

<span data-ttu-id="e4859-110"><span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**\_BOWTIES D3DXCLEAN**</span><span class="sxs-lookup"><span data-stu-id="e4859-110"><span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN\_BOWTIES**</span></span>
</dt> <dd>

<span data-ttu-id="e4859-111">Se un vertice è il vertice di due ventilatori a triangolo (bowtie) e le operazioni di mesh avranno effetto su una delle ventole, suddivideranno il vertice condiviso in due nuovi vertici.</span><span class="sxs-lookup"><span data-stu-id="e4859-111">If a vertex is the apex of two triangle fans (a bowtie) and mesh operations will affect one of the fans, then split the shared vertex into two new vertices.</span></span> <span data-ttu-id="e4859-112">Bowties può causare problemi per le operazioni, ad esempio la semplificazione della rete che rimuove i vertici, perché la rimozione di un vertice interessa due set distinti di triangoli.</span><span class="sxs-lookup"><span data-stu-id="e4859-112">Bowties can cause problems for operations such as mesh simplification that remove vertices, because removing one vertex affects two distinct sets of triangles.</span></span>

</dd> <dt>

<span data-ttu-id="e4859-113"><span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN \_ skining**</span><span class="sxs-lookup"><span data-stu-id="e4859-113"><span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN\_SKINNING**</span></span>
</dt> <dd>

<span data-ttu-id="e4859-114">Usare questo flag per impedire l'esecuzione di cicli infiniti durante la scuoiatura delle operazioni mesh di installazione.</span><span class="sxs-lookup"><span data-stu-id="e4859-114">Use this flag to prevent infinite loops during skinning setup mesh operations.</span></span>

</dd> <dt>

<span data-ttu-id="e4859-115"><span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**\_Ottimizzazione D3DXCLEAN**</span><span class="sxs-lookup"><span data-stu-id="e4859-115"><span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**D3DXCLEAN\_OPTIMIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="e4859-116">Usare questo flag per evitare cicli infiniti durante le operazioni di ottimizzazione della rete.</span><span class="sxs-lookup"><span data-stu-id="e4859-116">Use this flag to prevent infinite loops during mesh optimization operations.</span></span>

</dd> <dt>

<span data-ttu-id="e4859-117"><span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**\_Semplificazione D3DXCLEAN**</span><span class="sxs-lookup"><span data-stu-id="e4859-117"><span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**D3DXCLEAN\_SIMPLIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="e4859-118">Usare questo flag per evitare cicli infiniti durante le operazioni di semplificazione della rete.</span><span class="sxs-lookup"><span data-stu-id="e4859-118">Use this flag to prevent infinite loops during mesh simplification operations.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4859-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4859-119">Requirements</span></span>



| <span data-ttu-id="e4859-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4859-120">Requirement</span></span> | <span data-ttu-id="e4859-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e4859-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4859-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4859-122">Header</span></span><br/> | <dl> <span data-ttu-id="e4859-123"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4859-123"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4859-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4859-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4859-125">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="e4859-125">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




