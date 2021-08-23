---
title: Metodo playItem IWMPControls
description: Il metodo playItem riproduce l'elemento multimediale specificato. | Metodo playItem IWMPControls
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
ms.openlocfilehash: 1fabab78fe60120110f72176885e3b5825699b83782272dfbef0b48c165d1d02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761031"
---
# <a name="iwmpcontrolsplayitem-method"></a>Metodo IWMPControls::p layItem

Il **metodo playItem** riproduce l'elemento multimediale specificato.

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

*pIWMPMedia* \[ Pollici\]
</dt> <dd>

Interfaccia **WMPLib.IWMPMedia** per l'elemento multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

L'elemento multimediale verrà caricato e riprodotto automaticamente, indipendentemente dal valore della **proprietà IWMPSettings.autoStart.** Per caricare un elemento senza riprodurlo automaticamente, impostare **IWMPSettings.autoStart** su **false** e assegnare un valore a **AxWindowsMediaPlayer.URL**, dopo il quale È possibile chiamare **IWMPControls.play** per avviare la riproduzione dell'elemento.

Nota

**playItem** funziona solo con gli elementi in **AxWindowsMediaPlayer.currentPlaylist**. La **chiamata di playItem** con un riferimento a un elemento multimediale salvato non è supportata.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene **utilizzato playItem** per riprodurre un elemento multimediale dalla playlist corrente. L'elemento da riprodurre viene scelto in base alla relativa posizione nella playlist. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


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
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AxWindowsMediaPlayer.currentPlaylist (VB e C#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls.play (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.Item (VB e C#)**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.autoStart (VB e C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





