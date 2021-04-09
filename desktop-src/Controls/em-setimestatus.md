---
title: Messaggio EM_SETIMESTATUS (winuser. h)
description: Imposta i flag di stato che determinano il modo in cui un controllo di modifica interagisce con l'IME (Input Method Editor).
ms.assetid: 3de2e8b5-bdd8-4b25-9427-38a11b77a17a
keywords:
- Controlli di Windows Message EM_SETIMESTATUS
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
ms.openlocfilehash: e896c358281b2d4b5012fe13003720e0d008e6a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742010"
---
# <a name="em_setimestatus-message"></a>\_Messaggio SETIMESTATUS em

Imposta i flag di stato che determinano il modo in cui un controllo di modifica interagisce con l'IME (Input Method Editor).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di stato da impostare. Questo parametro può essere il valore seguente.



| Valore                                                                                                                                                                                       | Significato                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**\_COMPOSITIONSTRING EMSIS**</dt> </dl> | Imposta il comportamento per la stringa di composizione di gestione.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dati specifici del tipo di stato. Se *wParam* è **EMSIS \_ COMPOSITIONSTRING**, questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                            | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EIMES_GETCOMPSTRATONCE"></span><span id="eimes_getcompstratonce"></span><dl> <dt>**\_GETCOMPSTRATONCE EIMES**</dt> </dl>                         | Se questo flag è impostato, il controllo di modifica associa il messaggio di [**\_ \_ composizione IME WM**](/windows/desktop/Intl/wm-ime-composition) con *lParam* impostato su cataloghi globali \_ RESULTSTR e restituisce immediatamente la stringa di risultato. Se questo flag non è impostato, il controllo di modifica passa il messaggio di **\_ \_ composizione IME WM** alla routine della finestra predefinita e gestisce la stringa di risultato dal messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) ; questo è il comportamento predefinito del controllo di modifica.<br/> |
| <span id="EIMES_CANCELCOMPSTRINFOCUS"></span><span id="eimes_cancelcompstrinfocus"></span><dl> <dt>**\_CANCELCOMPSTRINFOCUS EIMES**</dt> </dl>             | Se questo flag è impostato, il controllo di modifica annulla la stringa di composizione quando riceve il messaggio di [**\_ SetFocus di WM**](/windows/desktop/inputdev/wm-setfocus) . Se questo flag non è impostato, il controllo di modifica non annulla la stringa di composizione. Questo è il comportamento predefinito del controllo di modifica.<br/>                                                                                                                                                                     |
| <span id="EIMES_COMPLETECOMPSTRKILLFOCUS"></span><span id="eimes_completecompstrkillfocus"></span><dl> <dt>**\_COMPLETECOMPSTRKILLFOCUS EIMES**</dt> </dl> | Se questo flag è impostato, il controllo di modifica completa la stringa di composizione al momento della ricezione del messaggio [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) . Se questo flag non è impostato, il controllo di modifica non completerà la stringa di composizione. Questo è il comportamento predefinito del controllo di modifica.<br/>                                                                                                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore precedente del parametro *lParam* .

## <a name="remarks"></a>Commenti

**Modifica avanzata:** Il **messaggio \_ SETIMESTATUS em** non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETIMESTATUS em**](em-getimestatus.md)
</dt> </dl>

 

