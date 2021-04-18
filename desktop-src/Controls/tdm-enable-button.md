---
title: Messaggio TDM_ENABLE_BUTTON (COMmctrl. h)
description: Abilita o Disabilita un pulsante di push in una finestra di dialogo attività.
ms.assetid: 133fe4ac-4e2d-4826-8510-c0d9f88b5b37
keywords:
- Controlli di Windows Message TDM_ENABLE_BUTTON
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
ms.openlocfilehash: db10d616b4d07adcdc8c97495f7d12c89e603a7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302514"
---
# <a name="tdm_enable_button-message"></a>\_Messaggio di abilitazione del \_ pulsante TDM

Abilita o Disabilita un pulsante di push in una finestra di dialogo attività.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Valore **int** che specifica l'ID del pulsante di push da abilitare o disabilitare.

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



 

 





