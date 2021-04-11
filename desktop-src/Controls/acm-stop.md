---
title: Messaggio ACM_STOP (COMmctrl. h)
description: Interrompe la riproduzione di un clip AVI in un controllo Animation. È possibile inviare questo messaggio in modo esplicito o usando la macro di animazione \_ stop.
ms.assetid: ba39a579-665e-4d45-8f1f-f190acd76db7
keywords:
- Controlli di Windows Message ACM_STOP
topic_type:
- apiref
api_name:
- ACM_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e81cfc92ac2778ae559fcd9fb8db2b0cd7bb866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119243"
---
# <a name="acm_stop-message"></a>\_Messaggio di arresto ACM

Interrompe la riproduzione di un clip AVI in un controllo Animation. È possibile inviare questo messaggio in modo esplicito o usando la macro di [**animazione \_ Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





