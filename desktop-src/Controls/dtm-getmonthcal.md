---
title: Messaggio DTM_GETMONTHCAL (COMmctrl. h)
description: Ottiene l'handle per un controllo calendario mensile figlio (DTP) di selezione data e ora. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime GetMonthCal.
ms.assetid: 78bbdcc9-2b2b-420b-be9b-6f2f573d60b6
keywords:
- Controlli di Windows Message DTM_GETMONTHCAL
topic_type:
- apiref
api_name:
- DTM_GETMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99609ed3a437990889066da9a3424ef147c3d6b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964583"
---
# <a name="dtm_getmonthcal-message"></a>\_Messaggio GETMONTHCAL DTM

Ottiene l'handle per un controllo calendario mensile figlio (DTP) di selezione data e ora. È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle a un controllo calendario mensile figlio di un controllo DTP, se ha esito positivo, oppure **null** in caso contrario.

## <a name="remarks"></a>Commenti

I controlli DTP creano un controllo calendario mensile figlio quando l'utente fa clic sulla freccia a discesa (notifica a[ \_ discesa DTN](dtn-dropdown.md) ). Quando il calendario mensile non è più necessario, viene eliminato definitivamente, ovvero viene inviata una notifica di [ \_ primo piano DTN](dtn-closeup.md) per la distruzione. Quindi, l'applicazione non deve basarsi su un handle statico per il calendario mensile figlio del controllo DTP.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[primo piano DTN \_](dtn-closeup.md)
</dt> <dt>

[\_elenco a discesa DTN](dtn-dropdown.md)
</dt> </dl>

 

 





