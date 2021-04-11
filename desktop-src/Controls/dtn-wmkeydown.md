---
title: Codice di notifica DTN_WMKEYDOWN (COMmctrl. h)
description: Inviato da un controllo di selezione data e ora (DTP) quando l'utente digita in un campo di callback. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: e67e222d-28a1-4d30-ae64-8ec9a62fa321
keywords:
- Controlli di Windows per il codice di notifica DTN_WMKEYDOWN
topic_type:
- apiref
api_name:
- DTN_WMKEYDOWN
- DTN_WMKEYDOWNA
- DTN_WMKEYDOWNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce2e7d0761308805746278d2f542f5e9458b56d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119167"
---
# <a name="dtn_wmkeydown-notification-code"></a>\_Codice di notifica WMKEYDOWN di DTN

Inviato da un controllo di selezione data e ora (DTP) quando l'utente digita in un campo di callback. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
DTN_WMKEYDOWN

    lpDTKeystroke = (LPNMDATETIMEWMKEYDOWN)lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) contenente informazioni su questa istanza del codice di notifica. La struttura include informazioni sulla chiave digitata dall'utente, la sottostringa che definisce il campo di callback e la data e l'ora di sistema correnti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il proprietario del controllo deve restituire zero.

## <a name="remarks"></a>Commenti

La gestione di questo codice di notifica consente al proprietario del controllo di fornire risposte specifiche alle sequenze di tasti all'interno dei campi di callback del controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DTN \_ WMKEYDOWNW** (Unicode) e **DTN \_ WMKEYDOWNA** (ANSI)<br/>               |



 

 





