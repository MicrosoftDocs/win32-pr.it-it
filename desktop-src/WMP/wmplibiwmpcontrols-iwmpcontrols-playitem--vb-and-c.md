---
title: Metodo IWMPControls playItem
description: Il metodo playItem riproduce l'elemento multimediale specificato. | Metodo IWMPControls playItem
ms.assetid: ddd4e4f7-475c-4964-a623-9123ed66be8e
keywords:
- Metodo playItem Windows Media Player
- Metodo playItem Windows Media Player, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, metodo playItem
topic_type:
- apiref
api_name:
- IWMPControls.playItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2ac11f93409128eccc88c1d916144615d77476
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332471"
---
# <a name="iwmpcontrolsplayitem-method"></a>IWMPControls::p metodo layItem

Il metodo **playItem** riproduce l'elemento multimediale specificato.

## <a name="syntax"></a>Sintassi


```CSharp
public void playItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub playItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPControls.playItem
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*pIWMPMedia* \[ in\]
</dt> <dd>

Interfaccia **wmplib. IWMPMedia** per l'elemento multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

L'elemento multimediale verrà caricato e riprodotto automaticamente, indipendentemente dal valore della proprietà **IWMPSettings. autostart** . Per caricare un elemento senza riprodurlo automaticamente, impostare **IWMPSettings. autostart** su **false** e assegnare un valore a **AxWindowsMediaPlayer. URL**, dopo il quale è possibile chiamare **IWMPControls. Play** per avviare la riproduzione dell'elemento.

Nota

**playItem** funziona solo con gli elementi in **AxWindowsMediaPlayer. currentPlaylist**. La chiamata di **playItem** con un riferimento a un elemento multimediale salvato non è supportata.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **playItem** per riprodurre un elemento multimediale dalla playlist corrente. L'elemento da riprodurre viene scelto in base alla relativa posizione nella playlist. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
int index = 3;

// Get the media item at the fourth position in the current playlist.
WMPLib.IWMPMedia media = player.currentPlaylist.get_Item(index);

// Play the media item.
player.Ctlcontrols.playItem(media);
```


```VB

' Declare a variable to hold the position of the media item 
&#39; in the current playlist. An arbitrary value is supplied here.
Dim index As Integer = 3

&#39; Get the media item at the fourth position in the current playlist.
Dim Media As WMPLib.IWMPMedia = player.currentPlaylist.Item(index)

&#39; Play the media item.
player.Ctlcontrols.playItem(Media)
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AxWindowsMediaPlayer. currentPlaylist (VB e C#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Play (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. Item (VB e C#)**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. AutoStart (VB e C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





