---
description: Identifica i dati di memoria.
ms.assetid: 0ec0597f-d83a-4c1e-b993-30f0bbd64e6b
title: D3DXF_FILELOADMEMORY struttura (D3dx9xof.h)
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
ms.openlocfilehash: b3709e6eeb99026b76d066edfccbae578b5c851d6e73936ffe06d10fbf69dcb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045059"
---
# <a name="d3dxf_fileloadmemory-structure"></a>Struttura D3DXF \_ FILELOADMEMORY

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

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensioni del blocco di memoria da caricare, in byte.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura identifica i dati da caricare dalla memoria quando un'applicazione usa il metodo [**CreateEnumObject**](id3dxfile--createenumobject.md) e specifica il flag D3DXF \_ FILELOAD \_ FROMMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9xof.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture di file D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
