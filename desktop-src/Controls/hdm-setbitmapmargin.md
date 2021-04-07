---
title: Messaggio HDM_SETBITMAPMARGIN (COMmctrl. h)
description: Imposta la larghezza del margine, espressa in pixel, di una bitmap in un controllo intestazione esistente. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetBitmapMargin dell'intestazione.
ms.assetid: 5ac04701-18c8-42d4-9850-fe6eb813672c
keywords:
- Controlli di Windows Message HDM_SETBITMAPMARGIN
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
ms.openlocfilehash: d2a5384151a63918a5828608b0aa8e829df61cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874269"
---
# <a name="hdm_setbitmapmargin-message"></a>\_Messaggio HDM SETBITMAPMARGIN

Imposta la larghezza del margine, espressa in pixel, di una bitmap in un controllo intestazione esistente. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetBitmapMargin dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Larghezza, espressa in pixel, del margine che racchiude una bitmap all'interno di un controllo intestazione esistente.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la larghezza, in pixel, del margine bitmap. Se il margine bitmap non è stato specificato in precedenza, viene restituito il valore predefinito 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM \_ CXEDGE*).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETBITMAPMARGIN HDM**](hdm-getbitmapmargin.md)
</dt> </dl>

 

