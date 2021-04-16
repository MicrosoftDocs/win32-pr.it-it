---
title: Messaggio di EM_SETFONTSIZE (RichEdit. h)
description: Imposta la dimensione del carattere per il testo selezionato in un controllo Rich Edit.
ms.assetid: 18d91370-12c0-4e5f-a0e9-ffde02abc966
keywords:
- Controlli di Windows Message EM_SETFONTSIZE
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
ms.openlocfilehash: 8eb75276acbb86cbd452a8ad97698f1cd7382bd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476829"
---
# <a name="em_setfontsize-message"></a>\_Messaggio DIFONTSIZE em

Imposta la dimensione del carattere per il testo selezionato in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Modifica le dimensioni in punti del testo selezionato. Il risultato verrà arrotondato in base ai valori indicati nella tabella seguente. Questo parametro deve essere compreso nell'intervallo da-1637 a 1638. Le dimensioni del carattere risultante saranno comprese nell'intervallo da 1 a 1638.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se non si è verificato alcun errore, il valore restituito è **true**.

Se si è verificato un errore, il valore restituito è **false**.

## <a name="remarks"></a>Commenti

È possibile ottenere facilmente le dimensioni del carattere inviando il messaggio [**\_ GETCHARFORMAT em**](em-getcharformat.md) .

Rich Edit aggiunge innanzitutto *wParam* alla dimensione corrente del carattere e quindi usa le dimensioni risultanti e la tabella seguente per determinare il valore di arrotondamento.



| Fuori banda    | Valore di arrotondamento |
|---------|----------------|
| <= 12 | 1              |
| 28      | 2              |
| 36      | 0              |
| 48      | 0              |
| 72      | 0              |
| 80      | 0              |
| > 80 | 10             |



 

Se la dimensione del carattere risultante non è divisibile in modo uniforme per il valore di arrotondamento, le dimensioni del carattere vengono arrotondate a un numero equamente divisibile per il valore di arrotondamento. Quindi, se la dimensione del carattere è minore o uguale a 12, il valore di arrotondamento sarà 1. Analogamente, se la dimensione del carattere è minore o uguale a 28, il valore di arrotondamento è 2. Per i valori maggiori di 28, le dimensioni del carattere vengono arrotondate alla banda successiva. Quindi, la dimensione del carattere passa a 36, 48, 72, 80. Dopo 80, l'arrotondamento viene eseguito in incrementi di dieci punti.

Le dimensioni del carattere vengono arrotondate per eccesso o per difetto a seconda del segno di *wParam*. Se *wParam* è positivo, l'arrotondamento è sempre attivo. In caso contrario, l'arrotondamento è sempre inattivo. Quindi, se la dimensione corrente del carattere è 10 e *wParam* è 3, le dimensioni del carattere risultante saranno 14 (10 + 3 = 13, che non è divisibile per 2, quindi la dimensione viene arrotondata a 14). Viceversa, se le dimensioni del carattere correnti sono 14 e *wParam* è-3, la dimensione del carattere risultante sarà 10 (14-3 = 11, che non è divisibile per 2, quindi la dimensione viene arrotondata a 10).

La modifica viene applicata a ogni parte della selezione. Quindi, se il testo è 10pt e alcuni 20pt, dopo una chiamata con *wParam* impostato su 1, le dimensioni del carattere diventano rispettivamente 11pt e 22pt.

Nella tabella seguente sono illustrati altri esempi.



| Dimensioni del carattere originale | *wParam* | Dimensioni del carattere risultanti |
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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Componente ridistribuibile<br/>          | Modifica avanzata 3,0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_GETCHARFORMAT em**](em-getcharformat.md)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sui controlli Rich Edit](about-rich-edit-controls.md)
</dt> </dl>

 

 





