---
title: TBN_QUERYINSERT codice di notifica (Commctrl.h)
description: Notifica alla finestra padre della barra degli strumenti se è possibile inserire un pulsante a sinistra del pulsante specificato mentre l'utente personalizza una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- TBN_QUERYINSERT del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TBN_QUERYINSERT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44f741fd7cfa5c6f72405b10ba9678aed71f7cb2359743593f117b17c8ad1c8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166961"
---
# <a name="tbn_queryinsert-notification-code"></a>Codice di notifica \_ TBN QUERYINSERT

Notifica alla finestra padre della barra degli strumenti se è possibile inserire un pulsante a sinistra del pulsante specificato mentre l'utente personalizza una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_QUERYINSERT 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTOOLBAR.**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) Il membro **iItem** contiene l'indice in base zero del pulsante da inserire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** per consentire l'inserimento di un pulsante davanti al pulsante specificato oppure **FALSE** per impedire l'inserimento del pulsante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





