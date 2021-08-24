---
title: TB_INDETERMINATE messaggio (Commctrl.h)
description: Imposta o cancella lo stato indeterminato del pulsante specificato in una barra degli strumenti.
ms.assetid: 6a0f2b82-8241-4c2e-b349-606975ba1a24
keywords:
- TB_INDETERMINATE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_INDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90845f269d0af1e690d5ddeb02f2a8ec2a2f63ff4f698f1dd0f3e2729d98b72c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078265"
---
# <a name="tb_indeterminate-message"></a>TB \_ INDETERMINATE message

Imposta o cancella lo stato indeterminato del pulsante specificato in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore del comando del pulsante il cui stato indeterminato deve essere impostato o cancellato.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD è**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un **valore BOOL** che indica se impostare o cancellare lo stato indeterminato. Se **TRUE,** viene impostato lo stato indeterminato. Se **FALSE,** lo stato viene cancellato.

HIWORD [**deve**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

