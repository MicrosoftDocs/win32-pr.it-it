---
title: TDM_SET_PROGRESS_BAR_MARQUEE messaggio (Commctrl.h)
description: Avvia e arresta la visualizzazione del riquadro di selezione dell'indicatore di stato in una finestra di dialogo attività e imposta la velocità del rettangolo di selezione.
ms.assetid: df947171-a916-4db9-abe0-57a3bf11037f
keywords:
- TDM_SET_PROGRESS_BAR_MARQUEE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_MARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b92816b70e683b9f58e0de2247b2710da38bee891caa39d9026fc342168c6be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060651"
---
# <a name="tdm_set_progress_bar_marquee-message"></a>TDM \_ SET PROGRESS BAR \_ \_ \_ MARQUEE message

Avvia e arresta la visualizzazione del riquadro di selezione dell'indicatore di stato in una finestra di dialogo attività e imposta la velocità del rettangolo di selezione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Valore **BOOL** che indica se attivare o disattivare la visualizzazione del riquadro di selezione. Usare **TRUE** per attivare la visualizzazione del riquadro di selezione o **FALSE** per disattivarlo.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

UINT **che** specifica il tempo, in millisecondi, tra gli aggiornamenti dell'animazione del rettangolo di selezione. Se questo parametro è zero, l'animazione del rettangolo di selezione viene aggiornata ogni 30 millisecondi.

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



 

 





