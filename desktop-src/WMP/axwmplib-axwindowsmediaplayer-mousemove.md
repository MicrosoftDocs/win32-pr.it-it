---
title: Evento MouseMove dell'oggetto AxWindowsMediaPlayer
description: L'evento MouseMove si verifica quando il puntatore del mouse viene spostato. | Evento MouseMove dell'oggetto AxWindowsMediaPlayer
ms.assetid: abf20c86-3bae-4677-8901-0af030a53286
keywords:
- Evento MouseMove dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- MouseMove Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 608dea9e69135f0f473b9dfba175dc6e9353afe0bc7e23368c144e2a0ea1a7f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902461"
---
# <a name="mousemove-event-of-the-axwindowsmediaplayer-object"></a>Evento MouseMove dell'oggetto AxWindowsMediaPlayer

L'evento MouseMove si verifica quando il puntatore del mouse viene spostato.

``` syntax
[C#]
private void player_MouseMoveEvent(
  object sender,
  _WMPOCXEvents_MouseMoveEvent e
)

[Visual Basic]
Private Sub player_MouseMoveEvent(
  sender As Object,
  e As _WMPOCXEvents_MouseMoveEvent
) Handles player.MouseMoveEvent
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_MouseMoveEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseMoveEvent**, che contiene le proprietà seguenti correlate a questo evento.



| Proprietà    | Descrizione                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nButton     | Campo di bit System.Int16A con bit corrispondenti al pulsante sinistro (bit 0), al pulsante destro (bit 1) e al pulsante centrale (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. Viene impostato solo uno dei bit, che indica il pulsante che ha causato l'evento.<br/>                                                |
| nShiftState | Campo di bit System.Int16A con i bit meno significativi corrispondenti al tasto MAIUSC (bit 0), al tasto CTRL (bit 1) e al tasto ALT (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. Alcuni, tutti o nessuno dei bit possono essere impostati, a indicare che alcuni, tutti o nessuno dei tasti vengono premuti.<br/> |
| Fx          | System.Int32 Coordinata x del puntatore del mouse rispetto all'angolo superiore sinistro del controllo.<br/>                                                                                                                                                                                                                 |
| Fy          | System.Int32 Coordinata y del puntatore del mouse rispetto all'angolo superiore sinistro del controllo.<br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





