---
title: Evento Player. PlaylistCollectionPlaylistAdded
description: L'evento PlaylistCollectionPlaylistAdded si verifica quando viene aggiunta una playlist alla raccolta playlist. | Evento Player. PlaylistCollectionPlaylistAdded
ms.assetid: 07acb5e6-d832-4f0b-a6bb-2b7ba27c368d
keywords:
- Media Player di Windows Event PlaylistCollectionPlaylistAdded
- Windows Event PlaylistCollectionPlaylistAdded Media Player, classe Player
- Classe Player Windows Media Player, evento PlaylistCollectionPlaylistAdded
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
ms.openlocfilehash: 6e6a229aff95d29ae93433dab538521d88c50c1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329070"
---
# <a name="playerplaylistcollectionplaylistadded-event"></a>Evento Player. PlaylistCollectionPlaylistAdded

L'evento **PlaylistCollectionPlaylistAdded** si verifica quando viene aggiunta una playlist alla raccolta playlist.

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

Il nome della playlist aggiunta può essere usato per recuperare l'oggetto **playlist** corrispondente usando *PlaylistCollection*. metodo **GetByName** .

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

 

 





