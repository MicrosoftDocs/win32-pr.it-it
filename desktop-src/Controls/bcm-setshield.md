---
title: Messaggio BCM_SETSHIELD (COMmctrl. h)
description: Imposta lo stato di elevazione richieste per un pulsante o un collegamento di comando specificato per visualizzare un'icona con privilegi elevati. Inviare questo messaggio in modo esplicito o tramite il pulsante \_ SetElevationRequiredState macro.
ms.assetid: 2ce2a006-7136-415b-824b-46b282b100f4
keywords:
- Controlli di Windows Message BCM_SETSHIELD
topic_type:
- apiref
api_name:
- BCM_SETSHIELD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2149e2945f2876309459c287961b7b0a4a1f9acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119595"
---
# <a name="bcm_setshield-message"></a>\_Messaggio SESHIELD BCM

Imposta lo stato di elevazione richieste per un pulsante o un collegamento di comando specificato per visualizzare un'icona con privilegi elevati. Inviare questo messaggio in modo esplicito o tramite il [**pulsante \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) macro.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

**Bool** che è **true** per creare un'icona con privilegi elevati o **false** in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 1 se ha esito positivo o un codice di errore.

## <a name="remarks"></a>Commenti

Per ottenere questa funzionalità, è necessario manifestare un'applicazione per utilizzare comctl32.dll versione 6.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





