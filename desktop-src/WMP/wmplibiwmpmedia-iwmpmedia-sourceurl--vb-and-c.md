---
title: Proprietà sourceURL di IWMPMedia
description: La proprietà sourceURL Ottiene l'URL dell'elemento multimediale.
ms.assetid: adaef82c-eeed-4cce-859b-c54b9c8fa085
keywords:
- Finestra delle proprietà di sourceURL Media Player
- Proprietà di sourceURL Media Player Windows, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, proprietà sourceURL
topic_type:
- apiref
api_name:
- IWMPMedia.sourceURL
- IWMPMedia.get_sourceURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ad2cdb2c0a67f65f7b0cf722d1b613307806d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328576"
---
# <a name="iwmpmediasourceurl-property"></a>Proprietà IWMPMedia:: sourceURL

La proprietà **sourceURL** Ottiene l'URL dell'elemento multimediale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String sourceURL {get;}
```


```VB

Public ReadOnly Property sourceURL As System.String
```





## <a name="property-value"></a>Valore proprietà

**System. String** che rappresenta l'URL di origine.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **sourceURL** per recuperare l'URL del primo elemento multimediale nella playlist "All Music"; l'URL dell'elemento multimediale viene quindi assegnato alla proprietà URL oggetto Player. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
// Get an interface to the All Music Playlist. 
WMPLib.IWMPPlaylist pl = player.playlistCollection.getByName("All Music").Item(0);

// Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)pl.get_Item(0);

// Change the URL property of the player to the URL of the media item.
player.URL = media.sourceURL;

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Get an interface to the All Music Playlist. 
Dim pl As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
Dim media As WMPLib.IWMPMedia3 = pl.Item(0)

&#39; Change the URL property of the player to the URL of the media item.
player.URL = Media.sourceURL

&#39; Play the media item.
player.Ctlcontrols.play()
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





