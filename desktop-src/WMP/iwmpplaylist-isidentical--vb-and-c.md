---
title: IWMPPlaylist.isIdentical (VB e C )
description: La proprietà isIdentical (il metodo get isIdentical in C\) ottiene un valore che indica se la playlist specificata è identica alla \_ playlist corrente.
ms.assetid: 0e5520ee-3d41-4e36-98f4-7bc2ec45fcb8
keywords:
- IWMPPlaylist.isIdentical (VB e C ) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca62b1667250b049cf47e797d59bdddea0444c6ea8803ca0fc8daf526289eb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119012"
---
# <a name="iwmpplaylistisidentical-vb-and-c"></a>IWMPPlaylist.isIdentical (VB e C#)

La **proprietà isIdentical** (il **metodo get \_ isIdentical** in C#) ottiene un valore che indica se la playlist specificata è identica alla playlist corrente.


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPPlaylist As IWMPPlaylist
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPPlaylist pIWMPPlaylist
);
```



## <a name="parameters"></a>Parametri

*pIWMPPlaylist*

Interfaccia **WMPLib.IWMPPlaylist** per la playlist confrontata da questo metodo con la playlist corrente.

## <a name="property-value"></a>Valore della proprietà

Valore **System.Boolean** che indica se le playlist confrontate sono identiche.

## <a name="remarks"></a>Commenti

**IWMPPlaylist.isIdentical** è una proprietà in Visual Basic che accetta un parametro , mentre in C# viene definita **metodo \_ isIdentical IWMPPlaylist.get.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





