---
title: Metodo IWMPMedia isMemberOf
description: Il metodo isMemberOf restituisce un valore che indica se l'elemento multimediale specificato è un membro della playlist specificata.
ms.assetid: 491e0dd5-38e5-47a5-9c94-f1d27d297f8d
keywords:
- Metodo isMemberOf Windows Media Player
- Metodo isMemberOf Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, metodo isMemberOf
topic_type:
- apiref
api_name:
- IWMPMedia.isMemberOf
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f627e9b2f0e1c4b226dda13d280d521ad52df2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332391"
---
# <a name="iwmpmediaismemberof-method"></a>Metodo IWMPMedia:: isMemberOf

Il metodo **isMemberOf** restituisce un valore che indica se l'elemento multimediale specificato è un membro della playlist specificata.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean isMemberOf(
  IWMPPlaylist pPlaylist
);
```


```VB

Public Function isMemberOf( _
  ByVal pPlaylist As IWMPPlaylist _
) As System.Boolean
Implements IWMPMedia.isMemberOf
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*pPlaylist* \[ in\]
</dt> <dd>

Interfaccia **wmplib. IWMPPlaylist** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore **System. Boolean** che indica se l'elemento multimediale è un membro della playlist.

## <a name="remarks"></a>Commenti

Questo metodo non consente di controllare le playlist recuperate tramite l'interfaccia **IWMPMediaCollection** . Per verificare se un elemento multimediale è un membro di una determinata playlist denominata, recuperare la raccolta di playlist con la proprietà **AxWindowsMediaPlayer. PlaylistCollection** . Una volta recuperata la raccolta, recuperare la singola playlist chiamando il metodo **IWMPPlaylistCollection. GetByName** .

Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **isMemberOf** per verificare se l'elemento multimediale corrente è un membro della playlist denominata All Music. In caso contrario, l'elemento multimediale corrente viene aggiunto alla playlist. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
// Get an interface to the playlist named All Music.
WMPLib.IWMPPlaylist sPlaylist = player.playlistCollection.getByName("All Music").Item(0);

// Test whether the current media item is a member of the All Music playlist.
// If it is not a member, append the current media item to the playlist.
if (player.currentMedia.isMemberOf(sPlaylist) == false)
{
    sPlaylist.appendItem(player.currentMedia);
}
```


```VB

' Get an interface to the playlist named All Music.
Dim sPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Test whether the current media item is a member of the All Music playlist.
&#39; If it is not a member, then append the current media item to the playlist.
If (player.currentMedia.isMemberOf(sPlaylist) = False) Then

    sPlaylist.appendItem(player.currentMedia)

End If
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AxWindowsMediaPlayer. PlaylistCollection (VB e C#)**](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getByName (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





