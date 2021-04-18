---
description: Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileEnumObject per scorrere gli oggetti dati nel file e per recuperare un oggetto dati in base al relativo identificatore univoco globale (GUID) o in base al nome. Deprecato.
ms.assetid: 9eefda2a-5b17-4330-8245-63a38c1b1469
title: Interfaccia IDirectXFileEnumObject (DXFile. h)
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
ms.openlocfilehash: f9220f6e0a406cb4143798787276d7aa6cb5f5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322538"
---
# <a name="idirectxfileenumobject-interface"></a>Interfaccia IDirectXFileEnumObject

Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileEnumObject per scorrere gli oggetti dati nel file e per recuperare un oggetto dati in base al relativo identificatore univoco globale (GUID) o in base al nome. Deprecato.

## <a name="members"></a>Membri

L'interfaccia **IDirectXFileEnumObject** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirectXFileEnumObject** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDirectXFileEnumObject** dispone di questi metodi.



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
| Intestazione<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di file X](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
