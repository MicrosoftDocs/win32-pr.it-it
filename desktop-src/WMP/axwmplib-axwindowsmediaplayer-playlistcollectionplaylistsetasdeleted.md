---
title: Evento PlaylistCollectionPlaylistSetAsDeleted dell'oggetto AxWindowsMediaPlayer
description: L'evento PlaylistCollectionPlaylistSetAsDeleted è riservato per un uso futuro.
ms.assetid: 6c0a4d2c-e965-4a88-acd4-2a2a12265e36
keywords:
- Evento PlaylistCollectionPlaylistSetAsDeleted dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistSetAsDeleted Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b11187ffaf6e16612ba7edb573e0b0bc71e9d2abf44ee509db2404026e3ed570
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864580"
---
# <a name="playlistcollectionplaylistsetasdeleted-event-of-the-axwindowsmediaplayer-object"></a>Evento PlaylistCollectionPlaylistSetAsDeleted dell'oggetto AxWindowsMediaPlayer

L'evento PlaylistCollectionPlaylistSetAsDeleted è riservato per un uso futuro.

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistSetAsDeleted(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistSetAsDeleted(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent
) Handles player.PlaylistCollectionPlaylistSetAsDeleted
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ Playlist Di \_ WMPOCXEventsCollectionPlaylistSetAsDeletedEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ \_PlaylistCollectionPlaylistSetAsDeletedEvent di WMPOCXEvents** che contiene le proprietà seguenti correlate a questo evento.



| Proprietà         | Descrizione                                 |
|------------------|---------------------------------------------|
| bstrPlaylistName | **System.String** Non supportato.<br/>  |
| varfIsDeleted    | **System.Boolean** Non supportato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo evento è riservato per un uso futuro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





