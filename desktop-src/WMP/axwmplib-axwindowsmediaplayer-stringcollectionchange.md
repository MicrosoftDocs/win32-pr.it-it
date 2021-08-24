---
title: Evento StringCollectionChange dell'oggetto AxWindowsMediaPlayer
description: L'evento StringCollectionChange si verifica quando viene modificata una raccolta di stringhe. | Evento StringCollectionChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: 21b66882-bff9-4482-b56c-32c9df0bc02f
keywords:
- Evento StringCollectionChange dell'oggetto AxWindowsMediaPlayer Windows Media Player
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
ms.openlocfilehash: 0ceeba7942be4180d02a44ff19d63c10f9bc9df0bba745fdf69bcf10e97c3052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764660"
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

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ WMPOCXEvents \_ StringCollectionChangeEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ StringCollectionChangeEvent**, che contiene le proprietà seguenti correlate a questo evento.



| Proprietà              | Descrizione                                                                                                                           |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| pdispStringCollection | System.Object Elemento della raccolta di stringhe modificato. È possibile eseguire il cast a un'interfaccia IWMPStringCollection per accedervi.<br/> |
| lCollectionIndex      | System.Int32 Indice dell'elemento della raccolta di stringhe modificato.<br/>                                                          |
| change (modifica)                | Valore di enumerazione WMPLib.WMPStringCollectionChangeEventTypeAn che indica il tipo di modifica che si è verificata.<br/>                 |



 

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

[**Interfaccia IWMPStringCollection (VB e C#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**WMPStringCollectionChangeEventType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpstringcollectionchangeeventtype)
</dt> </dl>

 

 





