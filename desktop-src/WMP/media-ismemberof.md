---
title: Media. isMemberOf, metodo
description: Il metodo isMemberOf restituisce un valore che indica se l'elemento multimediale è un membro della playlist specificata.
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- Metodo isMemberOf Windows Media Player
- Metodo isMemberOf Windows Media Player, classe media
- Media class Media Player Windows, metodo isMemberOf
topic_type:
- apiref
api_name:
- Media.isMemberOf
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41555bd5910ddb3151468a458c5becbf247ea484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325835"
---
# <a name="mediaismemberof-method"></a>Media. isMemberOf, metodo

Il metodo **isMemberOf** restituisce un valore che indica se l'elemento multimediale è un membro della playlist specificata.

## <a name="syntax"></a>Sintassi


```JScript
bRetVal = Media.isMemberOf(
  playlist
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*playlist* \[ in\]
</dt> <dd>

Oggetto **playlist** che potrebbe contenere l'elemento multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore booleano**.

## <a name="remarks"></a>Commenti

Questo metodo non consente di controllare le playlist recuperate tramite l'oggetto **mediacollection** . Per verificare se un elemento multimediale è un membro di una determinata playlist denominata, recuperare la playlist con *Player*. *PlaylistCollection*. **GetByName**(*Name*). **elemento**(0). Questo metodo può essere usato anche con playlist CD e playlist di metafile.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato il *supporto*. **isMemberOf** per verificare se l'elemento multimediale corrente è un membro della playlist denominata playlist di esempio. In caso contrario, l'elemento multimediale corrente viene aggiunto alla playlist di esempio. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
// Store the playlist object named Sample Playlist.
var sPlaylist = Player.playlistcollection.getbyname("Sample Playlist").item(0);

// Test whether the current media item is a member of Sample Playlist.
 var answer = ((Player.currentMedia.isMemberOf(sPlaylist))?"Yes":"No");

// If the current media item is not a member of Sample Playlist,
// append the current media item to the playlist.
if (answer == "No"){
   sPlaylist.appendItem(Player.currentMedia);
}

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Oggetto playlist**](playlist-object.md)
</dt> <dt>

[**PlaylistCollection (oggetto)**](playlistcollection-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





