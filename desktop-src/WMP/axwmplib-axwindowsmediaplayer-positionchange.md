---
title: Evento PositionChange dell'oggetto AxWindowsMediaPlayer
description: L'evento PositionChange si verifica quando la posizione di riproduzione corrente all'interno dell'elemento multimediale è stata modificata.
ms.assetid: 92d469b9-813a-4148-be68-0fcef2e41491
keywords:
- Evento PositionChange dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- PositionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 269d83c92687b5debda8b70fb4d6710b55eebd5476153759ebad36e5d17657d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764681"
---
# <a name="positionchange-event-of-the-axwindowsmediaplayer-object"></a>Evento PositionChange dell'oggetto AxWindowsMediaPlayer

L'evento PositionChange si verifica quando la posizione di riproduzione corrente all'interno dell'elemento multimediale è stata modificata.

``` syntax
[C#]
private void player_PositionChange(
  object sender,
  _WMPOCXEvents_PositionChangeEvent e
)

[Visual Basic]
Private Sub player_PositionChange(  
  sender As Object,
  e As _WMPOCXEvents_PositionChangeEvent
) Handles player.PositionChange
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ WMPOCXEvents \_ PositionChangeEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ \_PositionChangeEvent WMPOCXEvents**, che contiene le proprietà seguenti correlate a questo evento.



| Proprietà    | Descrizione                                         |
|-------------|-----------------------------------------------------|
| oldPosition | System.DoubleSpecifica la posizione precedente.<br/> |
| newPosition | System.DoubleSpecifica la nuova posizione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo evento non viene generato regolarmente durante la riproduzione. Si verifica solo quando un elemento cambia attivamente la posizione corrente dell'elemento multimediale in riproduzione, ad esempio quando l'utente sposta l'handle di ricerca o quando viene eseguito il codice che specifica un valore per IWMPControls. **currentPosition**.

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

[**IWMPControls.currentPosition (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





