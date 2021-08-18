---
title: Evento di memorizzazione nel buffer dell'oggetto AxWindowsMediaPlayer
description: L'evento Buffering si verifica quando il controllo Windows Media Player inizia o termina il buffering o il download. | Evento di memorizzazione nel buffer dell'oggetto AxWindowsMediaPlayer
ms.assetid: ad152c4d-1c91-4da1-bec0-46f89f3b8c79
keywords:
- Evento di memorizzazione nel buffer dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- Buffering Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30cca5d7ebe91859162bd729cc32cc03f36f9e3c59ba4474d41311befcce1d21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765251"
---
# <a name="buffering-event-of-the-axwindowsmediaplayer-object"></a>Evento di memorizzazione nel buffer dell'oggetto AxWindowsMediaPlayer

L'evento Buffering si verifica quando il controllo Windows Media Player inizia o termina il buffering o il download.

``` syntax
[C#]
private void player_Buffering(
  object sender,
  _WMPOCXEvents_BufferingEvent e
)

[Visual Basic]
Private Sub player_Buffering(
  sender As Object,
  e As _WMPOCXEvents_BufferingEvent
) Handles player.Buffering
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ WMPOCXEvents \_ BufferingEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ BufferingEvent**, che contiene la proprietà seguente correlata a questo evento.



| Proprietà | Descrizione                                                                                                                                                         |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inizia    | System.BooleanSpecifica se la memorizzazione nel buffer è iniziata o terminata. Il valore true indica che è iniziata. Il valore false indica che è stato terminato.<br/> |



 

## <a name="remarks"></a>Commenti

Usare questo evento per determinare quando il buffering o il download viene avviato o arrestato. È possibile usare lo stesso blocco di eventi per entrambi i casi e testare *IWMPNetwork*. **bufferingProgress** e *IWMPNetwork*. **downloadProgress** per determinare se Windows Media Player sta attualmente memorizzata nel buffer o scaricando il contenuto.

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

[**IWMPNetwork.bufferingProgress (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.downloadProgress (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)
</dt> </dl>

 

 





