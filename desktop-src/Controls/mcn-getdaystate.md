---
title: Codice di notifica MCN_GETDAYSTATE (COMmctrl. h)
description: Inviato da un controllo di calendario mensile per richiedere informazioni sulla modalità di visualizzazione dei singoli giorni. Questo codice di notifica viene inviato solo da controlli calendario mensile che usano lo \_ stile DAYSTATE MCS e viene inviato sotto forma di messaggio di notifica WM \_ .
ms.assetid: dc2608e0-c598-4b26-9195-208f09cd84b7
keywords:
- Controlli di Windows per il codice di notifica MCN_GETDAYSTATE
topic_type:
- apiref
api_name:
- MCN_GETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff81b9f171884f39063c517cb17299a55b4053b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741690"
---
# <a name="mcn_getdaystate-notification-code"></a>\_Codice di notifica GETDAYSTATE di MCN

Inviato da un controllo di calendario mensile per richiedere informazioni sulla modalità di visualizzazione dei singoli giorni. Questo codice di notifica viene inviato solo da controlli calendario mensile che usano lo stile [**\_ DAYSTATE MCS**](month-calendar-control-styles.md) e viene inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
MCN_GETDAYSTATE

    lpNMDayState = (LPNMDAYSTATE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) . La struttura contiene informazioni sull'intervallo di tempo per il quale il controllo necessita di informazioni e riceve l'indirizzo di una matrice che fornisce questi dati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

La gestione di questo codice di notifica consente all'applicazione di personalizzare la visualizzazione specificando che determinati giorni devono essere visualizzati in grassetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





