---
title: MCN_GETDAYSTATE codice di notifica (Commctrl.h)
description: Inviato da un controllo calendario mensile per richiedere informazioni sulla modalità di visualizzazione dei singoli giorni. Questo codice di notifica viene inviato solo dai controlli calendario mensile che usano lo stile MCS DAYSTATE e viene inviato sotto forma di \_ messaggio WM \_ NOTIFY.
ms.assetid: dc2608e0-c598-4b26-9195-208f09cd84b7
keywords:
- MCN_GETDAYSTATE codice di notifica Windows controlli
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
ms.openlocfilehash: 64af64fde86ed91ae41cbd3fed53e9cb27a0be410140bc1d25e0548a64042668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697141"
---
# <a name="mcn_getdaystate-notification-code"></a>Codice di notifica \_ MCN GETDAYSTATE

Inviato da un controllo calendario mensile per richiedere informazioni sulla modalità di visualizzazione dei singoli giorni. Questo codice di notifica viene inviato solo dai controlli calendario mensile che usano lo stile [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) e viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
MCN_GETDAYSTATE

    lpNMDayState = (LPNMDAYSTATE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMDAYSTATE.**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) La struttura contiene informazioni sull'intervallo di tempo per cui il controllo necessita di informazioni e riceve l'indirizzo di una matrice che fornisce questi dati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

La gestione di questo codice di notifica consente all'applicazione di personalizzarne la visualizzazione specificando che determinati giorni devono essere visualizzati in grassetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





