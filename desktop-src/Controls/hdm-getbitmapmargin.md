---
title: Messaggio HDM_GETBITMAPMARGIN (COMmctrl. h)
description: Ottiene la larghezza del margine bitmap per un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetBitmapMargin dell'intestazione.
ms.assetid: 67794ad4-3c22-4fad-a1d7-7a5d5cc6ad67
keywords:
- Controlli di Windows Message HDM_GETBITMAPMARGIN
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
ms.openlocfilehash: 08c3f0fced77edd3f149009e1b3c2bb1eb75182c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964260"
---
# <a name="hdm_getbitmapmargin-message"></a>\_Messaggio HDM GETBITMAPMARGIN

Ottiene la larghezza del margine bitmap per un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetBitmapMargin dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) .

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETBITMAPMARGIN HDM**](hdm-setbitmapmargin.md)
</dt> </dl>

 

