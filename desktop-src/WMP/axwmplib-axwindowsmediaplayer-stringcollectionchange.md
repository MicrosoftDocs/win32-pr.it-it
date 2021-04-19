---
title: Evento StringCollectionChange dell'oggetto AxWindowsMediaPlayer
description: L'evento StringCollectionChange si verifica quando viene modificata una raccolta di stringhe. | Evento StringCollectionChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: 21b66882-bff9-4482-b56c-32c9df0bc02f
keywords:
- Evento StringCollectionChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- StringCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5182352f7f18727a1c11e9a0ef49e8141000d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324105"
---
# <a name="stringcollectionchange-event-of-the-axwindowsmediaplayer-object"></a>Evento StringCollectionChange dell'oggetto AxWindowsMediaPlayer

L'evento StringCollectionChange si verifica quando viene modificata una raccolta di stringhe.

``` syntax
[C#]
private void player_StringCollectionChange(
  object sender,
  _WMPOCXEvents_StringCollectionChangeEvent e
)

[Visual Basic]
Private Sub player_StringCollectionChange(
  sender As Object,
  e As _WMPOCXEvents_StringCollectionChangeEvent
) Handles player.StringCollectionChange
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_StringCollectionChangeEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ StringCollectionChangeEvent**, che contiene le seguenti proprietà correlate a questo evento.



| Proprietà              | Descrizione                                                                                                                           |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| pdispStringCollection | Elemento della raccolta di stringhe System. ObjectThe modificato. È possibile eseguire il cast di questo oggetto a un'interfaccia IWMPStringCollection per accedervi.<br/> |
| lCollectionIndex      | Indice System. Int32The dell'elemento della raccolta di stringhe modificato.<br/>                                                          |
| change (modifica)                | Valore di enumerazione WMPLib. WMPStringCollectionChangeEventTypeAn che indica il tipo di modifica che si è verificato.<br/>                 |



 

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

[**Interfaccia IWMPStringCollection (VB e C#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**WMPStringCollectionChangeEventType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpstringcollectionchangeeventtype)
</dt> </dl>

 

 





