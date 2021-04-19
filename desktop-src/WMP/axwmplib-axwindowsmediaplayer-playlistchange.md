---
title: Evento PlaylistChange dell'oggetto AxWindowsMediaPlayer
description: L'evento PlaylistChange si verifica quando viene modificata una playlist. | Evento PlaylistChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: e4166d81-a205-401a-94c4-a1619e764647
keywords:
- Evento PlaylistChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- PlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9989b303d8e9077c158fd844c93431100205d9f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332310"
---
# <a name="playlistchange-event-of-the-axwindowsmediaplayer-object"></a>Evento PlaylistChange dell'oggetto AxWindowsMediaPlayer

L'evento PlaylistChange si verifica quando viene modificata una playlist.

``` syntax
[C#]
private void player_PlaylistChange(
  object sender,
  _WMPOCXEvents_PlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_PlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_PlaylistChangeEvent
) Handles player.PlaylistChange
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_PlaylistChangeEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistChangeEvent**, che contiene le seguenti proprietà correlate a questo evento.



| Proprietà     | Descrizione                                                                                                                   |
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| **playlist** | Oggetto System. ObjectThe che è stato modificato. È possibile eseguire il cast di questo oggetto a un'interfaccia IWMPPlaylist per accedervi.<br/>                |
| **change**   | Valore di enumerazione WMPLib. WMPPlaylistChangeEventTypeAn che indica il tipo di modifica apportata alla playlist.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





