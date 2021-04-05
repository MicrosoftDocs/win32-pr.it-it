---
title: Messaggio PGM_SETBORDER (COMmctrl. h)
description: Imposta la dimensione corrente del bordo per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro pager di pager \_ .
ms.assetid: 073a1f9e-f05b-4203-9035-8106e87e55cd
keywords:
- Controlli di Windows Message PGM_SETBORDER
topic_type:
- apiref
api_name:
- PGM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a987246a56da213098ba8632044af97ae51462df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048260"
---
# <a name="pgm_setborder-message"></a>\_Messaggio di DEBORDO PGM

Imposta la dimensione corrente del bordo per il controllo pager. È possibile inviare questo messaggio in modo esplicito o [**usare \_ la macro pager di pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Nuove dimensioni del bordo, in pixel. Il valore non deve essere maggiore del pulsante cercapersone o minore di zero. Se *lParam* è troppo grande, il bordo verrà disegnato con le stesse dimensioni del pulsante. Se *lParam* è negativo, la dimensione del bordo verrà impostata su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore INT che contiene le dimensioni del bordo precedenti, in pixel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





