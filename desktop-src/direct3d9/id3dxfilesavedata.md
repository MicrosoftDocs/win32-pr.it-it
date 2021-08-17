---
description: Le applicazioni usano i metodi dell'interfaccia ID3DXFileSaveData per aggiungere oggetti dati come elementi figlio di un nodo dati di file con estensione x.
ms.assetid: ab5bdd9a-496a-4ae1-b93a-fe5856bd97d4
title: Interfaccia ID3DXFileSaveData (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68d52c1c022ed292a879ae4f701df52524d4170160bc79b6f1956c744a530c22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121303"
---
# <a name="id3dxfilesavedata-interface"></a>Interfaccia ID3DXFileSaveData

Le applicazioni usano i metodi dell'interfaccia ID3DXFileSaveData per aggiungere oggetti dati come elementi figlio di un nodo dati di file con estensione x.

## <a name="members"></a>Membri

**L'interfaccia ID3DXFileSaveData** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXFileSaveData** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXFileSaveData** include questi metodi.



| Metodo                                                          | Descrizione                                                                                                                                |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDataObject**](id3dxfilesavedata--adddataobject.md)       | Aggiunge un oggetto dati come figlio del nodo dati del file **ID3DXFileSaveData.**<br/>                                                      |
| [**AddDataReference**](id3dxfilesavedata--adddatareference.md) | Aggiunge un riferimento ai dati come figlio di questo nodo dati del file **ID3DXFileSaveData.** Il riferimento ai dati punta a un oggetto dati file.<br/> |
| [**GetId**](id3dxfilesavedata--getid.md)                       | Recupera il GUID di questo nodo dati del file **ID3DXFileSaveData.**<br/>                                                                |
| [**GetName**](id3dxfilesavedata--getname.md)                   | Recupera il nome di questo nodo dati del file **ID3DXFileSaveData.**<br/>                                                                |
| [**GetSave**](id3dxfilesavedata--getsave.md)                   | Recupera un puntatore a questo nodo dati del file [**ID3DXFileSaveObject.**](id3dxfilesaveobject.md)<br/>                                  |
| [**GetType**](id3dxfilesavedata--gettype.md)                   | Recupera l'ID modello di questo nodo dati del file.<br/>                                                                               |



 

## <a name="remarks"></a>Commenti

Il GUID per l'interfaccia ID3DXFileSaveObject è IID \_ ID3DXFileSaveObject.

Il tipo LPD3DXFileSaveData è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXFileSaveData *LPD3DXFILESAVEDATA;
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

 

 
