---
title: Evento di buffering dell'oggetto AxWindowsMediaPlayer
description: L'evento di buffering si verifica quando il controllo Media Player Windows inizia o termina il buffering o il download. | Evento di buffering dell'oggetto AxWindowsMediaPlayer
ms.assetid: ad152c4d-1c91-4da1-bec0-46f89f3b8c79
keywords:
- Evento di buffering dell'oggetto AxWindowsMediaPlayer Windows Media Player
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
ms.openlocfilehash: af595443d78a311510df6a7e06b2e716da22ecae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323929"
---
# <a name="buffering-event-of-the-axwindowsmediaplayer-object"></a>Evento di buffering dell'oggetto AxWindowsMediaPlayer

L'evento di buffering si verifica quando il controllo Media Player Windows inizia o termina il buffering o il download.

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

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_BufferingEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ BufferingEvent**, che contiene la proprietà seguente correlata a questo evento.



| Proprietà | Descrizione                                                                                                                                                         |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inizia    | System. BooleanSpecifies se la memorizzazione nel buffer è iniziata o terminata. Il valore true indica che è iniziata. il valore false indica che è terminato.<br/> |



 

## <a name="remarks"></a>Commenti

Utilizzare questo evento per determinare quando viene avviata o arrestata la memorizzazione nel buffer o il download. È possibile usare lo stesso blocco di eventi per entrambi i casi e *IWMPNetwork* di test. **bufferingProgress** e *IWMPNetwork*. **downloadProgress** per determinare se Windows Media Player sta attualmente memorizzando nel buffer o scaricando il contenuto.

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

[**IWMPNetwork. bufferingProgress (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. downloadProgress (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)
</dt> </dl>

 

 





