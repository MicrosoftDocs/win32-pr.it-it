---
title: Messaggio PGM_FORWARDMOUSE (COMmctrl. h)
description: Abilita o Disabilita l'avanzamento del mouse per il controllo pager. Quando l'avanzamento del mouse è abilitato, il controllo pager trasmette i \_ messaggi di WM MOUSEMOVE alla finestra contenuta. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro ForwardMouse del cercapersone.
ms.assetid: 269972fe-50b3-4c9f-b5ac-65e768b30684
keywords:
- Controlli di Windows Message PGM_FORWARDMOUSE
topic_type:
- apiref
api_name:
- PGM_FORWARDMOUSE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: addc1c6bf762f540e9d7d785a5af2ba3fb7da93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302052"
---
# <a name="pgm_forwardmouse-message"></a>\_Messaggio FORWARDMOUSE PGM

Abilita o Disabilita l'avanzamento del mouse per il controllo pager. Quando l'avanzamento del mouse è abilitato, il controllo pager trasmette i messaggi di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) alla finestra contenuta. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ ForwardMouse del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore **bool** che determina se l'avanzamento del mouse è abilitato o disabilitato. Se questo valore è diverso da zero, l'avanzamento del mouse è abilitato. Se questo valore è zero, l'avanzamento del mouse è disabilitato.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

