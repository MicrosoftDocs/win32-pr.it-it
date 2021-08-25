---
title: DTM_SETMCFONT messaggio (Commctrl.h)
description: Imposta il tipo di carattere che deve essere utilizzato dal controllo calendario mensile figlio del controllo selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime SetMonthCalFont.
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- DTM_SETMCFONT di controllo Windows messaggio
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
ms.openlocfilehash: cfa1b34c1a51e365868cbdae30e46cd299937d3d6fe33bad6c57d630a0b226fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877811"
---
# <a name="dtm_setmcfont-message"></a>Messaggio DTM \_ SETMCFONT

Imposta il tipo di carattere che deve essere utilizzato dal controllo calendario mensile figlio del controllo selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ DateTime SetMonthCalFont.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il tipo di carattere che verrà impostato.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica se il controllo deve essere ridisegnato immediatamente dopo l'impostazione del tipo di carattere. Se si imposta questo **parametro su TRUE,** il controllo viene ridisegnato da solo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene usato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





