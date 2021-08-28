---
title: DTN_USERSTRING di notifica (Commctrl.h)
description: Inviato da un controllo di selezione data e ora quando un utente completa la modifica di una stringa nel controllo.
ms.assetid: a5b13582-323b-4804-912c-a988d902547d
keywords:
- DTN_USERSTRING del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- DTN_USERSTRING
- DTN_USERSTRINGA
- DTN_USERSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6eabae4ed5a4fbe9ff0652b77fb7b6fbaf709b9030e3aa982af486ad6b7ed0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062921"
---
# <a name="dtn_userstring-notification-code"></a>Codice di notifica \_ DTN USERSTRING

Inviato da un controllo di selezione data e ora quando un utente completa la modifica di una stringa nel controllo. Questo codice di notifica viene inviato solo dai controlli DTP impostati sullo stile [**\_ APPCANPARSE DTS.**](date-and-time-picker-control-styles.md) Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
DTN_USERSTRING

    lpDTstring = (LPNMDATETIMESTRING) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) che contiene informazioni sull'istanza del codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il proprietario del controllo deve restituire zero.

## <a name="remarks"></a>Commenti

La gestione di questo codice di notifica consente al proprietario di fornire risposte personalizzate alle stringhe immesse nel controllo dall'utente. Il proprietario deve essere preparato ad analizzare la stringa di input ed eseguire un'azione, se necessario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DTN \_ USERSTRINGW** (Unicode) e **DTN \_ USERSTRINGA** (ANSI)<br/>             |



 

 





