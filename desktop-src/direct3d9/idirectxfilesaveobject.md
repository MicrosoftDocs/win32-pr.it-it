---
description: Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileSaveObject per creare oggetti dati e salvare modelli e oggetti dati.
ms.assetid: 7948a7d2-b150-45cf-a1fc-5dca21d74770
title: Interfaccia IDirectXFileSaveObject (DXFile. h)
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
ms.openlocfilehash: 4be69b10037381d4b06466d52483427b6d40499a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322528"
---
# <a name="idirectxfilesaveobject-interface"></a>Interfaccia IDirectXFileSaveObject

Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileSaveObject per creare oggetti dati e salvare modelli e oggetti dati. Si noti che i modelli non sono necessari in ogni file. È ad esempio possibile inserire tutti i modelli in un singolo file Microsoft DirectX anziché duplicarli in ogni file DirectX. Deprecato.

## <a name="members"></a>Membri

L'interfaccia **IDirectXFileSaveObject** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirectXFileSaveObject** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDirectXFileSaveObject** dispone di questi metodi.



| Metodo                                                               | Descrizione                                                                    |
|:---------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**CreateDataObject**](idirectxfilesaveobject--createdataobject.md) | Crea un oggetto dati. Deprecato.<br/>                                  |
| [**SaveData**](idirectxfilesaveobject--savedata.md)                 | Salva un oggetto dati e i relativi elementi figlio in un file DirectX. Deprecato.<br/> |
| [**SaveTemplates**](idirectxfilesaveobject--savetemplates.md)       | Salva i modelli in un file DirectX. Deprecato.<br/>                      |



 

## <a name="remarks"></a>Commenti

L'identificatore univoco globale (GUID) per l'interfaccia IDirectXFileSaveObject è **IID \_ IDirectXFileSaveObject**.

L'interfaccia **IDirectXFileSaveObject** viene ottenuta chiamando il metodo [**IDirectXFile:: CreateSaveObject**](idirectxfile--createsaveobject.md) .

Il tipo **LPDIRECTXFILESAVEOBJECT** è definito come puntatore a questa interfaccia.


```
typedef interface IDirectXFileSaveObject *LPDIRECTXFILESAVEOBJECT;
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

 

 
