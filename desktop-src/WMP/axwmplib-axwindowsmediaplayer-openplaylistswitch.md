---
title: Evento OpenPlaylistSwitch dell'oggetto AxWindowsMediaPlayer
description: L'evento OpenPlaylistSwitch si verifica quando inizia la riproduzione di un titolo in un DVD. | Evento OpenPlaylistSwitch dell'oggetto AxWindowsMediaPlayer
ms.assetid: 0b9c37a3-1349-48bd-8e1a-aba286c82abf
keywords:
- Evento OpenPlaylistSwitch dell'oggetto AxWindowsMediaPlayer Windows Media Player
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
ms.openlocfilehash: c57341488c385b159ce294626a79b7e22287bff83864f7273b0f4432c1db95ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764701"
---
# <a name="openplaylistswitch-event-of-the-axwindowsmediaplayer-object"></a>Evento OpenPlaylistSwitch dell'oggetto AxWindowsMediaPlayer

L'evento OpenPlaylistSwitch si verifica quando inizia la riproduzione di un titolo in un DVD.

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

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ WMPOCXEvents \_ OpenPlaylistSwitchEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ OpenPlaylistSwitchEvent**, che contiene la proprietà seguente correlata a questo evento.



| Proprietà  | Descrizione                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------|
| **pItem** | Oggetto System.ObjectObject che rappresenta il titolo. È possibile eseguire il cast a un'interfaccia IWMPPlaylist per accedervi.<br/> |



 

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

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





