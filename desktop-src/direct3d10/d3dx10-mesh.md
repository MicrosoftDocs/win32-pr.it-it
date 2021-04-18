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
# <a name="d3dx10_mesh-enumeration"></a>\_Enumerazione mesh d3dx10

Flag utilizzati per specificare le opzioni di creazione per una mesh.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10 \_ MESH \_ 32 \_ bit**
</dt> <dd>

La mesh ha indici a 32 bit invece degli indici a 16 bit. Vedere la sezione Osservazioni.

</dd> <dt>

<span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3DX10 \_ mesh \_ GS \_ adiacenza**
</dt> <dd>

Segnala che la mesh contiene i dati adiacenza di Geometry shader.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una mesh a 32 bit (D3DXMESH a \_ 32 bit) può supportare teoricamente (2 ³ ²)-1 visi e vertici. Tuttavia, l'allocazione della memoria per una rete di grandi dimensioni in un sistema operativo a 32 bit non è praticabile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




