---
title: TDM_ENABLE_BUTTON messaggio (Commctrl.h)
description: Abilita o disabilita un pulsante di comando in una finestra di dialogo attività.
ms.assetid: 133fe4ac-4e2d-4826-8510-c0d9f88b5b37
keywords:
- TDM_ENABLE_BUTTON di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TDM_ENABLE_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a76603f61f3e27dce8cf7c8f5504457ce5a29a787b3b1f6357c1c519c735854
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104651"
---
# <a name="tdm_enable_button-message"></a>Messaggio TDM \_ ENABLE \_ BUTTON (Abilita TDM)

Abilita o disabilita un pulsante di comando in una finestra di dialogo attività.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Valore **int** che specifica l'ID del pulsante di comando da abilitato o disabilitato.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Specifica lo stato del pulsante. Impostare su 0 per disabilitare il pulsante. Impostare su un valore diverso da zero per abilitare il pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





