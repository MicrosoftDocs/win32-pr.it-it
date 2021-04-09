---
title: Messaggio EM_GETIMESTATUS (winuser. h)
description: Ottiene un set di flag di stato che indicano il modo in cui il controllo di modifica interagisce con l'IME (Input Method Editor).
ms.assetid: 56705aed-afab-4f4d-9e0b-dc533b516a15
keywords:
- Controlli di Windows Message EM_GETIMESTATUS
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
ms.openlocfilehash: 2a9b449053972db8101db7f5c01d1a03611cae67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120731"
---
# <a name="em_getimestatus-message"></a>\_Messaggio GETIMESTATUS em

Ottiene un set di flag di stato che indicano il modo in cui il controllo di modifica interagisce con l'IME (Input Method Editor).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di stato da recuperare. Questo parametro può essere il valore seguente.



| Valore                                                                                                                                                                                       | Significato                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**\_COMPOSITIONSTRING EMSIS**</dt> </dl> | Imposta il comportamento per la gestione della stringa di composizione.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Dati specifici del tipo di stato da recuperare. Con il valore **EMSIS \_ COMPOSITIONSTRING** per *status*, questo valore restituito corrisponde a uno o più dei valori seguenti.



| Codice restituito                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_GETCOMPSTRATONCE EIMES**</dt> </dl>         | Se questo flag è impostato, il controllo di modifica associa il messaggio di [**\_ \_ composizione IME WM**](/windows/desktop/Intl/wm-ime-composition) a *fFlags* impostato su GC \_ RESULTSTR e restituisce immediatamente la stringa di risultato. Se questo flag non è impostato, il controllo di modifica passa il messaggio di **\_ \_ composizione IME WM** alla routine della finestra predefinita ed elabora la stringa di risultato dal messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) ; questo è il comportamento predefinito del controllo di modifica.<br/> |
| <dl> <dt>**\_CANCELCOMPSTRINFOCUS EIMES**</dt> </dl>     | Se questo flag è impostato, il controllo di modifica annulla la stringa di composizione quando riceve il messaggio di [**\_ SetFocus di WM**](/windows/desktop/inputdev/wm-setfocus) . Se questo flag non è impostato, il controllo di modifica non annulla la stringa di composizione. Questo è il comportamento predefinito del controllo di modifica.<br/>                                                                                                                                                                       |
| <dl> <dt>**\_COMPLETECOMPSTRKILLFOCUS EIMES**</dt> </dl> | Se questo flag è impostato, il controllo di modifica completa la stringa di composizione al momento della ricezione del messaggio [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) . Se questo flag non è impostato, il controllo di modifica non completerà la stringa di composizione. Questo è il comportamento predefinito del controllo di modifica.<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Commenti

**Modifica avanzata:** Il **messaggio \_ GETIMESTATUS em** non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETIMESTATUS em**](em-setimestatus.md)
</dt> </dl>

 

