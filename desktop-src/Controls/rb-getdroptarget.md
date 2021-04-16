---
title: Messaggio RB_GETDROPTARGET (COMmctrl. h)
description: Recupera un puntatore all'interfaccia IDropTarget del controllo Rebar.
ms.assetid: f429c5d1-406b-47f0-a654-47cabccc1d0e
keywords:
- Controlli di Windows Message RB_GETDROPTARGET
topic_type:
- apiref
api_name:
- RB_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b7960cc13230a2715348bc55e5e65de6f72e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477872"
---
# <a name="rb_getdroptarget-message"></a>\_Messaggio GETDROPTARGET RB

Recupera un puntatore all'interfaccia [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) del controllo Rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

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



 

