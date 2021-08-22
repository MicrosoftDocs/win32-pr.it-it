---
title: BCM_SETSHIELD messaggio (Commctrl.h)
description: Imposta lo stato di elevazione dei privilegi richiesto per un pulsante o un collegamento di comando specificato per visualizzare un'icona con privilegi elevati. Inviare questo messaggio in modo esplicito o tramite la \_ macro Button SetElevationRequiredState.
ms.assetid: 2ce2a006-7136-415b-824b-46b282b100f4
keywords:
- BCM_SETSHIELD dei messaggi Windows controlli
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
ms.openlocfilehash: 67ab7ab495e713d9f2c8d58c6723489f0099a7c2cba9df93d4f08870d521a0cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921491"
---
# <a name="bcm_setshield-message"></a>Messaggio \_ BCM SETSHIELD

Imposta lo stato di elevazione dei privilegi richiesto per un pulsante o un collegamento di comando specificato per visualizzare un'icona con privilegi elevati. Inviare questo messaggio in modo esplicito o tramite la macro [**\_ Button SetElevationRequiredState.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

VALORE **BOOL true** per **disegnare** un'icona con privilegi elevati oppure FALSE in **caso contrario.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 1 in caso di esito positivo oppure un codice di errore in caso contrario.

## <a name="remarks"></a>Commenti

Un'applicazione deve essere manifestata per usare comctl32.dll versione 6 per ottenere questa funzionalità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





