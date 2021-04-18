---
title: IWMPPlaylist. è identico (VB e C)
description: La proprietà IsValid (il metodo Get è \_ identico in C \) ottiene un valore che indica se la playlist specificata è identica alla playlist corrente.
ms.assetid: 0e5520ee-3d41-4e36-98f4-7bc2ec45fcb8
keywords:
- Windows Media Player IWMPPlaylist. è identico (VB e C)
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
ms.openlocfilehash: bee30441e8f0275bba06f71a01095c39da8eae9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324990"
---
# <a name="iwmpplaylistisidentical-vb-and-c"></a>IWMPPlaylist. è identico (VB e C#)

La **proprietà IsValid (il** metodo **Get è \_ identico** in C#) ottiene un valore che indica se la playlist specificata è identica alla playlist corrente.


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

Interfaccia **wmplib. IWMPPlaylist** per la playlist che questo metodo confronta con la playlist corrente.

## <a name="property-value"></a>Valore della proprietà

**System. Boolean** che indica se le playlist confrontate sono identiche.

## <a name="remarks"></a>Commenti

**IWMPPlaylist.** IsValid è una proprietà in Visual Basic che accetta un parametro, mentre in C# è indicato come **IWMPPlaylist. Get \_** metodo IsValid.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





