---
title: EM_GETIMESTATUS messaggio (Winuser.h)
description: Ottiene un set di flag di stato che indicano come il controllo di modifica interagisce con Input Method Editor (IME).
ms.assetid: 56705aed-afab-4f4d-9e0b-dc533b516a15
keywords:
- EM_GETIMESTATUS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01a8251a62aa9cf48bcc6476af27e4c3a5dbbb82dd0ce76ca21ae094225a3e46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048991"
---
# <a name="em_getimestatus-message"></a>Messaggio \_ EM GETIMESTATUS

Ottiene un set di flag di stato che indicano come il controllo di modifica interagisce con Input Method Editor (IME).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di stato da recuperare. Questo parametro può essere il valore seguente.



| Valore                                                                                                                                                                                       | Significato                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**EMSIS \_ COMPOSITIONSTRING**</dt> </dl> | Imposta il comportamento per la gestione della stringa di composizione.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Dati specifici del tipo di stato da recuperare. Con il **valore EMSIS \_ COMPOSITIONSTRING** per *status*, questo valore restituito è uno o più dei valori seguenti.



| Codice restituito                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**EIMES \_ GETCOMPSTRATONCE**</dt> </dl>         | Se questo flag è impostato, il controllo di modifica esegue l'hook del messaggio [**WM \_ IME \_ COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) con *fFlags* impostato su GCS RESULTSTR e restituisce immediatamente la \_ stringa di risultato. Se questo flag non è impostato, il controllo di modifica passa il messaggio **WM \_ IME \_ COMPOSITION** alla routine della finestra predefinita ed elabora la stringa di risultato dal messaggio [**WM \_ CHAR.**](/windows/desktop/inputdev/wm-char) Questo è il comportamento predefinito del controllo di modifica.<br/> |
| <dl> <dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt> </dl>     | Se questo flag è impostato, il controllo di modifica annulla la stringa di composizione quando riceve il [**messaggio WM \_ SETFOCUS.**](/windows/desktop/inputdev/wm-setfocus) Se questo flag non è impostato, il controllo di modifica non annulla la stringa di composizione. questo è il comportamento predefinito del controllo di modifica.<br/>                                                                                                                                                                       |
| <dl> <dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt> </dl> | Se questo flag è impostato, il controllo di modifica completa la stringa di composizione alla ricezione del [**messaggio WM \_ KILLFOCUS.**](/windows/desktop/inputdev/wm-killfocus) Se questo flag non è impostato, il controllo di modifica non completa la stringa di composizione. questo è il comportamento predefinito del controllo di modifica.<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Commenti

**Rich Edit:** Il **messaggio EM \_ GETIMESTATUS** non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ SETIMESTATUS**](em-setimestatus.md)
</dt> </dl>

 

