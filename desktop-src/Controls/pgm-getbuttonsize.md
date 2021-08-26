---
title: PGM_GETBUTTONSIZE messaggio (Commctrl.h)
description: Recupera le dimensioni correnti del pulsante per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Pager GetButtonSize.
ms.assetid: fa8b4814-4587-4149-83a7-84faad2a4641
keywords:
- PGM_GETBUTTONSIZE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a77bbfdbac95c10afc721cfbae41798083ea98f4dd78e9dfdec9099871d7afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985900"
---
# <a name="pgm_getbuttonsize-message"></a>Messaggio \_ GETBUTTONSIZE PGM

Recupera le dimensioni correnti del pulsante per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Pager GetButtonSize.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore INT che contiene le dimensioni correnti del pulsante, in pixel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PGM \_ SETBUTTONSIZE**](pgm-setbuttonsize.md)
</dt> </dl>

 

 





