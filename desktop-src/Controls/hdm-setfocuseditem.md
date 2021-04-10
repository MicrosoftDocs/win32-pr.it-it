---
title: Messaggio HDM_SETFOCUSEDITEM (COMmctrl. h)
description: Imposta lo stato attivo su un elemento specificato in un controllo intestazione. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro SetFocusedItem dell'intestazione.
ms.assetid: 20a321ce-4420-4239-b34d-9e7f24a89fc3
keywords:
- Controlli di Windows Message HDM_SETFOCUSEDITEM
topic_type:
- apiref
api_name:
- HDM_SETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd416744478248760f4e2c9f94a362db5a8d327
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120846"
---
# <a name="hdm_setfocuseditem-message"></a>\_Messaggio HDM SETFOCUSEDITEM

Imposta lo stato attivo su un elemento specificato in un controllo intestazione. Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ SetFocusedItem dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Non usato. Deve essere zero.</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Indice dell'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sui controlli intestazione](header-controls.md)
</dt> </dl>

 

 





