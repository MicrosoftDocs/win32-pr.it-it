---
description: Le applicazioni usano i metodi dell'interfaccia IDirectXFileEnumObject per scorrere gli oggetti dati nel file e recuperare un oggetto dati in base al relativo identificatore univoco globale (GUID) o al relativo nome. Deprecato.
ms.assetid: 9eefda2a-5b17-4330-8245-63a38c1b1469
title: Interfaccia IDirectXFileEnumObject (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 448751cf7160dd9f5bd44f8f7460f30acc731ddf783c840654c3634e80f66540
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491751"
---
# <a name="idirectxfileenumobject-interface"></a>Interfaccia IDirectXFileEnumObject

Le applicazioni usano i metodi dell'interfaccia IDirectXFileEnumObject per scorrere gli oggetti dati nel file e recuperare un oggetto dati in base al relativo identificatore univoco globale (GUID) o al relativo nome. Deprecato.

## <a name="members"></a>Membri

**L'interfaccia IDirectXFileEnumObject** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDirectXFileEnumObject** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili **nell'interfaccia IDirectXFileEnumObject.**



| Metodo                                                                     | Descrizione                                                                     |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**GetDataObjectById**](idirectxfileenumobject--getdataobjectbyid.md)     | Recupera l'oggetto dati con il GUID specificato. Deprecato.<br/>   |
| [**GetDataObjectByName**](idirectxfileenumobject--getdataobjectbyname.md) | Recupera l'oggetto dati con il nome specificato. Deprecato.<br/>   |
| [**GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md)     | Recupera l'oggetto di primo livello successivo nel file DirectX. Deprecato.<br/> |



 

## <a name="remarks"></a>Commenti

Il GUID per l'interfaccia IDirectXFileEnumObject è IID \_ IDirectXFileEnumObject.

Il tipo LPDIRECTXFILEENUMOBJECT è definito come puntatore a questa interfaccia.


```
typedef interface IDirectXFileEnumObject *LPDIRECTXFILEENUMOBJECT;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[X Interfacce di file](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
