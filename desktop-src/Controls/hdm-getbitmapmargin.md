---
title: HDM_GETBITMAPMARGIN messaggio (Commctrl.h)
description: Ottiene la larghezza del margine della bitmap per un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Header GetBitmapMargin.
ms.assetid: 67794ad4-3c22-4fad-a1d7-7a5d5cc6ad67
keywords:
- HDM_GETBITMAPMARGIN di controllo Windows messaggio
topic_type:
- apiref
api_name:
- HDM_GETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 685fb96e2ecf97a33b264de7bb3a6579f0c3480b6a15fdf99929ae879f4b35c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436211"
---
# <a name="hdm_getbitmapmargin-message"></a>Messaggio \_ HDM GETBITMAPMARGIN

Ottiene la larghezza del margine della bitmap per un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Header GetBitmapMargin.**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la larghezza del margine della bitmap in pixel. Se il margine bitmap non è stato specificato in precedenza, viene restituito il valore predefinito 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM \_ CXEDGE).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**HDM \_ SETBITMAPMARGIN**](hdm-setbitmapmargin.md)
</dt> </dl>

 

