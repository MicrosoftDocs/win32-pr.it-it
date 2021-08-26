---
title: EM_SETFONTSIZE messaggio (Richedit.h)
description: Imposta le dimensioni del carattere per il testo selezionato in un controllo Rich Edit.
ms.assetid: 18d91370-12c0-4e5f-a0e9-ffde02abc966
keywords:
- EM_SETFONTSIZE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- EM_SETFONTSIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e646d58626a034f4764d6b9636e5b4b3eedba5befd7986eade9979c1f4a4fd5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048461"
---
# <a name="em_setfontsize-message"></a>Messaggio EM \_ SETFONTSIZE

Imposta le dimensioni del carattere per il testo selezionato in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Modificare le dimensioni in punti del testo selezionato. Il risultato verrà arrotondato in base ai valori illustrati nella tabella seguente. Questo parametro deve essere compreso nell'intervallo compreso tra -1637 e 1638. Le dimensioni del carattere risultanti saranno nell'intervallo compreso tra 1 e 1638.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se non si è verificato alcun errore, il valore restituito è **TRUE.**

Se si è verificato un errore, il valore restituito è **FALSE.**

## <a name="remarks"></a>Commenti

È possibile ottenere facilmente le dimensioni del carattere inviando il [**messaggio EM \_ GETCHARFORMAT.**](em-getcharformat.md)

Rich Edit aggiunge *prima wParam* alla dimensione del carattere corrente e quindi usa le dimensioni risultanti e la tabella seguente per determinare il valore di arrotondamento.



| Band    | Valore di arrotondamento |
|---------|----------------|
| <=12 | 1              |
| 28      | 2              |
| 36      | 0              |
| 48      | 0              |
| 72      | 0              |
| 80      | 0              |
| > 80 | 10             |



 

Se la dimensione del carattere risultante non è divisibile in modo uniforme per il valore di arrotondamento, la dimensione del carattere viene quindi arrotondata a un numero uniformemente divisibile per il valore di arrotondamento. Pertanto, se la dimensione del carattere è minore o uguale a 12, il valore di arrotondamento sarà 1. Analogamente, se la dimensione del carattere è minore o uguale a 28, il valore di arrotondamento è 2. Per i valori maggiori di 28, le dimensioni dei caratteri vengono arrotondate alla banda successiva. La dimensione del carattere passa quindi a 36, 48, 72, 80. Dopo 80, l'arrotondamento viene eseguito con incrementi di dieci punti.

La dimensione del carattere viene arrotondata per e per es. Se *wParam è* positivo, l'arrotondamento è sempre per es. In caso contrario, l'arrotondamento è sempre verso il basso. Pertanto, se la dimensione del carattere corrente è 10 e *wParam* è 3, la dimensione del carattere risultante sarà 14 (10 + 3 = 13, che non è divisibile per 2, quindi la dimensione viene arrotondata per es. 14). Al contrario, se la dimensione del carattere corrente è 14 e *wParam* è -3, la dimensione del carattere risultante sarà 10 (14 - 3 = 11, che non è divisibile per 2, quindi la dimensione viene arrotondata per esere a 10).

La modifica viene applicata a ogni parte della selezione. Pertanto, se una parte del testo è 10pt e circa 20 pt, dopo una chiamata con *wParam* impostato su 1, le dimensioni del carattere diventano rispettivamente 11 pt e 22pt.

Nella tabella seguente sono illustrati altri esempi.



| Dimensione del carattere originale | *wParam* | Dimensioni del carattere risultanti |
|--------------------|----------|---------------------|
| 7                  | 1        | 8                   |
| 7                  | 3        | 10                  |
| 10                 | 3        | 14                  |
| 14                 | -3       | 10                  |
| 28                 | 1        | 36                  |
| 28                 | 3        | 36                  |
| 80                 | 1        | 90                  |
| 80                 | -1       | 72                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Componente ridistribuibile<br/>          | Rich Edit 3.0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ GETCHARFORMAT**](em-getcharformat.md)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sui controlli Rich Edit](about-rich-edit-controls.md)
</dt> </dl>

 

 





