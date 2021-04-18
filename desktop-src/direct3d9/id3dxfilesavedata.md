---
description: Le applicazioni utilizzano i metodi dell'interfaccia ID3DXFileSaveData per aggiungere oggetti dati come elementi figlio di un nodo dati del file con estensione x.
ms.assetid: ab5bdd9a-496a-4ae1-b93a-fe5856bd97d4
title: Interfaccia ID3DXFileSaveData (D3DX9Xof. h)
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
ms.openlocfilehash: d42f431dbb2f9108c5e503aea07ba6b11915f0ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322623"
---
# <a name="id3dxfilesavedata-interface"></a>Interfaccia ID3DXFileSaveData

Le applicazioni utilizzano i metodi dell'interfaccia ID3DXFileSaveData per aggiungere oggetti dati come elementi figlio di un nodo dati del file con estensione x.

## <a name="members"></a>Membri

L'interfaccia **ID3DXFileSaveData** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFileSaveData** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXFileSaveData** dispone di questi metodi.



| Metodo                                                          | Descrizione                                                                                                                                |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDataObject**](id3dxfilesavedata--adddataobject.md)       | Aggiunge un oggetto dati come figlio del nodo dati del file **ID3DXFileSaveData** .<br/>                                                      |
| [**AddDataReference**](id3dxfilesavedata--adddatareference.md) | Aggiunge un riferimento ai dati come figlio del nodo dati del file **ID3DXFileSaveData** . Il riferimento ai dati punta a un oggetto dati di file.<br/> |
| [**GetId**](id3dxfilesavedata--getid.md)                       | Recupera il GUID del nodo dati del file **ID3DXFileSaveData** .<br/>                                                                |
| [**GetName**](id3dxfilesavedata--getname.md)                   | Recupera il nome del nodo dati del file **ID3DXFileSaveData** .<br/>                                                                |
| [**Getsave**](id3dxfilesavedata--getsave.md)                   | Recupera un puntatore a questo nodo dati del file [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .<br/>                                  |
| [**GetType**](id3dxfilesavedata--gettype.md)                   | Recupera l'ID modello del nodo dati del file.<br/>                                                                               |



 

## <a name="remarks"></a>Commenti

Il GUID per l'interfaccia ID3DXFileSaveObject è IID \_ ID3DXFileSaveObject.

Il tipo LPD3DXFileSaveData è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXFileSaveData *LPD3DXFILESAVEDATA;
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

 

 
