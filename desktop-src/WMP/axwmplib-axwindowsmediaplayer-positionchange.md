---
title: Evento PositionChange dell'oggetto AxWindowsMediaPlayer
description: L'evento PositionChange si verifica quando la posizione di riproduzione corrente all'interno dell'elemento multimediale è stata modificata.
ms.assetid: 92d469b9-813a-4148-be68-0fcef2e41491
keywords:
- Evento PositionChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
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
ms.openlocfilehash: 552b748121668e71ee4d2ffb54feed441620a1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326226"
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

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_PositionChangeEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ PositionChangeEvent**, che contiene le seguenti proprietà correlate a questo evento.



| Proprietà    | Descrizione                                         |
|-------------|-----------------------------------------------------|
| oldPosition | System. DoubleSpecifies la posizione precedente.<br/> |
| newPosition | System. DoubleSpecifies la nuova posizione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo evento non viene generato periodicamente durante la riproduzione. Si verifica solo quando un elemento modifica attivamente la posizione corrente dell'elemento multimediale in riproduzione, ad esempio quando l'utente sposta l'handle di ricerca o quando viene eseguito il codice che specifica un valore per IWMPControls. **currentPosition**.

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

[**IWMPControls. currentPosition (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





