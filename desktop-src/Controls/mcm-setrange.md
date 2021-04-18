---
title: Messaggio MCM_SETRANGE (COMmctrl. h)
description: Imposta le date minime e massime consentite per un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetRange MonthCal.
ms.assetid: dab9ebb0-f397-4e71-b060-ef8d7d89a6bc
keywords:
- Controlli di Windows Message MCM_SETRANGE
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
ms.openlocfilehash: 380e599da8cd4a054c02135bc64f57f29d2c81d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302281"
---
# <a name="mcm_setrange-message"></a>\_Messaggio di SEtrange MCM

Imposta le date minime e massime consentite per un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetRange MonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag che specificano i limiti di data da impostare. Questo valore deve essere uno o entrambi gli elementi seguenti:



| Valore                                                                                                                                          | Significato                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <dt>**GDTR \_ Max**</dt> </dl> | È in corso l'impostazione della data massima consentita. La struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) in *lpSysTimeArray* \[ 1 \] deve contenere informazioni sulla data. <br/> |
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <dt>**GDTR \_ min**</dt> </dl> | È in corso l'impostazione della data minima consentita. La struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) in *lpSysTimeArray* \[ 0 \] deve contenere informazioni sulla data. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice a due elementi di strutture [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che contengono i limiti di data. Il limite massimo deve trovarsi in *lpSysTimeArray* \[ 1 \] se \_ si specifica GDTR Max e *lpSysTimeArray* \[ 0 \] deve contenere il limite minimo se \_ viene specificato GDTR min.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Orari del controllo calendario mensile](month-calendar-controls.md)
</dt> </dl>

 

