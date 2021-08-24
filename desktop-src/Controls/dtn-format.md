---
title: DTN_FORMAT codice di notifica (Commctrl.h)
description: Inviato da un controllo di selezione data e ora (DTP) per richiedere la visualizzazione del testo in un campo di callback. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: ce0ee230-638e-425f-9f34-c379342cea93
keywords:
- DTN_FORMAT codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- DTN_FORMAT
- DTN_FORMATA
- DTN_FORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75fb4279f6ec6b95ded673083a024d32785dd5156588852663e6c307f8351dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916271"
---
# <a name="dtn_format-notification-code"></a>Codice di notifica DTN \_ FORMAT

Inviato da un controllo di selezione data e ora (DTP) per richiedere la visualizzazione del testo in un campo di callback. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
DTN_FORMAT

    lpNMFormat = (LPNMDATETIMEFORMAT) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) contenente informazioni relative a questa istanza del codice di notifica. La struttura contiene la sottostringa che definisce il campo di callback e riceve la stringa formattata che verrà visualizzata dal controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il proprietario del controllo deve restituire zero.

## <a name="remarks"></a>Commenti

La gestione di questo codice di notifica consente al proprietario del controllo di fornire una stringa personalizzata che verrà visualizzata dal controllo. Per altre informazioni sui campi di callback, vedere [Campi di callback.](date-and-time-picker-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DTN \_ FORMATW** (Unicode) e **DTN \_ FORMATA** (ANSI)<br/>                     |



 

 





