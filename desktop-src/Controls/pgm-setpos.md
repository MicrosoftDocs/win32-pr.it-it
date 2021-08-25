---
title: PGM_SETPOS messaggio (Commctrl.h)
description: Imposta la posizione di scorrimento corrente per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro SetPos del \_ pager.
ms.assetid: b882ea2d-9dab-4d36-9201-29522141f779
keywords:
- PGM_SETPOS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- PGM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a056d55d0ec70b3ff3068580c1e9923b363efa15e9ab26bf8aa67f476cc147
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046831"
---
# <a name="pgm_setpos-message"></a>Messaggio \_ PGM SETPOS

Imposta la posizione di scorrimento corrente per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetPos del pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore di tipo **int** che contiene la nuova posizione di scorrimento, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene usato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





