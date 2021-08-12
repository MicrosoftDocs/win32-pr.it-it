---
title: Evento Player.PlaylistCollectionPlaylistAdded
description: L'evento PlaylistCollectionPlaylistAdded si verifica quando viene aggiunta una playlist alla raccolta di playlist. | Evento Player.PlaylistCollectionPlaylistAdded
ms.assetid: 07acb5e6-d832-4f0b-a6bb-2b7ba27c368d
keywords:
- Gestore eventi PlaylistCollectionPlaylistAdded Windows Media Player
- Classe di evento PlaylistCollectionPlaylistAdded Windows Media Player , Player
- Classe Player Windows Media Player, PlaylistCollectionPlaylistAdded
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e72dcacbb60c141348a295fe086957b1404475e9e3be90433f8bdbe816fc834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572590"
---
# <a name="playerplaylistcollectionplaylistadded-event"></a>Evento Player.PlaylistCollectionPlaylistAdded

**L'evento PlaylistCollectionPlaylistAdded** si verifica quando viene aggiunta una playlist alla raccolta di playlist.

## <a name="syntax"></a>Sintassi


```JScript
Player.PlaylistCollectionPlaylistAdded(
  bstrPlaylistName
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrPlaylistName* 
</dt> <dd>

**Stringa** che specifica il nome della playlist aggiunta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il nome della playlist aggiunta può essere usato per recuperare l'oggetto **Playlist** corrispondente usando *PlaylistCollection.* **Metodo getByName.**

Il valore dei parametri dell'evento viene specificato da Windows Media Player ed è accessibile o passato a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





