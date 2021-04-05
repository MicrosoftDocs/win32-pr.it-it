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
# <a name="d3dx10_mesh_discard_flags-enumeration"></a>\_ \_ Enumerazione flag di eliminazione mesh d3dx10 \_

Specifica le parti di dati mesh da eliminare dal dispositivo. Usato con [**ID3DX10Mesh::D la scheda**](id3dx10mesh-discard.md).

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DX10_MESH_DISCARD_FLAGS { 
  D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER  = 0x01,
  D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE   = 0x02,
  D3DX10_MESH_DISCARD_POINTREPS         = 0x04,
  D3DX10_MESH_DISCARD_ADJACENCY         = 0x08,
  D3DX10_MESH_DISCARD_DEVICE_BUFFERS    = 0x10
} D3DX10_MESH_DISCARD_FLAGS, *LPD3DX10_MESH_DISCARD_FLAGS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**\_Buffer degli \_ attributi di eliminazione mesh \_ d3dx10 \_**
</dt> <dd>

Rimuovere il buffer dell'attributo.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**\_Tabella degli \_ attributi di eliminazione mesh \_ d3dx10 \_**
</dt> <dd>

Rimuovere la tabella degli attributi.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10 di \_ scarto della rete mesh \_ \_ POINTREPS**
</dt> <dd>

Rimuovere il buffer dei ripetitori del puntatore.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10 di \_ scarto della rete mesh \_ \_ adiacenza**
</dt> <dd>

Rimuovere il buffer adiacenza.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**D3DX10 \_ mesh \_ Elimina \_ i \_ buffer del dispositivo**
</dt> <dd>

Rimuovere i buffer di cui è stato eseguito il commit nel dispositivo (con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md)).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




