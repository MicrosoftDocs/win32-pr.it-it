---
title: NM_CHAR codice di notifica (Commctrl.h)
description: Il codice di notifica NM \_ CHAR viene inviato da un controllo quando viene elaborato un tasto carattere. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- NM_CHAR codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73c35871410244bfb69f67c7e0b2c960d0dd50d432ad9cdcfd8765c7df449bf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018949"
---
# <a name="nm_char-notification-code"></a>Codice di notifica NM \_ CHAR

Il codice di notifica NM \_ CHAR viene inviato da un controllo quando viene elaborato un tasto carattere. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) che contiene informazioni aggiuntive sul carattere che ha causato il codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato dalla maggior parte dei controlli. Per altre informazioni, vedere la documentazione per i singoli controlli.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[NM \_ CHAR (barra degli strumenti)](nm-char-toolbar.md)
</dt> </dl>

 

 





