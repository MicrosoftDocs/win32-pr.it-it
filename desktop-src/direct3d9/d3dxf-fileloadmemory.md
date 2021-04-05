---
description: Identifica i dati di memoria.
ms.assetid: 0ec0597f-d83a-4c1e-b993-30f0bbd64e6b
title: Struttura D3DXF_FILELOADMEMORY (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADMEMORY
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: a7ad988d9906101db57af6f8f5042766c3e32ccc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969356"
---
# <a name="d3dxf_fileloadmemory-structure"></a>\_Struttura D3DXF FILELOADMEMORY

Identifica i dati di memoria.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXF_FILELOADMEMORY {
  LPCVOID lpMemory;
  SIZE_T  dSize;
} D3DXF_FILELOADMEMORY, *LPD3DXF_FILELOADMEMORY;
```



## <a name="members"></a>Members

<dl> <dt>

**lpMemory**
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Puntatore a un blocco di memoria da caricare.

</dd> <dt>

**dSize**
</dt> <dd>

Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensione del blocco di memoria da caricare, in byte.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura identifica i dati da caricare dalla memoria quando un'applicazione usa il metodo [**CreateEnumObject**](id3dxfile--createenumobject.md) e specifica il \_ flag D3DXF fileload \_ FROMMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9xof. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture di file D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
