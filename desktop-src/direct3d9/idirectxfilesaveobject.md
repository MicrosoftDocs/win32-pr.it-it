---
description: Le applicazioni usano i metodi dell'interfaccia IDirectXFileSaveObject per creare oggetti dati e salvare modelli e oggetti dati.
ms.assetid: 7948a7d2-b150-45cf-a1fc-5dca21d74770
title: Interfaccia IDirectXFileSaveObject (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 7274ca544d7164400fc528fdec6f9640647126989637aa75929a3a9ae1cb72ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846901"
---
# <a name="idirectxfilesaveobject-interface"></a>Interfaccia IDirectXFileSaveObject

Le applicazioni usano i metodi dell'interfaccia IDirectXFileSaveObject per creare oggetti dati e salvare modelli e oggetti dati. Si noti che i modelli non sono necessari in ogni file. Ad esempio, è possibile inserire tutti i modelli in un singolo file Microsoft DirectX anziché duplicarli in ogni file DirectX. Deprecato.

## <a name="members"></a>Membri

**L'interfaccia IDirectXFileSaveObject** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDirectXFileSaveObject** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IDirectXFileSaveObject.**



| Metodo                                                               | Descrizione                                                                    |
|:---------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**CreateDataObject**](idirectxfilesaveobject--createdataobject.md) | Crea un oggetto dati. Deprecato.<br/>                                  |
| [**SaveData**](idirectxfilesaveobject--savedata.md)                 | Salva un oggetto dati e i relativi elementi figlio in un file DirectX. Deprecato.<br/> |
| [**SaveTemplates**](idirectxfilesaveobject--savetemplates.md)       | Salva i modelli in un file DirectX. Deprecato.<br/>                      |



 

## <a name="remarks"></a>Commenti

L'identificatore univoco globale (GUID) per l'interfaccia IDirectXFileSaveObject è **IID \_ IDirectXFileSaveObject.**

**L'interfaccia IDirectXFileSaveObject** viene ottenuta chiamando il [**metodo IDirectXFile::CreateSaveObject.**](idirectxfile--createsaveobject.md)

Il **tipo LPDIRECTXFILESAVEOBJECT** è definito come puntatore a questa interfaccia.


```
typedef interface IDirectXFileSaveObject *LPDIRECTXFILESAVEOBJECT;
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

 

 
