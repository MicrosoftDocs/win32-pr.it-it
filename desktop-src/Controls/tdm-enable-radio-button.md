---
title: TDM_ENABLE_RADIO_BUTTON messaggio (Commctrl.h)
description: Abilita o disabilita un pulsante di opzione in una finestra di dialogo attività.
ms.assetid: da605ce0-b2d5-481a-a0e1-628ae5b65726
keywords:
- TDM_ENABLE_RADIO_BUTTON del messaggio Windows controlli
topic_type:
- apiref
api_name:
- TDM_ENABLE_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 493c6813f15baa3ad3b5ceb7050049f620010a9eed12d75d09b3c9f102aa62db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876072"
---
# <a name="tdm_enable_radio_button-message"></a>Messaggio del PULSANTE \_ DI OPZIONE ABILITA TDM \_ \_

Abilita o disabilita un pulsante di opzione in una finestra di dialogo attività.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Valore **int** che specifica l'ID del pulsante di opzione da abilitato o disabilitato.

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



 

 





