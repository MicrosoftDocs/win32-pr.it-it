---
title: PlaylistCollection. importPlaylist, metodo
description: Il metodo importPlaylist aggiunge una playlist statica alla libreria. | PlaylistCollection. importPlaylist, metodo
ms.assetid: 0611ba42-fd8f-4fb9-9fbb-809a82775c2a
keywords:
- Metodo importPlaylist Windows Media Player
- Metodo importPlaylist Windows Media Player, Classe PlaylistCollection
- Classe PlaylistCollection Windows Media Player, metodo importPlaylist
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
ms.openlocfilehash: 736e9afa17f571428fada48660726b606268796a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329433"
---
# <a name="playlistcollectionimportplaylist-method"></a>PlaylistCollection. importPlaylist, metodo

Il metodo **importPlaylist** aggiunge una playlist statica alla libreria.

## <a name="syntax"></a>Sintassi


```JScript
retVal = PlaylistCollection.importPlaylist(
  playlist
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*playlist* \[ in\]
</dt> <dd>

Oggetto **playlist** da aggiungere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce l'oggetto **playlist** che è stato aggiunto.

## <a name="remarks"></a>Commenti

Le playlist che non contengono elementi multimediali non possono essere aggiunte alla libreria utilizzando questo metodo. Per creare una playlist vuota nella libreria, usare il metodo **nuova playlist** . È quindi possibile compilare la playlist risultante con elementi multimediali usando *playlist*. **appendItem** o *playlist*. **InsertItem**.

Se si passa questo metodo una playlist automatica, la query viene eseguita una volta e il risultato viene aggiunto alla libreria come playlist statica. Per aggiungere una playlist automatica alla libreria e mantenerne il comportamento automatico, usare *mediacollection*. **Aggiungi**. Per altre informazioni, vedere [playlist statiche e automatiche](static-and-auto-playlists.md).

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Gestione delle playlist**](managing-playlists.md)
</dt> <dt>

[**Mediacollection (oggetto)**](mediacollection-object.md)
</dt> <dt>

[**Mediacollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Playlist. appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Playlist. insertItem**](playlist-insertitem.md)
</dt> <dt>

[**PlaylistCollection (oggetto)**](playlistcollection-object.md)
</dt> <dt>

[**PlaylistCollection. nuova playlist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**PlaylistCollection. Remove**](playlistcollection-remove.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





