---
description: Le applicazioni usano i metodi dell'interfaccia ID3DXFileSaveObject per scrivere un file con estensione x su disco e per aggiungere e salvare oggetti dati e modelli.
ms.assetid: 1131c151-fa21-4654-9776-484922d58487
title: Interfaccia ID3DXFileSaveObject (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6efb87f92a81ec40fe919d76d18a9746e0d88c45f19616933f1b014402aa3e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121185"
---
# <a name="id3dxfilesaveobject-interface"></a>Interfaccia ID3DXFileSaveObject

Le applicazioni usano i metodi dell'interfaccia ID3DXFileSaveObject per scrivere un file con estensione x su disco e per aggiungere e salvare oggetti dati e modelli.

## <a name="members"></a>Membri

**L'interfaccia ID3DXFileSaveObject** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXFileSaveObject** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXFileSaveObject** include questi metodi.



| Metodo                                                      | Descrizione                                                                                                                  |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**AddDataObject**](id3dxfilesaveobject--adddataobject.md) | Aggiunge un oggetto dati come figlio [**dell'oggetto ID3DXFileSaveData.**](id3dxfilesavedata.md)<br/>                       |
| [**GetFile**](id3dxfilesaveobject--getfile.md)             | Ottiene [**l'interfaccia ID3DXFile**](id3dxfile.md) dell'oggetto che ha creato questo **oggetto ID3DXFileSaveObject.**<br/> |
| [**Salva**](id3dxfilesaveobject--save.md)                   | Salva un oggetto dati e i relativi elementi figlio in un file con estensione x su disco.<br/>                                                        |



 

## <a name="remarks"></a>Commenti

I modelli non sono necessari in ogni file. Ad esempio, è possibile inserire tutti i modelli in un singolo file con estensione x anziché duplicarli in ogni file con estensione x.

L'interfaccia ID3DXFileSaveObject viene ottenuta chiamando il [**metodo ID3DXFile::CreateSaveObject.**](id3dxfile--createsaveobject.md)

L'identificatore univoco globale (GUID) per l'interfaccia ID3DXFileSaveObject è IID \_ ID3DXFileSaveObject.

Il tipo LPD3DXFILESAVEOBJECT è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXFileSaveObject *LPD3DXFILESAVEOBJECT;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di file D3DX X](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
