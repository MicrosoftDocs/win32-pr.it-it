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
# <a name="d3dx10_mesh-enumeration"></a>Enumerazione D3DX10 \_ MESH

Flag usati per specificare le opzioni di creazione per una mesh.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10 \_ MESH \_ A 32 \_ BIT**
</dt> <dd>

La mesh ha indici a 32 bit anziché indici a 16 bit. Vedere la sezione Osservazioni.

</dd> <dt>

<span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**ADIZIA D3DX10 \_ \_ MESH GS \_**
</dt> <dd>

Segnala che la mesh contiene dati di adiziazione geometry shader.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una mesh a 32 bit (D3DXMESH 32BIT) può teoricamente \_ supportare (2 °)-1 visi e vertici. Tuttavia, l'allocazione di memoria per una mesh di grandi dimensioni in un sistema operativo a 32 bit non è pratica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Mesh.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




