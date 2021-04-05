---
title: Codice di notifica NM_FONTCHANGED (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco quando il controllo ha modificato un tipo di carattere. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ffa019b0-34be-4bb3-b9dd-c267545fec84
keywords:
- Controlli di Windows per il codice di notifica NM_FONTCHANGED
topic_type:
- apiref
api_name:
- NM_FONTCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75003021f83276c953b5aa2cf0b812d20d60857b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873306"
---
# <a name="nm_fontchanged-notification-code"></a>\_Codice di notifica FONTCHANGED Nm

Inviato da un controllo di visualizzazione elenco quando il controllo ha modificato un tipo di carattere. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_FONTCHANGED
        
    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato dal controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





