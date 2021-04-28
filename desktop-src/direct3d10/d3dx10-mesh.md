---
description: 'D3DX10_MESH: flag usati per specificare le opzioni di creazione per una mesh.'
ms.assetid: 1a5a6b3f-34f4-4338-9ffe-8f95f6f0c385
title: D3DX10_MESH enumerazione (D3DX10Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 2659783b0443396508465f9498eec86950f825bc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105439"
---
# <a name="d3dx10_mesh-enumeration"></a><span data-ttu-id="c59ba-103">Enumerazione D3DX10 \_ MESH</span><span class="sxs-lookup"><span data-stu-id="c59ba-103">D3DX10\_MESH enumeration</span></span>

<span data-ttu-id="c59ba-104">Flag usati per specificare le opzioni di creazione per una mesh.</span><span class="sxs-lookup"><span data-stu-id="c59ba-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="c59ba-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c59ba-105">Syntax</span></span>


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a><span data-ttu-id="c59ba-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="c59ba-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c59ba-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10 \_ MESH \_ A 32 \_ BIT**</span><span class="sxs-lookup"><span data-stu-id="c59ba-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10\_MESH\_32\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="c59ba-108">La mesh ha indici a 32 bit anziché indici a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="c59ba-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="c59ba-109">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="c59ba-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c59ba-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**ADIZIA D3DX10 \_ \_ MESH GS \_**</span><span class="sxs-lookup"><span data-stu-id="c59ba-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3DX10\_MESH\_GS\_ADJACENCY**</span></span>
</dt> <dd>

<span data-ttu-id="c59ba-111">Segnala che la mesh contiene dati di adiziazione geometry shader.</span><span class="sxs-lookup"><span data-stu-id="c59ba-111">Signals that the mesh contains geometry shader adjacency data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c59ba-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="c59ba-112">Remarks</span></span>

<span data-ttu-id="c59ba-113">Una mesh a 32 bit (D3DXMESH 32BIT) può teoricamente \_ supportare (2 °)-1 visi e vertici.</span><span class="sxs-lookup"><span data-stu-id="c59ba-113">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2³²)-1 faces and vertices.</span></span> <span data-ttu-id="c59ba-114">Tuttavia, l'allocazione di memoria per una mesh di grandi dimensioni in un sistema operativo a 32 bit non è pratica.</span><span class="sxs-lookup"><span data-stu-id="c59ba-114">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="c59ba-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c59ba-115">Requirements</span></span>



| <span data-ttu-id="c59ba-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c59ba-116">Requirement</span></span> | <span data-ttu-id="c59ba-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c59ba-117">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c59ba-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c59ba-118">Header</span></span><br/> | <dl> <span data-ttu-id="c59ba-119"><dt>D3DX10Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="c59ba-119"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c59ba-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c59ba-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c59ba-121">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="c59ba-121">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




