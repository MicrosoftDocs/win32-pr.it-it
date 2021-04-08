---
title: Codice di notifica DTN_USERSTRING (COMmctrl. h)
description: Inviato da un controllo di selezione data e ora (DTP) quando un utente completa la modifica di una stringa nel controllo.
ms.assetid: a5b13582-323b-4804-912c-a988d902547d
keywords:
- Controlli di Windows per il codice di notifica DTN_USERSTRING
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
ms.openlocfilehash: 4878875d23a0a5fce95aa4cc9ebfedfbdf24cb93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873437"
---
# <a name="dtn_userstring-notification-code"></a>\_Codice di notifica USERSTRING di DTN

Inviato da un controllo di selezione data e ora (DTP) quando un utente completa la modifica di una stringa nel controllo. Questo codice di notifica viene inviato solo dai controlli DTP impostati sullo stile [**DTS \_ APPCANPARSE**](date-and-time-picker-control-styles.md) . Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
DTN_USERSTRING

    lpDTstring = (LPNMDATETIMESTRING) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) che contiene informazioni sull'istanza del codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il proprietario del controllo deve restituire zero.

## <a name="remarks"></a>Commenti

La gestione di questo codice di notifica consente al proprietario di fornire risposte personalizzate alle stringhe immesse nel controllo dall'utente. Il proprietario deve essere preparato per analizzare la stringa di input ed eseguire l'azione, se necessario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DTN \_ USERSTRINGW** (Unicode) e **DTN \_ USERSTRINGA** (ANSI)<br/>             |



 

 





