---
title: AxWindowsMediaPlayer.currentMedia - proprietà
description: La proprietà currentMedia ottiene o imposta l'interfaccia IWMPMedia che corrisponde all'elemento multimediale corrente.
ms.assetid: 814ccb1d-713d-4b91-b225-d2199a7c9b6b
keywords:
- proprietà currentMedia Windows Media Player
- proprietà currentMedia Windows Media Player , classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player , proprietà currentMedia
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027949872b2ff988fcfcad5a8464d9a48ed69d3389ddbca0ad4f91b2d9e3c8d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098841"
---
# <a name="axwindowsmediaplayercurrentmedia-property"></a>AxWindowsMediaPlayer.currentMedia - proprietà

La proprietà currentMedia ottiene o imposta l'interfaccia IWMPMedia che corrisponde all'elemento multimediale corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPMedia currentMedia {get; set;}
```


```VB

Public Property currentMedia As IWMPMedia
```





## <a name="property-value"></a>Valore proprietà

Interfaccia WMPLib.IWMPMedia che fornisce l'accesso all'elemento multimediale corrente.

## <a name="remarks"></a>Commenti

Se axWindowsMediaPlayer.settings. **la proprietà autoStart** è true, la riproduzione inizia automaticamente ogni volta che si imposta **currentMedia.**

È possibile recuperare un'interfaccia IWMPMedia per un determinato elemento multimediale tramite la proprietà IWMPPlaylist.Item (metodo IWMPPlaylist.get \_ Item in C#). Per caricare un elemento multimediale usando un nome file, impostare la proprietà URL o usare newMedia.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene recuperato il primo elemento multimediale nella libreria e viene utilizzata la proprietà currentMedia per impostare l'elemento multimediale recuperato come elemento multimediale corrente e visualizzarne il nome. L'oggetto AxWMPLib.AxWindowsMediaPlayer è rappresentato dalla variabile denominata player.


```CSharp
// Get an interface to the first media item in the library. 
WMPLib.IWMPMedia3 firstMedia = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Make the retrieved media item the current media item.
player.currentMedia = firstMedia;

// Display the name of the current media item.
currentMediaLabel.Text = ("Found first media item. Name = " + player.currentMedia.name);
```


```VB

' Get an interface to the first media item in the library. 
Dim firstMedia As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Make the retrieved media item the current media item.
player.currentMedia = firstMedia

&#39; Display the name of the current media item.
currentMediaLabel.Text = (&quot;Found first media item. Name = &quot; + player.currentMedia.name)
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

[**AxWindowsMediaPlayer.newMedia (VB e C#)**](axwmplib-axwindowsmediaplayer-newmedia.md)
</dt> <dt>

[**AxWindowsMediaPlayer.URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.Item (VB e C#)**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.autoStart (VB e C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





