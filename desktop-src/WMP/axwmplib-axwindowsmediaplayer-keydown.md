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
ms.openlocfilehash: fc89814063e1a43badd22e658b5f19ece7abb074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331890"
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

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_KeyDownEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyDownEvent**, che contiene le seguenti proprietà correlate a questo evento.



| Proprietà    | Descrizione                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nKeyCode    | System. Int16Specifies in cui viene premuto il tasto fisico. Per i valori possibili, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                                                                                                                    |
| nShiftState | System. Int16a bit con i bit meno significativi che corrispondono al tasto MAIUSC (bit 0), al tasto CTRL (bit 1) e al tasto ALT (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. L'argomento Shift indica lo stato di queste chiavi. È possibile impostare some, all o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti.<br/> |



 

## <a name="remarks"></a>Commenti

La proprietà **nKeyCode** specifica una chiave fisica. Nelle tabelle seguenti vengono illustrati i valori possibili per le chiavi principali in una tastiera standard.

Valori per le chiavi principali.



| Chiave                     | Valore   |
|-------------------------|---------|
| A-Z                     | 65-90   |
| 0-9                     | 48-56   |
| F1-F12                  | 112-123 |
| ESC                     | 27      |
| TAB                     | 9       |
| Bloc Maiusc               | 20      |
| Maiusc (a sinistra o a destra)   | 16      |
| CTRL (a sinistra o a destra)    | 17      |
| ALT (a sinistra o a destra)     | 18      |
| SPACE                   | 32      |
| BACKSPACE               | 8       |
| INVIO                   | 13      |
| Tasto logo Windows, a sinistra  | 91      |
| Tasto logo Windows, a destra | 92      |
| Chiave applicazione         | 93      |



 

Valori per le chiavi del tastierino numerico.



| Chiave               | Valore  |
|-------------------|--------|
| 0-9               | 96-105 |
| BLOC NUM          | 144    |
| Divisione (/)        | 111    |
| MULTIPLY ( \* )     | 106    |
| SOTTRAzione (-)      | 109    |
| AGGIUNGI (+)           | 107    |
| SEPARATOre (invio) | 108    |
| DECIMALE (.)       | 110    |



 

Valori per i tasti di navigazione.



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
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





