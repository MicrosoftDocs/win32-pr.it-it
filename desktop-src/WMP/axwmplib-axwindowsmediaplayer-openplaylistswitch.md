---
title: Evento OpenPlaylistSwitch dell'oggetto AxWindowsMediaPlayer
description: L'evento OpenPlaylistSwitch si verifica quando viene avviata la riproduzione di un titolo su un DVD. | Evento OpenPlaylistSwitch dell'oggetto AxWindowsMediaPlayer
ms.assetid: 0b9c37a3-1349-48bd-8e1a-aba286c82abf
keywords:
- Evento OpenPlaylistSwitch dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d360944b46555be53d5e212561cf906dd33c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325868"
---
# <a name="openplaylistswitch-event-of-the-axwindowsmediaplayer-object"></a>Evento OpenPlaylistSwitch dell'oggetto AxWindowsMediaPlayer

L'evento OpenPlaylistSwitch si verifica quando viene avviata la riproduzione di un titolo su un DVD.

``` syntax
[C#]
private void player_OpenPlaylistSwitch(
  object sender,
  _WMPOCXEvents_OpenPlaylistSwitchEvent e
)

[Visual Basic]
Private Sub player_OpenPlaylistSwitch(
  sender As Object,
  e As _WMPOCXEvents_OpenPlaylistSwitchEvent
) Handles player.OpenPlaylistSwitch
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_OpenPlaylistSwitchEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ OpenPlaylistSwitchEvent**, che contiene la proprietà seguente correlata a questo evento.



| Proprietà  | Descrizione                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------|
| **pItem** | System. ObjectObject che rappresenta il titolo. È possibile eseguire il cast di questo oggetto a un'interfaccia IWMPPlaylist per accedervi.<br/> |



 

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

 

 





