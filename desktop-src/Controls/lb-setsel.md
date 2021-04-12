---
title: Messaggio LB_SETSEL (winuser. h)
description: Seleziona un elemento in una casella di riepilogo a selezione multipla e, se necessario, scorre l'elemento nella visualizzazione.
ms.assetid: 643783f2-0e00-4b79-b957-47938bb9f8da
keywords:
- Controlli di Windows Message LB_SETSEL
topic_type:
- apiref
api_name:
- LB_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd50f12c4190ba9ecafad11b167c1ac60adf691d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478538"
---
# <a name="lb_setsel-message"></a>\_Messaggio SETSEL lb

Seleziona un elemento in una casella di riepilogo a selezione multipla e, se necessario, scorre l'elemento nella visualizzazione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica come impostare la selezione. Se questo parametro è **true**, l'elemento viene selezionato ed evidenziato; Se è **false**, l'evidenziazione viene rimossa e l'elemento non è più selezionato.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica l'indice in base zero dell'elemento da impostare. Se questo parametro è-1, la selezione viene aggiunta o rimossa da tutti gli elementi, a seconda del valore di *wParam*, e non si verifica alcuno scorrimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si verifica un errore, il valore restituito è LB \_ Err.

## <a name="remarks"></a>Commenti

Utilizzare questo messaggio solo con caselle di riepilogo a selezione multipla.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_GETSEL lb**](lb-getsel.md)
</dt> <dt>

[**\_SELITEMRANGE lb**](lb-selitemrange.md)
</dt> </dl>

 

 





