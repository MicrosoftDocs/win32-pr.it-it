---
description: Le applicazioni utilizzano i metodi dell'interfaccia ID3DXFileEnumObject per scorrere gli oggetti dati del file figlio nel file e per recuperare un oggetto figlio in base al relativo identificatore univoco globale (GUID) o in base al nome.
ms.assetid: 23b28f07-5832-4163-953b-615d20e781f6
title: Interfaccia ID3DXFileEnumObject (D3DX9Xof. h)
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
ms.openlocfilehash: f9b28f94c8d514f81aaa51426557c825da91c4bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969409"
---
# <a name="id3dxfileenumobject-interface"></a>Interfaccia ID3DXFileEnumObject

Le applicazioni utilizzano i metodi dell'interfaccia ID3DXFileEnumObject per scorrere gli oggetti dati del file figlio nel file e per recuperare un oggetto figlio in base al relativo identificatore univoco globale (GUID) o in base al nome.

## <a name="members"></a>Membri

L'interfaccia **ID3DXFileEnumObject** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFileEnumObject** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXFileEnumObject** dispone di questi metodi.



| Metodo                                                                  | Descrizione                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**GetChild**](id3dxfileenumobject--getchild.md)                       | Recupera un oggetto figlio in questo oggetto dati del file.<br/>              |
| [**GetChildren**](id3dxfileenumobject--getchildren.md)                 | Recupera il numero di oggetti figlio in questo oggetto dati di file.<br/> |
| [**GetDataObjectById**](id3dxfileenumobject--getdataobjectbyid.md)     | Recupera l'oggetto dati con il GUID specificato.<br/>          |
| [**GetDataObjectByName**](id3dxfileenumobject--getdataobjectbyname.md) | Recupera l'oggetto dati con il nome specificato.<br/>          |
| [**GetFile**](id3dxfileenumobject--getfile.md)                         | Recupera l'oggetto [**ID3DXFile**](id3dxfile.md) .<br/>            |



 

## <a name="remarks"></a>Commenti

Il GUID per l'interfaccia ID3DXFileEnumObject è IID \_ ID3DXFileEnumObject.

Il tipo LPD3DXFILEENUMOBJECT è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXFileEnumObject *LPD3DXFILEENUMOBJECT;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di file D3DX X](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
