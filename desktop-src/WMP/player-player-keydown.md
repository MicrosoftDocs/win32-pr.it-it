---
title: Evento Player. KeyDown
description: L'evento KeyDown si verifica quando viene premuto un tasto. | Evento Player. KeyDown
ms.assetid: a34dafca-5db2-4065-bcfe-d66e633b26fb
keywords:
- Media Player di Windows evento KeyDown
- KeyDown Event Windows Media Player, classe Player
- Classe Player Windows Media Player, evento KeyDown
topic_type:
- apiref
api_name:
- Player.KeyDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 226430421977a58eca02b7a42cf0349f2a5ff520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331859"
---
# <a name="playerkeydown-event"></a>Evento Player. KeyDown

L'evento **KeyDown** si verifica quando viene premuto un tasto.

## <a name="syntax"></a>Sintassi


```JScript
Player.KeyDown(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nKeyCode* 
</dt> <dd>

**Numero** (**int**) che specifica quale tasto fisico è premuto. Per i valori possibili, vedere la sezione Osservazioni.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Number** (**int**) che specifica un bit con i bit meno significativi che corrispondono al tasto MAIUSC (bit 0), il tasto Ctrl (bit 1) e il tasto Alt (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. L'argomento Shift indica lo stato di queste chiavi. È possibile impostare some, all o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

L'argomento *nKeyCode* specifica una chiave fisica. Nelle tabelle seguenti vengono illustrati i valori possibili per le chiavi principali in una tastiera standard.

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



 

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





