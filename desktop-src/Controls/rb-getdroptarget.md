---
title: RB_GETDROPTARGET messaggio (Commctrl.h)
description: Recupera il puntatore a interfaccia IDropTarget di un controllo rebar.
ms.assetid: f429c5d1-406b-47f0-a654-47cabccc1d0e
keywords:
- RB_GETDROPTARGET dei messaggi Windows controlli
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
ms.openlocfilehash: 5793d2192ef65f193ff27d40cc14660c90d067034d8c1304e1bde1a354a4f493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169611"
---
# <a name="rb_getdroptarget-message"></a>Messaggio RB \_ GETDROPTARGET

Recupera il puntatore a interfaccia [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) di un controllo rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un [**puntatore IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) che riceve il puntatore a interfaccia. È responsabilità del chiamante chiamare [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su questo puntatore quando non è più necessario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene usato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

