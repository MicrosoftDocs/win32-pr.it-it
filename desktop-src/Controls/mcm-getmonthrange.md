---
title: Messaggio MCM_GETMONTHRANGE (COMmctrl. h)
description: Recupera le informazioni sulla data (usando le strutture SYSTEMTIME) che rappresentano i limiti massimo e minimo della visualizzazione di un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetMonthRange.
ms.assetid: f50ac4b7-1f58-4639-8c78-341bb33db3c3
keywords:
- Controlli di Windows Message MCM_GETMONTHRANGE
topic_type:
- apiref
api_name:
- MCM_GETMONTHRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022ca7e05cc0c69cd32f6ad92531420cdaed7c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302795"
---
# <a name="mcm_getmonthrange-message"></a>\_Messaggio GETMONTHRANGE MCM

Recupera le informazioni sulla data (usando le strutture [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) ) che rappresentano i limiti massimo e minimo della visualizzazione di un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che specifica l'ambito dei limiti di intervallo da recuperare. Questo valore deve essere uno dei seguenti:



| Valore                                                                                                                                                      | Significato                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="GMR_DAYSTATE"></span><span id="gmr_daystate"></span><dl> <dt>**\_DAYSTATE GMR**</dt> </dl> | Includere i mesi precedenti e finali dell'intervallo visibile che vengono visualizzati solo parzialmente. <br/> |
| <span id="GMR_VISIBLE"></span><span id="gmr_visible"></span><dl> <dt>**GMR \_ visibile**</dt> </dl>    | Includere solo i mesi che vengono visualizzati interamente. <br/>                                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice a due elementi di strutture [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che riceveranno i limiti inferiore e superiore dell'ambito specificato da *wParam*. I limiti inferiore e superiore vengono inseriti rispettivamente in *lprgSysTimeArray* \[ 0 \] e *lprgSysTimeArray* \[ 1 \] . Questo parametro deve essere un indirizzo valido e non può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore INT che rappresenta l'intervallo, in mesi, esteso dai due limiti restituiti in *lParam*.

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

 

