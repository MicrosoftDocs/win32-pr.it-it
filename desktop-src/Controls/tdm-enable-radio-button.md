---
title: Messaggio TDM_ENABLE_RADIO_BUTTON (COMmctrl. h)
description: Abilita o Disabilita un pulsante di opzione in una finestra di dialogo attività.
ms.assetid: da605ce0-b2d5-481a-a0e1-628ae5b65726
keywords:
- Controlli di Windows Message TDM_ENABLE_RADIO_BUTTON
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
ms.openlocfilehash: a78445158c5edc920eb329cdfc52d44f9cb7d6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964850"
---
# <a name="tdm_enable_radio_button-message"></a>TDM \_ Abilita \_ \_ messaggio pulsante di opzione

Abilita o Disabilita un pulsante di opzione in una finestra di dialogo attività.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Valore **int** che specifica l'ID del pulsante di opzione da abilitare o disabilitare.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Specifica lo stato del pulsante. Impostare su 0 per disabilitare il pulsante. impostare su un valore diverso da zero per abilitare il pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





