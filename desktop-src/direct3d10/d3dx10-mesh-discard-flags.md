---
description: Specifica quali parti di dati mesh rimuovere dal dispositivo. Usato con ID3DX10Mesh::D iscard.
ms.assetid: 8b3c22ab-1337-4a66-ae32-17bd1b73f624
title: D3DX10_MESH_DISCARD_FLAGS enumerazione (D3DX10Mesh.h)
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
ms.openlocfilehash: d4b98550a2f3a896ed7b99f3e16f33a399a58035497e44420709ee8a0726901b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989471"
---
# <a name="d3dx10_mesh_discard_flags-enumeration"></a>Enumerazione D3DX10 \_ MESH \_ DISCARD \_ FLAGS

Specifica quali parti di dati mesh rimuovere dal dispositivo. Usato con [**ID3DX10Mesh::D iscard**](id3dx10mesh-discard.md).

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

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**BUFFER DELL'ATTRIBUTO \_ \_ DISCARD \_ DELLA MESH D3DX10 \_**
</dt> <dd>

Rimuovere il buffer dell'attributo.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**TABELLA DEGLI ATTRIBUTI DISCARD DELLA MESH D3DX10 \_ \_ \_ \_**
</dt> <dd>

Rimuovere la tabella degli attributi.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**PUNTI DI ELIMINAZIONE DELLA MESH D3DX10 \_ \_ \_**
</dt> <dd>

Rimuovere il buffer delle ripetizioni dei puntatori.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10 \_ MESH \_ DISCARD \_ ADJACENCY**
</dt> <dd>

Rimuovere il buffer di adienze.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**BUFFER DEI DISPOSITIVI DI ELIMINAZIONE DELLA RETE D3DX10 \_ \_ \_ \_**
</dt> <dd>

Eliminare i buffer di cui è stato eseguito il commit nel dispositivo [**(con ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Mesh.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




