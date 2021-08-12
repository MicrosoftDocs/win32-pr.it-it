---
title: Metodo Media.isMemberOf
description: Il metodo isMemberOf restituisce un valore che indica se l'elemento multimediale è un membro della playlist specificata.
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- Metodo isMemberOf Windows Media Player
- Metodo isMemberOf Windows Media Player classe Media
- Classe media Windows Media Player metodo , isMemberOf
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
ms.openlocfilehash: ef9fc5eb55a306dad8b9d5de6d6501b615a9156c026c8e0fc12664795a23ab21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574803"
---
# <a name="mediaismemberof-method"></a>Metodo Media.isMemberOf

Il **metodo isMemberOf** restituisce un valore che indica se l'elemento multimediale è un membro della playlist specificata.

## <a name="syntax"></a>Sintassi


```JScript
bRetVal = Media.isMemberOf(
  playlist
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*playlist* \[ Pollici\]
</dt> <dd>

**Oggetto playlist** che potrebbe contenere l'elemento multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un valore **booleano**.

## <a name="remarks"></a>Commenti

Questo metodo non è in grado di controllare le playlist recuperate tramite **l'oggetto MediaCollection.** Per verificare se un elemento multimediale è membro di una determinata playlist denominata, recuperare la playlist con *il lettore*. *playlistCollection*. **getByName**(*name*). **item**(0). Questo metodo può essere usato anche con playlist cd e playlist metafile.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *Media*. **isMemberOf per** verificare se l'elemento multimediale corrente è un membro della playlist denominata Playlist di esempio. In caso contrario, l'elemento multimediale corrente viene aggiunto alla playlist di esempio. **L'oggetto** Player è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Oggetto Playlist**](playlist-object.md)
</dt> <dt>

[**Oggetto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





