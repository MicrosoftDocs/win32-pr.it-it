---
title: HDM_SETBITMAPMARGIN messaggio (Commctrl.h)
description: Imposta la larghezza del margine, espressa in pixel, di una bitmap in un controllo intestazione esistente. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Header SetBitmapMargin.
ms.assetid: 5ac04701-18c8-42d4-9850-fe6eb813672c
keywords:
- HDM_SETBITMAPMARGIN di Windows messaggi
topic_type:
- apiref
api_name:
- HDM_SETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa2e7c24ea52edc0001cea9f4d7184957c2cfbf50f15769df964351df91e5813
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435951"
---
# <a name="hdm_setbitmapmargin-message"></a>Messaggio \_ HDM SETBITMAPMARGIN

Imposta la larghezza del margine, espressa in pixel, di una bitmap in un controllo intestazione esistente. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Header SetBitmapMargin.**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Larghezza, espressa in pixel, del margine che circonda una bitmap all'interno di un controllo intestazione esistente.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la larghezza del margine della bitmap, in pixel. Se il margine bitmap non è stato specificato in precedenza, viene restituito il valore predefinito di 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM \_ CXEDGE).*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**HDM \_ GETBITMAPMARGIN**](hdm-getbitmapmargin.md)
</dt> </dl>

 

