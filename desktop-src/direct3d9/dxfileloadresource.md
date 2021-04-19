---
description: Identifica i dati della risorsa. Deprecato.
ms.assetid: acb379c7-ac80-412f-8891-d5917b3f8da4
title: Struttura DXFILELOADRESOURCE (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 233fe6acb13a6ae654a714028a316d7d6f6871ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323084"
---
# <a name="dxfileloadresource-structure"></a>Struttura DXFILELOADRESOURCE

Identifica i dati della risorsa. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
typedef struct DXFILELOADRESOURCE {
  HMODULE hModule;
  LPCTSTR lpName;
  LPCTSTR lpType;
} DXFILELOADRESOURCE, *LPDXFILELOADRESOURCE;
```



## <a name="members"></a>Members

<dl> <dt>

**hModule**
</dt> <dd>

Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**

</dd> <dd>

Handle del modulo che contiene la risorsa da caricare. Se questo membro è **null**, la risorsa deve essere collegata al file eseguibile che lo utilizzerà.

</dd> <dt>

**lpName**
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Puntatore a una stringa che specifica il nome della risorsa da caricare. Ad esempio, se la risorsa è una mesh, questo membro deve specificare il nome del file mesh.

</dd> <dt>

**lpType**
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Puntatore a una stringa che specifica il tipo definito dall'utente che identifica la risorsa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura identifica una risorsa da caricare quando un'applicazione usa il metodo [**CreateEnumObject**](idirectxfile--createenumobject.md) e specifica DXFILELOAD \_ FROMRESOURCE.

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

 

 
