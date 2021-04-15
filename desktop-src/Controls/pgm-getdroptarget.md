---
title: Messaggio PGM_GETDROPTARGET (COMmctrl. h)
description: Recupera un puntatore all'interfaccia IDropTarget del controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro GetDropTarget del cercapersone.
ms.assetid: 6b548c30-2d32-4372-90e4-346a27dda218
keywords:
- Controlli di Windows Message PGM_GETDROPTARGET
topic_type:
- apiref
api_name:
- PGM_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b90f7f9667dd30a79b9345eec211a6ebfcd7a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477897"
---
# <a name="pgm_getdroptarget-message"></a>\_Messaggio GETDROPTARGET PGM

Recupera un puntatore all'interfaccia [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) del controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ GetDropTarget del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un puntatore [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) che riceve il puntatore a interfaccia. È responsabilità del chiamante chiamare il [**rilascio**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su questo puntatore quando non è più necessario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

