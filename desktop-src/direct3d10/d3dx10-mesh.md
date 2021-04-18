---
description: Flag utilizzati per specificare le opzioni di creazione per una mesh.
ms.assetid: 1a5a6b3f-34f4-4338-9ffe-8f95f6f0c385
title: Enumerazione D3DX10_MESH (D3DX10Mesh. h)
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
ms.openlocfilehash: c2387024512a42c0a9e06ac1818b0282121cd0eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323319"
---
# <a name="d3dx10_mesh-enumeration"></a><span data-ttu-id="1a524-103">\_Enumerazione mesh d3dx10</span><span class="sxs-lookup"><span data-stu-id="1a524-103">D3DX10\_MESH enumeration</span></span>

<span data-ttu-id="1a524-104">Flag utilizzati per specificare le opzioni di creazione per una mesh.</span><span class="sxs-lookup"><span data-stu-id="1a524-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a524-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a524-105">Syntax</span></span>


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a><span data-ttu-id="1a524-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="1a524-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1a524-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10 \_ MESH \_ 32 \_ bit**</span><span class="sxs-lookup"><span data-stu-id="1a524-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10\_MESH\_32\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="1a524-108">La mesh ha indici a 32 bit invece degli indici a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="1a524-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="1a524-109">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1a524-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1a524-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3DX10 \_ mesh \_ GS \_ adiacenza**</span><span class="sxs-lookup"><span data-stu-id="1a524-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3DX10\_MESH\_GS\_ADJACENCY**</span></span>
</dt> <dd>

<span data-ttu-id="1a524-111">Segnala che la mesh contiene i dati adiacenza di Geometry shader.</span><span class="sxs-lookup"><span data-stu-id="1a524-111">Signals that the mesh contains geometry shader adjacency data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a524-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a524-112">Remarks</span></span>

<span data-ttu-id="1a524-113">Una mesh a 32 bit (D3DXMESH a \_ 32 bit) può supportare teoricamente (2 ³ ²)-1 visi e vertici.</span><span class="sxs-lookup"><span data-stu-id="1a524-113">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2³²)-1 faces and vertices.</span></span> <span data-ttu-id="1a524-114">Tuttavia, l'allocazione della memoria per una rete di grandi dimensioni in un sistema operativo a 32 bit non è praticabile.</span><span class="sxs-lookup"><span data-stu-id="1a524-114">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a524-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a524-115">Requirements</span></span>



| <span data-ttu-id="1a524-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a524-116">Requirement</span></span> | <span data-ttu-id="1a524-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1a524-117">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a524-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a524-118">Header</span></span><br/> | <dl> <span data-ttu-id="1a524-119"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a524-119"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a524-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a524-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a524-121">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="1a524-121">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




