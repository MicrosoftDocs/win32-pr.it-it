---
title: Evento PlaylistCollectionPlaylistSetAsDeleted dell'oggetto AxWindowsMediaPlayer
description: L'evento PlaylistCollectionPlaylistSetAsDeleted è riservato per un utilizzo futuro.
ms.assetid: 6c0a4d2c-e965-4a88-acd4-2a2a12265e36
keywords:
- Evento PlaylistCollectionPlaylistSetAsDeleted dell'oggetto AxWindowsMediaPlayer Media Player Windows
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
ms.openlocfilehash: bf432ede40298abed98cdf0c5b02b0a192f7b3a9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332301"
---
# <a name="playlistcollectionplaylistsetasdeleted-event-of-the-axwindowsmediaplayer-object"></a>Evento PlaylistCollectionPlaylistSetAsDeleted dell'oggetto AxWindowsMediaPlayer

L'evento PlaylistCollectionPlaylistSetAsDeleted è riservato per un utilizzo futuro.

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

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_PlaylistCollectionPlaylistSetAsDeletedEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistSetAsDeletedEvent**, che contiene le seguenti proprietà correlate a questo evento.



| Proprietà         | Descrizione                                 |
|------------------|---------------------------------------------|
| bstrPlaylistName | **System. String** Non supportato.<br/>  |
| varfIsDeleted    | **System. Boolean** Non supportato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo evento è riservato per un utilizzo futuro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





