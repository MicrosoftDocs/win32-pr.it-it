---
title: Evento MediaCollectionMediaAdded dell'oggetto AxWindowsMediaPlayer
description: L'evento MediaCollectionMediaAdded si verifica quando un elemento multimediale viene aggiunto alla libreria locale. | Evento MediaCollectionMediaAdded dell'oggetto AxWindowsMediaPlayer
ms.assetid: ba1779f6-a212-44f4-b52a-c88e22aebcce
keywords:
- Evento MediaCollectionMediaAdded dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb48a41970840a45344e2e6fdd578f4e84e23751fd8e337052e66ccd0a058d5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765101"
---
# <a name="mediacollectionmediaadded-event-of-the-axwindowsmediaplayer-object"></a>Evento MediaCollectionMediaAdded dell'oggetto AxWindowsMediaPlayer

L'evento MediaCollectionMediaAdded si verifica quando un elemento multimediale viene aggiunto alla libreria locale.

``` syntax
[C#]
private void player_MediaCollectionMediaAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionMediaAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaAddedEvent
) Handles player.MediaCollectionMediaAdded
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaAddedEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaAddedEvent**, che contiene la proprietà seguente correlata a questo evento.



| Proprietà | Descrizione                                                                                                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------|
| pMedia   | System.ObjectL'elemento multimediale aggiunto alla libreria locale. È possibile eseguire il cast a un'interfaccia IWMPMedia per accedervi.<br/> |



 

## <a name="remarks"></a>Commenti

Questo evento si verifica solo per la libreria locale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11<br/>                                                                                         |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.mediaCollection (VB e C#)**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





