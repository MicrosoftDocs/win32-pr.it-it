---
description: Identifica i dati di memoria. Deprecato.
ms.assetid: fe791e13-d5de-425f-b68f-80db8b332cc6
title: Struttura DXFILELOADMEMORY (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADMEMORY
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 02424abd354811a6522b58dd0011ecdddce24564
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323085"
---
# <a name="dxfileloadmemory-structure"></a>Struttura DXFILELOADMEMORY

Identifica i dati di memoria. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
typedef struct DXFILELOADMEMORY {
  LPVOID lpMemory;
  DWORD  dSize;
} DXFILELOADMEMORY, *LPDXFILELOADMEMORY;
```



## <a name="members"></a>Members

<dl> <dt>

**lpMemory**
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Puntatore a un blocco di memoria da caricare.

</dd> <dt>

**dSize**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensione del blocco di memoria da caricare, in byte.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura identifica una risorsa da caricare quando un'applicazione usa il metodo [**CreateEnumObject**](idirectxfile--createenumobject.md) e specifica DXFILELOAD \_ FROMMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DXFile. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture di file X](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[**CreateEnumObject**](idirectxfile--createenumobject.md)
</dt> <dt>

[Costanti DXFILE](dxfile.md)
</dt> </dl>

 

 
