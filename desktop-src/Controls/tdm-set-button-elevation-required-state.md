---
title: Messaggio TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE (COMmctrl. h)
description: Specifica se un pulsante o un collegamento di comando di una determinata attività deve avere un'icona di schermatura controllo dell'account utente. ovvero se l'azione richiamata dal pulsante richiede l'elevazione dei privilegi.
ms.assetid: c4321fdb-3ea9-49bf-b53d-eb73d5b11084
keywords:
- Controlli di Windows Message TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE
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
ms.openlocfilehash: 7ef5f8479e88a3b63cbd5fab6a5686913864fd9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121299"
---
# <a name="tdm_set_button_elevation_required_state-message"></a>\_Messaggio di \_ \_ \_ stato richiesta di elevazione del pulsante set TDM \_

Specifica se un pulsante o un collegamento di comando di una determinata attività deve avere un'icona di schermatura controllo dell'account utente. ovvero se l'azione richiamata dal pulsante richiede l'elevazione dei privilegi.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

ID del pulsante di push o del collegamento del comando da aggiornare.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Impostare su 0 per indicare che l'azione richiamata dal pulsante non richiede l'elevazione dei privilegi. Impostare su un valore diverso da zero per indicare che l'azione richiede l'elevazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





