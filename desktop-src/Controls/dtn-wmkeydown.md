---
title: DTN_WMKEYDOWN codice di notifica (Commctrl.h)
description: Inviato da un controllo di selezione data e ora (DTP) quando l'utente digitare in un campo di callback. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: e67e222d-28a1-4d30-ae64-8ec9a62fa321
keywords:
- DTN_WMKEYDOWN codice di notifica Windows controlli
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
ms.openlocfilehash: 0eaf822cc5eb8d1d8bdeca6b0853766774105af07cda77f55743d60d0fb12cdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019979"
---
# <a name="dtn_wmkeydown-notification-code"></a>Codice di notifica WMKEYDOWN DTN \_

Inviato da un controllo di selezione data e ora (DTP) quando l'utente digitare in un campo di callback. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
DTN_WMKEYDOWN

    lpDTKeystroke = (LPNMDATETIMEWMKEYDOWN)lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) contenente informazioni su questa istanza del codice di notifica. La struttura include informazioni sulla chiave digitata dall'utente, sulla sottostringa che definisce il campo di callback e sulla data e sull'ora correnti del sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il proprietario del controllo deve restituire zero.

## <a name="remarks"></a>Commenti

La gestione di questo codice di notifica consente al proprietario del controllo di fornire risposte specifiche alle sequenze di tasti all'interno dei campi di callback del controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DTN \_ WMKEYDOWNW** (Unicode) e **DTN \_ WMKEYDOWNA** (ANSI)<br/>               |



 

 





