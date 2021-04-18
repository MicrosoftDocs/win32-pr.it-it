---
title: Metodo IWMPPlaylist removeItem
description: Il metodo removeItem rimuove l'elemento multimediale specificato dalla playlist.
ms.assetid: 8b5a4c34-863d-4963-97c8-cc5aa2223ab5
keywords:
- Metodo removeItem Windows Media Player
- Metodo removeItem Windows Media Player, interfaccia IWMPPlaylist
- Interfaccia IWMPPlaylist Windows Media Player, metodo removeItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.removeItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec845b7657e04f17c47119dd169032ebe5815786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325966"
---
# <a name="iwmpplaylistremoveitem-method"></a>Metodo IWMPPlaylist:: removeItem

Il metodo **RemoveItem** rimuove l'elemento multimediale specificato dalla playlist.

## <a name="syntax"></a>Sintassi


```CSharp
public void removeItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub removeItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.removeItem
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*pIWMPMedia* \[ in\]
</dt> <dd>

Interfaccia **wmplib. IWMPMedia** che rappresenta l'elemento multimediale da rimuovere dalla playlist.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se l'elemento rimosso è la traccia attualmente in esecuzione, la riproduzione viene arrestata e l'elemento successivo nella playlist diventa quello corrente.

Se non è presente alcun elemento successivo, viene usato l'elemento precedente. Se non sono presenti altri elementi, la proprietà **AxWindowsMediaPlayer. currentMedia** restituirà **null**.

Prima di chiamare questo metodo, è necessario disporre dell'accesso completo alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AxWindowsMediaPlayer. currentMedia (VB e C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. insertItem (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. Item (VB e C#)**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





