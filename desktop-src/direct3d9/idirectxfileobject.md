---
description: Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileObject per recuperare informazioni sugli oggetti file Microsoft DirectX. Deprecato.
ms.assetid: 015d2c4e-4a25-40da-b88a-bad0c4e20e09
title: Interfaccia IDirectXFileObject (DXFile. h)
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
ms.openlocfilehash: e03f4a80c0cff25fa9416d35c20f2d60d17b206b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322533"
---
# <a name="idirectxfileobject-interface"></a>Interfaccia IDirectXFileObject

Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileObject per recuperare informazioni sugli oggetti file Microsoft DirectX. Deprecato.

## <a name="members"></a>Membri

L'interfaccia **IDirectXFileObject** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirectXFileObject** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDirectXFileObject** dispone di questi metodi.



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
| Intestazione<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di file X](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
