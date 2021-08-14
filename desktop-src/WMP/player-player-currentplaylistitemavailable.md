---
title: Evento Player.CurrentPlaylistItemAvailable
description: L'evento CurrentPlaylistItemAvailable si verifica quando la playlist corrente diventa disponibile. | Evento Player.CurrentPlaylistItemAvailable
ms.assetid: 4894e2fc-3464-413f-8abf-8b5e91899946
keywords:
- Evento CurrentPlaylistItemAvailable Windows Media Player
- Evento CurrentPlaylistItemAvailable Windows Media Player , classe Player
- Classe Player Windows Media Player, evento CurrentPlaylistItemAvailable
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4c2543f99d9bc645fa021d7dc5c94f66369b3c3151647dc4d575aab0a32f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338137"
---
# <a name="playercurrentplaylistitemavailable-event"></a>Evento Player.CurrentPlaylistItemAvailable

**L'evento CurrentPlaylistItemAvailable** si verifica quando la playlist corrente diventa disponibile.

## <a name="syntax"></a>Sintassi


```JScript
Player.CurrentPlaylistItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrItemName* 
</dt> <dd>

**Stringa** contenente il nome dell'elemento della playlist corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il nome della playlist corrente può essere usato per recuperare l'oggetto **Playlist** corrispondente usando *PlaylistCollection.* **Metodo getByName.**

Il valore dei parametri dell'evento viene specificato da Windows Media Player ed è accessibile o passato a un metodo in un file di JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

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

[**Oggetto Playlist**](playlist-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





