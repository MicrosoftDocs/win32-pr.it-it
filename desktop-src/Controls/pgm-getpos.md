---
title: PGM_GETPOS messaggio (Commctrl.h)
description: Recupera la posizione di scorrimento corrente del controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro GetPos del \_ pager.
ms.assetid: 1e0f967a-3290-43b7-b812-8cf56abf2d32
keywords:
- PGM_GETPOS dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- PGM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16f1d5608b720d5a5d3d661a368d094da9469d71108874a6cec5495bf120cc54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046871"
---
# <a name="pgm_getpos-message"></a>Messaggio \_ GETPOS PGM

Recupera la posizione di scorrimento corrente del controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetPos del pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore INT che contiene la posizione di scorrimento corrente, in pixel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





