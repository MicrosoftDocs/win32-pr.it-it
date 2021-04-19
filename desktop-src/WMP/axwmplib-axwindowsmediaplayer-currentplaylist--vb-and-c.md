---
title: Proprietà AxWindowsMediaPlayer. currentPlaylist
description: La proprietà currentPlaylist Ottiene o imposta l'interfaccia IWMPPlaylist corrente che fornisce un modo semplice per organizzare e modificare gli elementi multimediali in un elenco.
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- Finestra delle proprietà di currentPlaylist Media Player
- Proprietà currentPlaylist Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Media Player Windows, proprietà currentPlaylist
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0f5b91a2e65b81fd1f13da0bad5f77c5ea1415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330129"
---
# <a name="axwindowsmediaplayercurrentplaylist-property"></a>Proprietà AxWindowsMediaPlayer. currentPlaylist

La proprietà currentPlaylist Ottiene o imposta l'interfaccia **IWMPPlaylist** corrente che fornisce un modo semplice per organizzare e modificare gli elementi multimediali in un elenco.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPPlaylist currentPlaylist {get; set;}
```


```VB

Public Property currentPlaylist As IWMPPlaylist
```





## <a name="property-value"></a>Valore proprietà

Interfaccia WMPLib. IWMPPlaylist che fornisce l'accesso alla playlist corrente.

## <a name="remarks"></a>Commenti

Se la proprietà IWMPSettings. AutoStart (accessibile anche tramite AxWindowsMediaPlayer. Settings.**autostart**) è true, la riproduzione viene avviata automaticamente quando si imposta **currentPlaylist**.

Questa proprietà accetta un'interfaccia IWMPPlaylist, che può essere acquisita in diversi modi, ad esempio ottenendo il valore da *IWMPPlaylistArray*. **Elemento** o *IWMPPlaylistCollection*. proprietà **nuova playlist** . Per caricare un elemento della **playlist** usando un nome di file, impostare la proprietà URL o usare AxWindowsMediaPlayer. **nuova playlist**.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene recuperata la prima playlist nella libreria e viene utilizzata la proprietà currentPlaylist per impostare la playlist recuperata come playlist corrente e visualizzarne il nome. L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.


```CSharp
// Get an interface to the first playlist from the library. 
WMPLib.IWMPPlaylist firstPlaylist = player.playlistCollection.getAll().Item(0);

// Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist;

// Display the name of the current playlist.
currentPlaylistLabel.Text = ("Found first playlist. Name = " + player.currentPlaylist.name);
```


```VB

' Get an interface to the first playlist from the library. 
Dim firstPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getAll().Item(0)

&#39; Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist

&#39; Display the name of the current playlist.
currentPlaylistLabel.Text = (&quot;Found first playlist. Name = &quot; + player.currentPlaylist.name)
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. nuova playlist (VB e C#)**](axwmplib-axwindowsmediaplayer-newplaylist.md)
</dt> <dt>

[**AxWindowsMediaPlayer. Settings (VB e C#)**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray. Item (VB e C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-item--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. nuova playlist (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. AutoStart (VB e C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





