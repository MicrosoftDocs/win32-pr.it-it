---
description: Identifica i dati delle risorse. Deprecato.
ms.assetid: acb379c7-ac80-412f-8891-d5917b3f8da4
title: Struttura DXFILELOADRESOURCE (DXFile.h)
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
ms.openlocfilehash: 54d0072d7c87f6d26483faf8c591ea7651eff29b411643eb9848de11ff50d899
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803038"
---
# <a name="dxfileloadresource-structure"></a>Struttura DXFILELOADRESOURCE

Identifica i dati delle risorse. Deprecato.

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

**Hmodule**
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

</dd> <dd>

Handle del modulo contenente la risorsa da caricare. Se questo membro è **NULL,** la risorsa deve essere collegata al file eseguibile che lo userà.

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

Questa struttura identifica una risorsa da caricare quando un'applicazione usa il [**metodo CreateEnumObject**](idirectxfile--createenumobject.md) e specifica DXFILELOAD \_ FROMRESOURCE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DXFile.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[X Strutture di file](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[**CreateEnumObject**](idirectxfile--createenumobject.md)
</dt> <dt>

[Costanti DXFILE](dxfile.md)
</dt> </dl>

 

 
