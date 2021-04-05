---
description: Specifica le parti di dati mesh da eliminare dal dispositivo. Usato con ID3DX10Mesh::D la scheda.
ms.assetid: 8b3c22ab-1337-4a66-ae32-17bd1b73f624
title: Enumerazione D3DX10_MESH_DISCARD_FLAGS (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH_DISCARD_FLAGS
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 6640834cf81bfa5e4b6263d3b3cfbb1181bb16c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969462"
---
# <a name="d3dx10_mesh_discard_flags-enumeration"></a><span data-ttu-id="24dad-104">\_ \_ Enumerazione flag di eliminazione mesh d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="24dad-104">D3DX10\_MESH\_DISCARD\_FLAGS enumeration</span></span>

<span data-ttu-id="24dad-105">Specifica le parti di dati mesh da eliminare dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="24dad-105">Specifies which pieces of mesh data to discard from the device.</span></span> <span data-ttu-id="24dad-106">Usato con [**ID3DX10Mesh::D la scheda**](id3dx10mesh-discard.md).</span><span class="sxs-lookup"><span data-stu-id="24dad-106">Used with [**ID3DX10Mesh::Discard**](id3dx10mesh-discard.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="24dad-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24dad-107">Syntax</span></span>


```C++
typedef enum D3DX10_MESH_DISCARD_FLAGS { 
  D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER  = 0x01,
  D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE   = 0x02,
  D3DX10_MESH_DISCARD_POINTREPS         = 0x04,
  D3DX10_MESH_DISCARD_ADJACENCY         = 0x08,
  D3DX10_MESH_DISCARD_DEVICE_BUFFERS    = 0x10
} D3DX10_MESH_DISCARD_FLAGS, *LPD3DX10_MESH_DISCARD_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="24dad-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="24dad-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="24dad-109"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**\_Buffer degli \_ attributi di eliminazione mesh \_ d3dx10 \_**</span><span class="sxs-lookup"><span data-stu-id="24dad-109"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**D3DX10\_MESH\_DISCARD\_ATTRIBUTE\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="24dad-110">Rimuovere il buffer dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="24dad-110">Discard the attribute buffer.</span></span>

</dd> <dt>

<span data-ttu-id="24dad-111"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**\_Tabella degli \_ attributi di eliminazione mesh \_ d3dx10 \_**</span><span class="sxs-lookup"><span data-stu-id="24dad-111"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**D3DX10\_MESH\_DISCARD\_ATTRIBUTE\_TABLE**</span></span>
</dt> <dd>

<span data-ttu-id="24dad-112">Rimuovere la tabella degli attributi.</span><span class="sxs-lookup"><span data-stu-id="24dad-112">Discard the attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="24dad-113"><span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10 di \_ scarto della rete mesh \_ \_ POINTREPS**</span><span class="sxs-lookup"><span data-stu-id="24dad-113"><span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10\_MESH\_DISCARD\_POINTREPS**</span></span>
</dt> <dd>

<span data-ttu-id="24dad-114">Rimuovere il buffer dei ripetitori del puntatore.</span><span class="sxs-lookup"><span data-stu-id="24dad-114">Discard the pointer reps buffer.</span></span>

</dd> <dt>

<span data-ttu-id="24dad-115"><span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10 di \_ scarto della rete mesh \_ \_ adiacenza**</span><span class="sxs-lookup"><span data-stu-id="24dad-115"><span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10\_MESH\_DISCARD\_ADJACENCY**</span></span>
</dt> <dd>

<span data-ttu-id="24dad-116">Rimuovere il buffer adiacenza.</span><span class="sxs-lookup"><span data-stu-id="24dad-116">Discard the adjacency buffer.</span></span>

</dd> <dt>

<span data-ttu-id="24dad-117"><span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**D3DX10 \_ mesh \_ Elimina \_ i \_ buffer del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="24dad-117"><span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**D3DX10\_MESH\_DISCARD\_DEVICE\_BUFFERS**</span></span>
</dt> <dd>

<span data-ttu-id="24dad-118">Rimuovere i buffer di cui è stato eseguito il commit nel dispositivo (con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md)).</span><span class="sxs-lookup"><span data-stu-id="24dad-118">Discard the buffers committed to the device (with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24dad-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24dad-119">Requirements</span></span>



| <span data-ttu-id="24dad-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="24dad-120">Requirement</span></span> | <span data-ttu-id="24dad-121">Valore</span><span class="sxs-lookup"><span data-stu-id="24dad-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24dad-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24dad-122">Header</span></span><br/> | <dl> <span data-ttu-id="24dad-123"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="24dad-123"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24dad-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24dad-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24dad-125">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="24dad-125">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




