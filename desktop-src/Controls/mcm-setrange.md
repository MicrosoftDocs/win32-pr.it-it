---
title: MCM_SETRANGE messaggio (Commctrl.h)
description: Imposta le date minime e massime consentite per un controllo calendario mensile. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro MonthCal SetRange.
ms.assetid: dab9ebb0-f397-4e71-b060-ef8d7d89a6bc
keywords:
- MCM_SETRANGE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- MCM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c66e9cca17aabd93bfba896d361da6b90eab0c5c21fc4d50ec3c81a9eba5ccd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319251"
---
# <a name="mcm_setrange-message"></a>Messaggio \_ MCM SETRANGE

Imposta le date minime e massime consentite per un controllo calendario mensile. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ MonthCal SetRange.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valori di flag che specificano i limiti di data da impostare. Questo valore deve essere uno o entrambi gli elementi seguenti:



| Valore                                                                                                                                          | Significato                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <dt>**GDTR \_ MAX**</dt> </dl> | È in corso l'impostazione della data massima consentita. La [**struttura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) in *lpSysTimeArray* \[ 1 deve \] contenere informazioni sulla data. <br/> |
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <dt>**GDTR \_ MIN**</dt> </dl> | È in corso l'impostazione della data minima consentita. La [**struttura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) in *lpSysTimeArray* \[ 0 deve \] contenere informazioni sulla data. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice a due elementi di [**strutture SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che contengono i limiti di data. Il limite massimo deve essere in *lpSysTimeArray* 1 se si specifica \[ \] GDTR MAX e \_ *lpSysTimeArray* 0 deve contenere il limite minimo se si specifica \[ \] GDTR \_ MIN.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Ore nel controllo Calendario mensile](month-calendar-controls.md)
</dt> </dl>

 

