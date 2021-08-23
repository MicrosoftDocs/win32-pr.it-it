---
description: Le applicazioni usano i metodi dell'interfaccia ID3DXFileEnumObject per scorrere gli oggetti dati dei file figlio nel file e recuperare un oggetto figlio in base al relativo identificatore univoco globale (GUID) o in base al nome.
ms.assetid: 23b28f07-5832-4163-953b-615d20e781f6
title: Interfaccia ID3DXFileEnumObject (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4c274a42a5e07f05af3b0b2ffe18dc3fbaf546591f23e6f24906cd1723578303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121360"
---
# <a name="id3dxfileenumobject-interface"></a>Interfaccia ID3DXFileEnumObject

Le applicazioni usano i metodi dell'interfaccia ID3DXFileEnumObject per scorrere gli oggetti dati dei file figlio nel file e recuperare un oggetto figlio in base al relativo identificatore univoco globale (GUID) o in base al nome.

## <a name="members"></a>Membri

**L'interfaccia ID3DXFileEnumObject** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXFileEnumObject** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXFileEnumObject** include questi metodi.



| Metodo                                                                  | Descrizione                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**GetChild**](id3dxfileenumobject--getchild.md)                       | Recupera un oggetto figlio in questo oggetto dati di file.<br/>              |
| [**GetChildren**](id3dxfileenumobject--getchildren.md)                 | Recupera il numero di oggetti figlio in questo oggetto dati di file.<br/> |
| [**GetDataObjectById**](id3dxfileenumobject--getdataobjectbyid.md)     | Recupera l'oggetto dati con il GUID specificato.<br/>          |
| [**GetDataObjectByName**](id3dxfileenumobject--getdataobjectbyname.md) | Recupera l'oggetto dati con il nome specificato.<br/>          |
| [**GetFile**](id3dxfileenumobject--getfile.md)                         | Recupera [**l'oggetto ID3DXFile.**](id3dxfile.md)<br/>            |



 

## <a name="remarks"></a>Commenti

Il GUID per l'interfaccia ID3DXFileEnumObject è IID \_ ID3DXFileEnumObject.

Il tipo LPD3DXFILEENUMOBJECT è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXFileEnumObject *LPD3DXFILEENUMOBJECT;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce file D3DX X](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
