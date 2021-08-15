---
title: Metodo PlaylistCollection.importPlaylist
description: Il metodo importPlaylist aggiunge una playlist statica alla libreria. | Metodo PlaylistCollection.importPlaylist
ms.assetid: 0611ba42-fd8f-4fb9-9fbb-809a82775c2a
keywords:
- Metodo importPlaylist Windows Media Player
- Metodo importPlaylist Windows Media Player , classe PlaylistCollection
- Classe PlaylistCollection Windows Media Player , metodo importPlaylist
topic_type:
- apiref
api_name:
- PlaylistCollection.importPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f6c2a61b6603c0bfb38025548eaa4b0943bcdd1a5e81cb1ac27c17969fe87ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334843"
---
# <a name="playlistcollectionimportplaylist-method"></a>Metodo PlaylistCollection.importPlaylist

Il **metodo importPlaylist** aggiunge una playlist statica alla libreria.

## <a name="syntax"></a>Sintassi


```JScript
retVal = PlaylistCollection.importPlaylist(
  playlist
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*playlist* \[ Pollici\]
</dt> <dd>

**Oggetto playlist** da aggiungere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce **l'oggetto Playlist** aggiunto.

## <a name="remarks"></a>Commenti

Le playlist che non contengono elementi multimediali non possono essere aggiunte alla libreria usando questo metodo. Per creare una playlist vuota nella libreria, usare il **metodo newPlaylist.** È quindi possibile riempire la playlist risultante con elementi multimediali usando *Playlist*. **appendItem o** *Playlist.* **insertItem**.

Se si passa questo metodo a una playlist automatica, la query viene eseguita una sola volta e il risultato viene aggiunto alla libreria come playlist statica. Per aggiungere una playlist automatica alla libreria e mantenere il comportamento automatico, usare *MediaCollection*. **aggiungere**. Per altre informazioni, vedere [Playlist statiche e auto.](static-and-auto-playlists.md)

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Gestione delle playlist**](managing-playlists.md)
</dt> <dt>

[**Oggetto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection.add**](mediacollection-add.md)
</dt> <dt>

[**Playlist.appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Playlist.insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Oggetto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**PlaylistCollection.newPlaylist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**PlaylistCollection.remove**](playlistcollection-remove.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





