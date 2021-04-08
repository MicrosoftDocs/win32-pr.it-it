---
title: Codice di notifica MCN_SELCHANGE (COMmctrl. h)
description: Inviato da un controllo di calendario mensile quando cambia la data o l'intervallo di date attualmente selezionato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 8923524f-d257-409d-bd3e-021684b88856
keywords:
- Controlli di Windows per il codice di notifica MCN_SELCHANGE
topic_type:
- apiref
api_name:
- MCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffa328ca0173afd3a577f6cf14e0204cd5c0f7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047996"
---
# <a name="mcn_selchange-notification-code"></a>\_Codice di notifica SelChange di MCN

Inviato da un controllo di calendario mensile quando cambia la data o l'intervallo di date attualmente selezionato. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
MCN_SELCHANGE

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) che contiene informazioni sull'intervallo di date attualmente selezionato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Ad esempio, il controllo Invia MCN \_ selChange quando l'utente modifica in modo esplicito la selezione nel mese corrente o quando la selezione viene modificata in modo implicito in risposta alla navigazione successiva/precedente del mese. Questo codice di notifica viene inoltre inviato dal sistema a intervalli regolari, in modo che il controllo possa rispondere alle modifiche apportate alla data.

Questo codice di notifica è simile a [MCN \_ SELECT](mcn-select.md), ma viene inviato in risposta a una modifica di selezione. MCN \_ Select viene inviato solo per la selezione di una data esplicita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





