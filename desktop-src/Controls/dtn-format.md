---
title: Codice di notifica DTN_FORMAT (COMmctrl. h)
description: Inviato da un controllo di selezione data e ora (DTP) per richiedere il testo da visualizzare in un campo di callback. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ce0ee230-638e-425f-9f34-c379342cea93
keywords:
- Controlli di Windows per il codice di notifica DTN_FORMAT
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
ms.openlocfilehash: 4fadd11b090777d2226eeed85f32d2062e8340e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477633"
---
# <a name="dtn_format-notification-code"></a>\_Codice di notifica del formato DTN

Inviato da un controllo di selezione data e ora (DTP) per richiedere il testo da visualizzare in un campo di callback. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
DTN_FORMAT

    lpNMFormat = (LPNMDATETIMEFORMAT) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) contenente informazioni relative a questa istanza del codice di notifica. La struttura contiene la sottostringa che definisce il campo di callback e riceve la stringa formattata che il controllo visualizzerà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il proprietario del controllo deve restituire zero.

## <a name="remarks"></a>Commenti

La gestione di questo codice di notifica consente al proprietario del controllo di fornire una stringa personalizzata che verrà visualizzata dal controllo. Per ulteriori informazioni sui campi di callback, vedere [campi callback](date-and-time-picker-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DTN \_ FORMATW** (Unicode) e **DTN \_ formata** (ANSI)<br/>                     |



 

 





