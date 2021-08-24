---
title: PGM_SETBORDER messaggio (Commctrl.h)
description: Imposta le dimensioni correnti del bordo per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Pager SetBorder.
ms.assetid: 073a1f9e-f05b-4203-9035-8106e87e55cd
keywords:
- PGM_SETBORDER di controllo Windows messaggio
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
ms.openlocfilehash: 4c44433189c9d791aba1d50372176309682c1361c5b0efe31b11aaa99e9b322b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540531"
---
# <a name="pgm_setborder-message"></a>Messaggio PGM \_ SETBORDER

Imposta le dimensioni correnti del bordo per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Pager SetBorder.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Nuova dimensione del bordo, in pixel. Questo valore non deve essere maggiore del pulsante del pager o minore di zero. Se *lParam* è troppo grande, il bordo verrà disegnato con le stesse dimensioni del pulsante. Se *lParam* è negativo, le dimensioni del bordo verranno impostate su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore INT che contiene le dimensioni del bordo precedenti, in pixel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





