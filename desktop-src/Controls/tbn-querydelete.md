---
title: TBN_QUERYDELETE di notifica (Commctrl.h)
description: Notifica alla finestra padre della barra degli strumenti se un pulsante può essere eliminato da una barra degli strumenti mentre l'utente sta personalizzando la barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- TBN_QUERYDELETE codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TBN_QUERYDELETE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a01d1322ce8461c5cdb53fc76cfc220bbb5d292dedbe589d8b6ada5a48756d55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077885"
---
# <a name="tbn_querydelete-notification-code"></a>Codice di notifica \_ TBN QUERYDELETE

Notifica alla finestra padre della barra degli strumenti se un pulsante può essere eliminato da una barra degli strumenti mentre l'utente sta personalizzando la barra degli strumenti. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_QUERYDELETE 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTOOLBAR.**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) Il membro **iItem** contiene l'indice in base zero del pulsante da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** per consentire l'eliminazione del pulsante o **FALSE** per impedire l'eliminazione del pulsante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





