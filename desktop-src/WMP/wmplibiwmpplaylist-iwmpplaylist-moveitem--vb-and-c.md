---
title: Metodo moveItem IWMPPlaylist
description: Il metodo moveItem modifica la posizione di un elemento multimediale nella playlist.
ms.assetid: e82c820f-4640-4289-88c1-79a92e520f00
keywords:
- Metodo moveItem Windows Media Player
- Metodo moveItem Windows Media Player, interfaccia IWMPPlaylist
- Interfaccia IWMPPlaylist Windows Media Player, metodo moveItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.moveItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f2c4f2aa3d4478a114e405b1b40816fc1697c2c291c272aabc68db3813766d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760661"
---
# <a name="iwmpplaylistmoveitem-method"></a>Metodo IWMPPlaylist::moveItem

Il **metodo moveItem** modifica la posizione di un elemento multimediale nella playlist.

## <a name="syntax"></a>Sintassi


```CSharp
public void moveItem(
  System.Int32 lIndexOld,
  System.Int32 lIndexNew
);
```


```VB

Public Sub moveItem( _
  ByVal lIndexOld As System.Int32, _
  ByVal lIndexNew As System.Int32 _
)
Implements IWMPPlaylist.moveItem
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*lIndexOld* \[ Pollici\]
</dt> <dd>

**System.Int32** che rappresenta l'indice originale.

</dd> <dt>

*lIndexNew* \[ Pollici\]
</dt> <dd>

**System.Int32** che rappresenta il nuovo indice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

I numeri di indice di tutti gli elementi dopo l'elemento inserito saranno aumentati di uno.

Prima di chiamare questo metodo, è necessario avere accesso completo alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





