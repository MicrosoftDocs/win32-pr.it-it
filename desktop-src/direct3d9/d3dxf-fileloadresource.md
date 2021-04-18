---
description: Identifica i dati della risorsa.
ms.assetid: f2ace2ad-228f-4f76-ab31-16e045e09331
title: Struttura D3DXF_FILELOADRESOURCE (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: ee5dc27b551382a5fa5d1c7f4833c94b205e5521
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322704"
---
# <a name="d3dxf_fileloadresource-structure"></a>\_Struttura D3DXF FILELOADRESOURCE

Identifica i dati della risorsa.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXF_FILELOADRESOURCE {
  HMODULE hModule;
  LPCSTR  lpName;
  LPCSTR  lpType;
} D3DXF_FILELOADRESOURCE, *LPD3DXF_FILELOADRESOURCE;
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

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Puntatore a una stringa che specifica il nome della risorsa da caricare. Ad esempio, se la risorsa è una mesh, questo membro deve specificare il nome del file mesh.

</dd> <dt>

**lpType**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Puntatore a una stringa che specifica il tipo definito dall'utente che identifica la risorsa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura identifica una risorsa da caricare quando un'applicazione usa il metodo [**CreateEnumObject**](id3dxfile--createenumobject.md) e specifica il flag [D3DXF \_ fileload \_ FROMRESOURCE](d3dxf.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9xof. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture di file D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
