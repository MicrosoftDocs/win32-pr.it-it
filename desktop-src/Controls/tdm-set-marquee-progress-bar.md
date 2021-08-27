---
title: TDM_SET_MARQUEE_PROGRESS_BAR messaggio (Commctrl.h)
description: Indica se l'indicatore di stato ospitato di una finestra di dialogo attività deve essere visualizzato in modalità selezione.
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- TDM_SET_MARQUEE_PROGRESS_BAR di controllo Windows messaggio
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
ms.openlocfilehash: 13262339f7d87ea68755a38a49cc8c327706939d6b18025f350334dfdbe3dd4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104611"
---
# <a name="tdm_set_marquee_progress_bar-message"></a>TDM \_ SET \_ MARQUEE \_ PROGRESS BAR \_ MESSAGE

Indica se l'indicatore di stato ospitato di una finestra di dialogo attività deve essere visualizzato in modalità selezione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Valore **BOOL** che indica se l'indicatore di stato deve essere visualizzato in modalità di selezione. Il valore **TRUE attiva** la modalità di selezione e il valore **FALSE** disattiva la modalità di selezione.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Per informazioni sulla modalità di selezione, vedere Controllo indicatore [di stato](progress-bar-control.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





