---
title: Messaggio MCM_GETRANGE (COMmctrl. h)
description: Recupera le date minime e massime consentite impostate per un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro MonthCal GetRange.
ms.assetid: 5000053a-2975-4781-b3c9-83f9763f679a
keywords:
- Controlli di Windows Message MCM_GETRANGE
topic_type:
- apiref
api_name:
- MCM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c757c046b88479072eb0771ecbf3f7fb79cdb31b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874514"
---
# <a name="mcm_getrange-message"></a>\_Messaggio MCM GETrange

Recupera le date minime e massime consentite impostate per un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o usando la macro [**MonthCal \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice a due elementi di strutture [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che riceveranno le informazioni sui limiti di data. Il limite minimo è impostato in *lprgSysTimeArray* \[ 0 \] e *lprgSysTimeArray* \[ 1 \] riceve il limite massimo. Se uno dei due elementi viene impostato su tutti zeri, non viene impostato alcun limite corrispondente per il controllo di calendario mensile. Questo parametro deve essere un indirizzo valido e non può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** che può essere zero (nessun limite impostato) o una combinazione dei valori seguenti che specificano le informazioni sui limiti:



| Codice restituito                                                                              | Descrizione                                                                                                                        |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GDTR \_ Max**</dt> </dl> | Per il controllo è impostato un limite massimo. *lprgSysTimeArray* \[ 0 \] è valido e contiene le informazioni sulla data applicabili. <br/> |
| <dl> <dt>**GDTR \_ min**</dt> </dl> | È stato impostato un limite minimo per il controllo; *lprgSysTimeArray* \[ 1 \] è valido e contiene le informazioni sulla data applicabili. <br/> |



 

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

 

