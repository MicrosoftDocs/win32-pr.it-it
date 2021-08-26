---
title: TDM_CLICK_VERIFICATION messaggio (Commctrl.h)
description: Simula un clic sulla casella di controllo di verifica di una finestra di dialogo attività, se esistente.
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- TDM_CLICK_VERIFICATION dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- TDM_CLICK_VERIFICATION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3cda5e85b138225d69e159792cbe641122e91bf9602b3e0f5edafa419edc3c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876091"
---
# <a name="tdm_click_verification-message"></a>Messaggio DI VERIFICA \_ TDM CLICK \_

Simula un clic sulla casella di controllo di verifica di una finestra di dialogo attività, se esistente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

**TRUE** per impostare lo stato della casella di controllo da controllare. **FALSE** per impostarlo in modo che sia deselezionato.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

**TRUE** per impostare lo stato attivo della tastiera sulla casella di controllo. **FALSE in** caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





