---
title: MCM_GETMONTHRANGE messaggio (Commctrl.h)
description: Recupera informazioni sulla data (usando strutture SYSTEMTIME) che rappresentano i limiti massimo e minimo della visualizzazione di un controllo calendario mensile. È possibile inviare questo messaggio in modo esplicito o tramite la macro MonthCal \_ GetMonthRange.
ms.assetid: f50ac4b7-1f58-4639-8c78-341bb33db3c3
keywords:
- MCM_GETMONTHRANGE dei messaggi Windows controllo
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
ms.openlocfilehash: bc55f9732199f2e6e031248003c6dcad4abe8cb713182081666cfbee6a4ce50b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319581"
---
# <a name="mcm_getmonthrange-message"></a>Messaggio \_ MCM GETMONTHRANGE

Recupera informazioni sulla data (usando [**strutture SYSTEMTIME)**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che rappresentano i limiti massimo e minimo della visualizzazione di un controllo calendario mensile. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MonthCal \_ GetMonthRange.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che specifica l'ambito dei limiti di intervallo da recuperare. Questo valore deve essere uno dei seguenti:



| Valore                                                                                                                                                      | Significato                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="GMR_DAYSTATE"></span><span id="gmr_daystate"></span><dl> <dt>**GMR \_ DAYSTATE**</dt> </dl> | Includere i mesi precedenti e finali dell'intervallo visibile che vengono visualizzati solo parzialmente. <br/> |
| <span id="GMR_VISIBLE"></span><span id="gmr_visible"></span><dl> <dt>**GMR \_ VISIBLE**</dt> </dl>    | Includere solo i mesi interamente visualizzati. <br/>                                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice a due elementi di [**strutture SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che riceverà i limiti inferiore e superiore dell'ambito specificato *da wParam*. I limiti inferiore e superiore vengono inseriti rispettivamente in *lprgSysTimeArray* 0 e \[ \] *lprgSysTimeArray* \[ \] 1. Questo parametro deve essere un indirizzo valido e non può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore INT che rappresenta l'intervallo, in mesi, compreso tra i due limiti restituiti in *lParam*.

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

 

