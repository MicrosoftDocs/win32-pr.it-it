---
description: Le applicazioni usano i metodi dell'interfaccia IDirectXFileObject per recuperare informazioni sugli oggetti file Microsoft DirectX. Deprecato.
ms.assetid: 015d2c4e-4a25-40da-b88a-bad0c4e20e09
title: Interfaccia IDirectXFileObject (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 3aa0ffffb8766707841fa0a4a5ec54fe0db9caf1d86b885afc36bffa5f8352d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951301"
---
# <a name="idirectxfileobject-interface"></a>Interfaccia IDirectXFileObject

Le applicazioni usano i metodi dell'interfaccia IDirectXFileObject per recuperare informazioni sugli oggetti file Microsoft DirectX. Deprecato.

## <a name="members"></a>Membri

**L'interfaccia IDirectXFileObject** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDirectXFileObject** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IDirectXFileObject.**



| Metodo                                         | Descrizione                                                                                   |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**GetId**](idirectxfileobject--getid.md)     | Recupera un puntatore al GUID che identifica un oggetto file DirectX. Deprecato.<br/> |
| [**GetName**](idirectxfileobject--getname.md) | Recupera un puntatore al nome di un oggetto file DirectX. Deprecato.<br/>                   |



 

## <a name="remarks"></a>Commenti

Il GUID per l'interfaccia IDirectXFileObject è IID \_ IDirectXFileObject.

Il tipo LPDIRECTXFILEOBJECT è definito come puntatore a questa interfaccia.


```
typedef interface IDirectXFileObject *LPDIRECTXFILEOBJECT;
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

 

 
