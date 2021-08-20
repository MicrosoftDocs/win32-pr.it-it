---
title: MCM_GETRANGE messaggio (Commctrl.h)
description: Recupera le date minime e massime consentite impostate per un controllo calendario mensile. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetRange MonthCal.
ms.assetid: 5000053a-2975-4781-b3c9-83f9763f679a
keywords:
- MCM_GETRANGE di controllo Windows messaggio
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
ms.openlocfilehash: 26f8b9d5a485b12caf720afe518a2fc5499e55eba07c90c2fde1bb34eea2404b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830395"
---
# <a name="mcm_getrange-message"></a>Messaggio \_ MCM GETRANGE

Recupera le date minime e massime consentite impostate per un controllo calendario mensile. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetRange MonthCal.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice a due elementi di [**strutture SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che riceverà le informazioni sul limite di date. Il limite minimo è impostato in *lprgSysTimeArray* \[ 0 \] e *lprgSysTimeArray* 1 riceve \[ il limite \] massimo. Se uno degli elementi è impostato su tutti gli zeri, non viene impostato alcun limite corrispondente per il controllo calendario mensile. Questo parametro deve essere un indirizzo valido e non può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD che** può essere zero (non sono impostati limiti) o una combinazione dei valori seguenti che specificano informazioni sui limiti:



| Codice restituito                                                                              | Descrizione                                                                                                                        |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GDTR \_ MAX**</dt> </dl> | Viene impostato un limite massimo per il controllo. *lprgSysTimeArray* \[ 0 \] è valido e contiene le informazioni sulla data applicabili. <br/> |
| <dl> <dt>**GDTR \_ MIN**</dt> </dl> | Viene impostato un limite minimo per il controllo. *lprgSysTimeArray* \[ 1 \] è valido e contiene le informazioni sulla data applicabili. <br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Ore nel controllo Calendario mensile](month-calendar-controls.md)
</dt> </dl>

 

