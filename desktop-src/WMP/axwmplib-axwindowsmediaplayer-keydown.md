---
title: Evento KeyDown dell'oggetto AxWindowsMediaPlayer
description: L'evento KeyDown si verifica quando viene premuto un tasto. | Evento KeyDown dell'oggetto AxWindowsMediaPlayer
ms.assetid: e67b9628-6c53-4893-921a-9487ebfc1cd5
keywords:
- Evento KeyDown dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- KeyDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 054736007219021dbc0a4c1c968f61e1bbdb285fa416aae5f3c92c3880fb55de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469721"
---
# <a name="keydown-event-of-the-axwindowsmediaplayer-object"></a>Evento KeyDown dell'oggetto AxWindowsMediaPlayer

L'evento KeyDown si verifica quando viene premuto un tasto.

``` syntax
[C#]
private void player_KeyDownEvent(
  object sender,
  _WMPOCXEvents_KeyDownEvent e
)

[Visual Basic]
Private Sub player_KeyDownEvent(  
  sender As Object, 
  e As _WMPOCXEvents_KeyDownEvent
) Handles player.KeyDownEvent
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyDownEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyDownEvent**, che contiene le proprietà seguenti correlate a questo evento.



| Proprietà    | Descrizione                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nKeyCode    | System.Int16Specifica quale tasto fisico viene premuto. Per i valori possibili, vedere La sezione Osservazioni.<br/>                                                                                                                                                                                                                                                                                    |
| nShiftState | Campo di bit System.Int16A con i bit meno significativi corrispondenti al tasto MAIUSC (bit 0), al tasto CTRL (bit 1) e al tasto ALT (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. L'argomento shift indica lo stato di queste chiavi. È possibile impostare alcuni, tutti o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti.<br/> |



 

## <a name="remarks"></a>Commenti

La **proprietà nKeyCode** specifica una chiave fisica. Le tabelle seguenti illustrano i valori possibili per i tasti principali su una tastiera standard.

Valori per le chiavi principali.



| Chiave                     | Valore   |
|-------------------------|---------|
| A-Z                     | 65-90   |
| 0-9                     | 48-56   |
| F1-F12                  | 112-123 |
| ESC                     | 27      |
| TAB                     | 9       |
| Bloc Maiusc               | 20      |
| MAIUSC (a sinistra o a destra)   | 16      |
| CTRL (sinistra o destra)    | 17      |
| ALT (sinistra o destra)     | 18      |
| SPACE                   | 32      |
| BACKSPACE               | 8       |
| INVIO                   | 13      |
| Windows del logo, a sinistra  | 91      |
| Windows del logo, a destra | 92      |
| Chiave applicazione         | 93      |



 

Valori per i tasti di riempimento dei numeri.



| Chiave               | Valore  |
|-------------------|--------|
| 0-9               | 96-105 |
| BLOC NUM          | 144    |
| DIVIDE (/)        | 111    |
| MULTIPLY ( \* )     | 106    |
| SOTTRAZIONE (-)      | 109    |
| ADD (+)           | 107    |
| SEPARATOR (INVIO) | 108    |
| DECIMAL (.)       | 110    |



 

Valori per i tasti di spostamento.



| Chiave         | Valore |
|-------------|-------|
| INSERT      | 45    |
| DELETE      | 46    |
| HOME        | 36    |
| FINE         | 35    |
| PGSU     | 33    |
| PGGIÙ   | 34    |
| FRECCIA SU    | 38    |
| Freccia GIÙ  | 40    |
| FRECCIA SINISTRA  | 37    |
| FRECCIA DESTRA | 39    |



 

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

 

 





