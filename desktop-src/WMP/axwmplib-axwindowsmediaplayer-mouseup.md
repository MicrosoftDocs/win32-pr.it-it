---
title: Evento MouseUp dell'oggetto AxWindowsMediaPlayer
description: L'evento MouseUp si verifica quando l'utente rilascia un pulsante del mouse. | Evento MouseUp dell'oggetto AxWindowsMediaPlayer
ms.assetid: 26bb6e82-d744-4770-b4de-07c9f52b76ec
keywords:
- Evento MouseUp dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- MouseUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2bf9c209b4fa263eb0a6cbcba2a32b0b1c46fa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329444"
---
# <a name="mouseup-event-of-the-axwindowsmediaplayer-object"></a>Evento MouseUp dell'oggetto AxWindowsMediaPlayer

L'evento MouseUp si verifica quando l'utente rilascia un pulsante del mouse.

``` syntax
[C#]
private void player_MouseUpEvent(
  object sender,
  _WMPOCXEvents_MouseUpEvent e
)

[Visual Basic]
Private Sub player_MouseUpEvent(  
  sender As Object,
  e As _WMPOCXEvents_MouseUpEvent
) Handles player.MouseUpEvent
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_MouseUpEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseUpEvent**, che contiene le seguenti proprietà correlate a questo evento.



| Proprietà    | Descrizione                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Npulsante     | System. Int16a bit con bit corrispondente al pulsante sinistro (bit 0), pulsante destro (bit 1) e pulsante centrale (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. Viene impostato solo uno dei bit, che indica il pulsante che ha causato l'evento.<br/>                                                |
| nShiftState | System. Int16a bit con i bit meno significativi che corrispondono al tasto MAIUSC (bit 0), al tasto CTRL (bit 1) e al tasto ALT (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. È possibile impostare some, all o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti.<br/> |
| fX          | System. Int32The: coordinata x del puntatore del mouse rispetto all'angolo superiore sinistro del controllo.<br/>                                                                                                                                                                                                                 |
| fY          | Coordinata y di System. Int32The del puntatore del mouse rispetto all'angolo superiore sinistro del controllo.<br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





