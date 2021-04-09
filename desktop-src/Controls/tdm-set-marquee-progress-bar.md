---
title: Messaggio TDM_SET_MARQUEE_PROGRESS_BAR (COMmctrl. h)
description: Indica se l'indicatore di stato ospitato di una finestra di dialogo attività deve essere visualizzato in modalità marquee.
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- Controlli di Windows Message TDM_SET_MARQUEE_PROGRESS_BAR
topic_type:
- apiref
api_name:
- TDM_SET_MARQUEE_PROGRESS_BAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a9384826b89d07c6564dc511d4909058871ca3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121298"
---
# <a name="tdm_set_marquee_progress_bar-message"></a>Messaggio indicatore indicatore di stato TDM \_ set \_ Marquee \_ \_

Indica se l'indicatore di stato ospitato di una finestra di dialogo attività deve essere visualizzato in modalità marquee.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

**Bool** che indica se l'indicatore di stato deve essere visualizzato in modalità marquee. Il valore **true** attiva la modalità marquee e il valore **false** disattiva la modalità marquee.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Per informazioni sulla modalità Marquee, vedere [controllo indicatore di stato](progress-bar-control.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





