---
title: AxWindowsMediaPlayer.currentPlaylist - proprietà
description: La proprietà currentPlaylist ottiene o imposta l'interfaccia IWMPPlaylist corrente che offre un modo semplice per organizzare e modificare gli elementi multimediali in un elenco.
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- Proprietà currentPlaylist Windows Media Player
- Proprietà currentPlaylist Windows Media Player , classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player , proprietà currentPlaylist
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
ms.openlocfilehash: f976084773a333e40c0a278878e9a35ed913e5911ec732c0dccfe6525e5f45a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765262"
---
# <a name="axwindowsmediaplayercurrentplaylist-property"></a>AxWindowsMediaPlayer.currentPlaylist - proprietà

La proprietà currentPlaylist ottiene o imposta l'interfaccia **IWMPPlaylist** corrente che offre un modo semplice per organizzare e modificare gli elementi multimediali in un elenco.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPPlaylist currentPlaylist {get; set;}
```


```VB

Public Property currentPlaylist As IWMPPlaylist
```





## <a name="property-value"></a>Valore proprietà

Interfaccia WMPLib.IWMPPlaylist che fornisce l'accesso alla playlist corrente.

## <a name="remarks"></a>Commenti

Se la proprietà IWMPSettings.autoStart (accessibile anche tramite AxWindowsMediaPlayer.settings).**autoStart**) è true, la riproduzione inizia automaticamente ogni volta che si imposta **currentPlaylist**.

Questa proprietà accetta un'interfaccia IWMPPlaylist, che può essere acquisita in diversi modi, ad esempio ottenendo il valore da *IWMPPlaylistArray.* **Item** o *IWMPPlaylistCollection.* **Proprietà newPlaylist.** Per caricare un **elemento della playlist** usando un nome file, impostare la proprietà URL o usare AxWindowsMediaPlayer. **newPlaylist**.

## <a name="examples"></a>Esempio

L'esempio seguente recupera la prima playlist nella libreria e usa la proprietà currentPlaylist per impostare la playlist recuperata come playlist corrente e visualizzarne il nome. L'oggetto AxWMPLib.AxWindowsMediaPlayer è rappresentato dalla variabile denominata player.


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
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.newPlaylist (VB e C#)**](axwmplib-axwindowsmediaplayer-newplaylist.md)
</dt> <dt>

[**AxWindowsMediaPlayer.settings (VB e C#)**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray.Item (VB e C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-item--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.newPlaylist (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.autoStart (VB e C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





