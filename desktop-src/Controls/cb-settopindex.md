---
title: Messaggio CB_SETTOPINDEX (winuser. h)
description: Un'applicazione invia il \_ messaggio SETTOPINDEX CB per assicurarsi che un particolare elemento sia visibile nella casella di riepilogo di una casella combinata.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- Controlli di Windows Message CB_SETTOPINDEX
topic_type:
- apiref
api_name:
- CB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f402cbd16cd61a829a2221600bd3c548829f348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740119"
---
# <a name="cb_settopindex-message"></a>\_Messaggio SETTOPINDEX CB

Un'applicazione invia il **messaggio \_ SETTOPINDEX CB** per assicurarsi che un particolare elemento sia visibile nella casella di riepilogo di una casella combinata. Il sistema scorre il contenuto della casella di riepilogo in modo che l'elemento specificato venga visualizzato nella parte superiore della casella di riepilogo oppure che sia stato raggiunto l'intervallo massimo di scorrimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'indice in base zero dell'elemento dell'elenco.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è zero.

Se il messaggio ha esito negativo, il valore restituito è CB \_ Err.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CB \_ GETTOPINDEX**](cb-gettopindex.md)
</dt> </dl>

 

 





