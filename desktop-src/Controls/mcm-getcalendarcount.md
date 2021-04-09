---
title: Messaggio MCM_GETCALENDARCOUNT (COMmctrl. h)
description: Ottiene il numero di calendari attualmente visualizzati nel controllo Calendar. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetCalendarCount.
ms.assetid: b9463f02-d37b-49b0-8387-0938020c23ee
keywords:
- Controlli di Windows Message MCM_GETCALENDARCOUNT
topic_type:
- apiref
api_name:
- MCM_GETCALENDARCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a3be9e9bcc5db8c1aab32cacbcc2ded82727af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120522"
---
# <a name="mcm_getcalendarcount-message"></a>\_Messaggio GETCALENDARCOUNT MCM

Ottiene il numero di calendari attualmente visualizzati nel controllo Calendar. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetCalendarCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Numero di calendari attualmente visualizzati nel controllo calendario. Il numero massimo di calendari consentiti è 12.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





