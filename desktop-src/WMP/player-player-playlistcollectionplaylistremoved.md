---
title: Evento Player.PlaylistCollectionPlaylistRemoved
description: L'evento PlaylistCollectionPlaylistRemoved si verifica quando una playlist viene rimossa dalla raccolta di playlist. | Evento Player.PlaylistCollectionPlaylistRemoved
ms.assetid: 2405be98-b4c2-4b4e-bea6-0c48a3e26f18
keywords:
- Gestore eventi PlaylistCollectionPlaylistRemoved Windows Media Player
- Classe di evento PlaylistCollectionPlaylistRemoved Windows Media Player , Player
- Classe Player Windows Media Player, PlaylistCollectionPlaylistRemoved
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 456f7598b9e1f1d2c2a6e76e58a0b06142980835c3c6d71d9ab10c2230ac386f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118337975"
---
# <a name="playerplaylistcollectionplaylistremoved-event"></a>Evento Player.PlaylistCollectionPlaylistRemoved

**L'evento PlaylistCollectionPlaylistRemoved** si verifica quando una playlist viene rimossa dalla raccolta di playlist.

## <a name="syntax"></a>Sintassi


```JScript
Player.PlaylistCollectionPlaylistRemoved(
  bstrPlaylistName
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrPlaylistName* 
</dt> <dd>

**Stringa** che specifica il nome della playlist rimossa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il valore dei parametri dell'evento viene specificato da Windows Media Player e può essere accessibile o passato a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

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

 

 





