---
description: Identifica i dati delle risorse.
ms.assetid: f2ace2ad-228f-4f76-ab31-16e045e09331
title: D3DXF_FILELOADRESOURCE struttura (D3dx9xof.h)
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
ms.openlocfilehash: ddc105d3df7732e1572e41c3d9cb47a285caf69cba0a24f6ea65090706394592
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564931"
---
# <a name="d3dxf_fileloadresource-structure"></a>Struttura FILELOADRESOURCE D3DXF \_

Identifica i dati delle risorse.

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

**Hmodule**
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

</dd> <dd>

Handle del modulo contenente la risorsa da caricare. Se questo membro è **NULL,** la risorsa deve essere collegata al file eseguibile che lo userà.

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

Questa struttura identifica una risorsa da caricare quando un'applicazione usa il [**metodo CreateEnumObject**](id3dxfile--createenumobject.md) e specifica il flag [D3DXF \_ FILELOAD \_ FROMRESOURCE.](d3dxf.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9xof.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture di file D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
