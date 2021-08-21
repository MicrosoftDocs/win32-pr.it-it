---
title: TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE messaggio (Commctrl.h)
description: Specifica se un pulsante della finestra di dialogo attività o un collegamento di comando specificato deve avere un'icona a forma di schermatura di Controllo dell'account utente. indica se l'azione richiamata dal pulsante richiede l'elevazione dei privilegi.
ms.assetid: c4321fdb-3ea9-49bf-b53d-eb73d5b11084
keywords:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c69998da085a74b144179a0a4244c787cd3a871d63eca1e5df9c4e555b1a7e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104621"
---
# <a name="tdm_set_button_elevation_required_state-message"></a>TDM \_ SET BUTTON ELEVATION REQUIRED STATE \_ \_ \_ \_ message

Specifica se un pulsante della finestra di dialogo attività o un collegamento di comando specificato deve avere un'icona a forma di schermatura di Controllo dell'account utente. indica se l'azione richiamata dal pulsante richiede l'elevazione dei privilegi.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

ID del pulsante di comando o del collegamento di comando da aggiornare.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Impostare su 0 per indicare che l'azione richiamata dal pulsante non richiede l'elevazione dei privilegi. Impostare su un valore diverso da zero per indicare che l'azione richiede l'elevazione dei privilegi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





