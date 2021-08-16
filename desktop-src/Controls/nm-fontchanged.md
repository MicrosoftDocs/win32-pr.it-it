---
title: NM_FONTCHANGED codice di notifica (Commctrl.h)
description: Inviato da un controllo di visualizzazione elenco quando il controllo ha modificato un tipo di carattere. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: ffa019b0-34be-4bb3-b9dd-c267545fec84
keywords:
- NM_FONTCHANGED codice di notifica Windows controlli
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
ms.openlocfilehash: b5369b7719a02e28562f4e71aecffdd3680aa602b6154eac9cc8685bdbe2b2b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411146"
---
# <a name="nm_fontchanged-notification-code"></a>Codice \_ di notifica FONTCHANGED di NM

Inviato da un controllo di visualizzazione elenco quando il controllo ha modificato un tipo di carattere. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_FONTCHANGED
        
    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato dal controllo .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





