---
title: PGM_GETBORDER messaggio (Commctrl.h)
description: Recupera le dimensioni correnti del bordo per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetBorder del pager.
ms.assetid: 5d2f49ad-d940-4a0b-b5a0-05d742151b1c
keywords:
- PGM_GETBORDER dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- PGM_GETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148b3d840548116d3082e27b5a760650c5802bdb2c6dbc1fc7c94f1df3a3d5b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046861"
---
# <a name="pgm_getborder-message"></a>Messaggio \_ GETBORDER PGM

Recupera le dimensioni correnti del bordo per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetBorder del pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore INT che contiene le dimensioni correnti del bordo, in pixel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PGM \_ SETBORDER**](pgm-setborder.md)
</dt> </dl>

 

 





