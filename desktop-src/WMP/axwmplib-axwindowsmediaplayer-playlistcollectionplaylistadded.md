---
title: Evento PlaylistCollectionPlaylistAdded dell'oggetto AxWindowsMediaPlayer
description: L'evento PlaylistCollectionPlaylistAdded si verifica quando viene aggiunta una playlist alla raccolta di playlist. | Evento PlaylistCollectionPlaylistAdded dell'oggetto AxWindowsMediaPlayer
ms.assetid: 13d3bc86-6655-4536-a58f-327eabb2b8f9
keywords:
- Evento PlaylistCollectionPlaylistAdded dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5223d5864aa8be9019b2219ef09917a1c63cf16d87a48aef9543246d5197a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581826"
---
# <a name="playlistcollectionplaylistadded-event-of-the-axwindowsmediaplayer-object"></a>Evento PlaylistCollectionPlaylistAdded dell'oggetto AxWindowsMediaPlayer

L'evento PlaylistCollectionPlaylistAdded si verifica quando viene aggiunta una playlist alla raccolta di playlist.

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistAdded(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistAdded(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent
) Handles player.PlaylistCollectionPlaylistAdded
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ Playlist di \_ WMPOCXEventsCollectionPlaylistAddedEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ \_PlaylistCollectionPlaylistAddedEvent di WMPOCXEvents** che contiene la proprietà seguente correlata a questo evento.



| Proprietà             | Descrizione                                                                |
|----------------------|----------------------------------------------------------------------------|
| **bstrPlaylistName** | System.StringSpecifica il nome della playlist aggiunta.<br/> |



 

## <a name="remarks"></a>Commenti

Il nome della playlist aggiunta può essere usato per recuperare la playlist corrispondente usando IWMPPlaylistCollection. **Metodo getByName.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.getByName (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





