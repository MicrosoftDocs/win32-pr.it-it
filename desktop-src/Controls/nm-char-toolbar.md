---
title: NM_CHAR di notifica (barra degli strumenti) (Commctrl.h)
description: Inviato da una barra degli strumenti quando riceve un messaggio WM \_ CHAR. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 7bf0b046-da8e-448f-94e1-62ba0989f7ba
keywords:
- NM_CHAR di notifica (barra degli strumenti) Windows controlli
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
ms.openlocfilehash: a318c7385e9d7205ad0fa159e1f987c5d650d27414eefeed4d915c5544cb4564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018939"
---
# <a name="nm_char-toolbar-notification-code"></a>Codice di \_ notifica NM CHAR (barra degli strumenti)

Inviato da una barra degli strumenti quando riceve un [**messaggio WM \_ CHAR.**](/windows/desktop/inputdev/wm-char) Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) che contiene informazioni aggiuntive sul carattere che ha causato il codice di notifica. Il **membro dwItemPrev** di questa struttura contiene l'identificatore di comando dell'elemento attualmente in stato di accesso o -1 se nessun elemento è attualmente in stato di accesso. Il **membro dwItemNext** di questa struttura contiene l'identificatore di comando dell'elemento che diventerà hot o -1 se il tasto non corrisponde ad alcun tasto di scelta rapida dell'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** per indicare che la barra degli strumenti non deve elaborare il carattere e **FALSE** per fare in modo che la barra degli strumenti ese elaborare il carattere.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

