---
title: Evento Player. CurrentPlaylistItemAvailable
description: L'evento CurrentPlaylistItemAvailable si verifica quando la playlist corrente diventa disponibile. | Evento Player. CurrentPlaylistItemAvailable
ms.assetid: 4894e2fc-3464-413f-8abf-8b5e91899946
keywords:
- Media Player di Windows Event CurrentPlaylistItemAvailable
- Windows Event CurrentPlaylistItemAvailable Media Player, classe Player
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
ms.openlocfilehash: 2fe5809e50d572cfb8eb7a36220d083ec18a0a76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328874"
---
# <a name="playercurrentplaylistitemavailable-event"></a>Evento Player. CurrentPlaylistItemAvailable

L'evento **CurrentPlaylistItemAvailable** si verifica quando la playlist corrente diventa disponibile.

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

**Stringa** che contiene il nome dell'elemento della playlist corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il nome della playlist corrente può essere usato per recuperare l'oggetto **playlist** corrispondente usando *PlaylistCollection*. metodo **GetByName** .

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

[**Oggetto playlist**](playlist-object.md)
</dt> <dt>

[**PlaylistCollection. getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





