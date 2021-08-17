---
title: EM_SETIMESTATUS messaggio (Winuser.h)
description: Imposta i flag di stato che determinano il modo in cui un controllo di modifica interagisce con Input Method Editor (IME).
ms.assetid: 3de2e8b5-bdd8-4b25-9427-38a11b77a17a
keywords:
- EM_SETIMESTATUS controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5a3e5413c577fcecd89ebb27bc61e5fff31f7e71b3ec7e6da67523d6ee9392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412398"
---
# <a name="em_setimestatus-message"></a>Messaggio EM \_ SETIMESTATUS

Imposta i flag di stato che determinano il modo in cui un controllo di modifica interagisce con Input Method Editor (IME).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di stato da impostare. Questo parametro può essere il valore seguente.



| Valore                                                                                                                                                                                       | Significato                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**EMSIS \_ COMPOSITIONSTRING**</dt> </dl> | Imposta il comportamento per la stringa di composizione di gestione.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dati specifici del tipo di stato. Se *wParam* è **EMSIS \_ COMPOSITIONSTRING,** questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                            | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EIMES_GETCOMPSTRATONCE"></span><span id="eimes_getcompstratonce"></span><dl> <dt>**EIMES \_ GETCOMPSTRATONCE**</dt> </dl>                         | Se questo flag è impostato, il controllo di modifica esegue l'hook del messaggio [**WM \_ IME \_ COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) con *lParam* impostato su GCS RESULTSTR e restituisce immediatamente \_ la stringa di risultato. Se questo flag non è impostato, il controllo di modifica passa il messaggio **WM \_ IME \_ COMPOSITION** alla routine della finestra predefinita e gestisce la stringa di risultato del messaggio [**WM \_ CHAR.**](/windows/desktop/inputdev/wm-char) Questo è il comportamento predefinito del controllo di modifica.<br/> |
| <span id="EIMES_CANCELCOMPSTRINFOCUS"></span><span id="eimes_cancelcompstrinfocus"></span><dl> <dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt> </dl>             | Se questo flag è impostato, il controllo di modifica annulla la stringa di composizione quando riceve il [**messaggio WM \_ SETFOCUS.**](/windows/desktop/inputdev/wm-setfocus) Se questo flag non è impostato, il controllo di modifica non annulla la stringa di composizione. Questo è il comportamento predefinito del controllo di modifica.<br/>                                                                                                                                                                     |
| <span id="EIMES_COMPLETECOMPSTRKILLFOCUS"></span><span id="eimes_completecompstrkillfocus"></span><dl> <dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt> </dl> | Se questo flag è impostato, il controllo di modifica completa la stringa di composizione alla ricezione del [**messaggio \_ KILLFOCUS WM.**](/windows/desktop/inputdev/wm-killfocus) Se questo flag non è impostato, il controllo di modifica non completa la stringa di composizione. Questo è il comportamento predefinito del controllo di modifica.<br/>                                                                                                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore precedente del *parametro lParam.*

## <a name="remarks"></a>Commenti

**Rich Edit:** Il **messaggio EM \_ SETIMESTATUS** non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETIMESTATUS**](em-getimestatus.md)
</dt> </dl>

 

