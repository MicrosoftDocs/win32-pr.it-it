---
title: Evento Player. PlaylistCollectionPlaylistRemoved
description: L'evento PlaylistCollectionPlaylistRemoved si verifica quando una playlist viene rimossa dalla raccolta di playlist. | Evento Player. PlaylistCollectionPlaylistRemoved
ms.assetid: 2405be98-b4c2-4b4e-bea6-0c48a3e26f18
keywords:
- Media Player di Windows Event PlaylistCollectionPlaylistRemoved
- Windows Event PlaylistCollectionPlaylistRemoved Media Player, classe Player
- Classe Player Windows Media Player, evento PlaylistCollectionPlaylistRemoved
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
ms.openlocfilehash: a449a7b00516f4fee613722d1cc126eb74227948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332672"
---
# <a name="playerplaylistcollectionplaylistremoved-event"></a>Evento Player. PlaylistCollectionPlaylistRemoved

L'evento **PlaylistCollectionPlaylistRemoved** si verifica quando una playlist viene rimossa dalla raccolta di playlist.

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

**Stringa** che specifica il nome della playlist che è stata rimossa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**PlaylistCollection. getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





