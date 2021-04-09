---
description: Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFile per creare istanze delle interfacce IDirectXFileEnumObject e IDirectXFileSaveObject e per registrare i modelli. Deprecato.
ms.assetid: c4e800dc-72a9-4b91-9c89-ee76764b1bb9
title: Interfaccia IDirectXFile (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 0a1e084108580277432aaeb61086b43a97dbd9f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886316"
---
# <a name="idirectxfile-interface"></a>Interfaccia IDirectXFile

Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFile per creare istanze delle interfacce [**IDirectXFileEnumObject**](idirectxfileenumobject.md) e [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) e per registrare i modelli. Deprecato.

## <a name="members"></a>Membri

L'interfaccia **IDirectXFile** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirectXFile** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDirectXFile** dispone di questi metodi.



| Metodo                                                       | Descrizione                                          |
|:-------------------------------------------------------------|:-----------------------------------------------------|
| [**CreateEnumObject**](idirectxfile--createenumobject.md)   | Crea un oggetto enumeratore. Deprecato.<br/> |
| [**CreateSaveObject**](idirectxfile--createsaveobject.md)   | Crea un oggetto Save. Deprecato.<br/>        |
| [**RegisterTemplates**](idirectxfile--registertemplates.md) | Registra i modelli personalizzati. Deprecato.<br/>   |



 

## <a name="remarks"></a>Commenti

L'identificatore univoco globale (GUID) per l'interfaccia IDirectXFile è IID \_ IDirectXFile.

L'interfaccia IDirectXFile viene ottenuta chiamando la funzione [**DirectXFileCreate**](directxfilecreate.md) .

Il tipo LPDIRECTXFILE è definito come puntatore a questa interfaccia.


```
typedef interface IDirectXFile *LPDIRECTXFILE;
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

 

 
