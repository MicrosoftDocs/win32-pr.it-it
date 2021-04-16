---
title: Messaggio DTM_SETMCFONT (COMmctrl. h)
description: Imposta il tipo di carattere che verrà utilizzato dal controllo Calendar Month Child del controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime SetMonthCalFont.
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- Controlli di Windows Message DTM_SETMCFONT
topic_type:
- apiref
api_name:
- DTM_SETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b148ffb95acd82257265bf0bab53000b10803793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477932"
---
# <a name="dtm_setmcfont-message"></a>\_Messaggio SETMCFONT DTM

Imposta il tipo di carattere che verrà utilizzato dal controllo Calendar Month Child del controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il tipo di carattere che verrà impostato.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica se il controllo deve essere ridisegnato immediatamente dopo l'impostazione del tipo di carattere. Se si imposta questo parametro su **true** , il controllo verrà ridisegnato automaticamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





