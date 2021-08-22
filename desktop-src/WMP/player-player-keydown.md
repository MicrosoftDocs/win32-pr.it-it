---
title: Evento Player.KeyDown
description: L'evento KeyDown si verifica quando viene premuto un tasto. | Evento Player.KeyDown
ms.assetid: a34dafca-5db2-4065-bcfe-d66e633b26fb
keywords:
- Evento KeyDown Windows Media Player
- KeyDown event Windows Media Player , Player class
- Classe player Windows Media Player, evento KeyDown
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
ms.openlocfilehash: a067e0125bea6bcabec591d6c1f3ec6fc5a2ee1b0d649a02009690c89d68952e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134774"
---
# <a name="playerkeydown-event"></a>Evento Player.KeyDown

**L'evento KeyDown** si verifica quando viene premuto un tasto.

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

**Numero** (**int**) che specifica quale tasto fisico viene premuto. Per i valori possibili, vedere la sezione Osservazioni.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Numero** (**int**) che specifica un campo di bit con i bit meno significativi corrispondenti al tasto MAIUSC (bit 0), al tasto CTRL (bit 1) e al tasto ALT (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. L'argomento shift indica lo stato di queste chiavi. Alcuni, tutti o nessuno dei bit possono essere impostati, a indicare che alcuni, tutti o nessuno dei tasti vengono premuti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

*L'argomento nKeyCode* specifica una chiave fisica. Le tabelle seguenti illustrano i valori possibili per i tasti principali su una tastiera standard.

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



 

Valori per le chiavi del tastierino numerico.



| Chiave               | Valore  |
|-------------------|--------|
| 0-9               | 96-105 |
| BLOC NUM          | 144    |
| DIVISIONE (/)        | 111    |
| MULTIPLY ( \* )     | 106    |
| SUBTRACT (-)      | 109    |
| ADD (+)           | 107    |
| SEPARATOR (INVIO) | 108    |
| DECIMALE (.)       | 110    |



 

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



 

Il valore dei parametri dell'evento viene specificato da Windows Media Player ed è accessibile o passato a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





