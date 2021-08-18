---
title: TBN_DRAGOUT di notifica (Commctrl.h)
description: Inviato da un controllo barra degli strumenti quando l'utente fa clic su un pulsante e quindi sposta il cursore fuori dal pulsante. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 3566ad60-9744-494f-bb02-d30b41d06351
keywords:
- TBN_DRAGOUT del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TBN_DRAGOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad707fa357a487e271bbe03039745b97521542a1305f9745a71a56044060c950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077945"
---
# <a name="tbn_dragout-notification-code"></a>Codice di notifica \_ TBN DRAGOUT

Inviato da un controllo barra degli strumenti quando l'utente fa clic su un pulsante e quindi sposta il cursore fuori dal pulsante. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_DRAGOUT

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) che contiene informazioni su questo codice di notifica. Per questo codice di notifica, sono validi solo i membri **hdr** e **iItem** di questa struttura. Il **membro iItem** di questa struttura contiene l'identificatore di comando del pulsante trascinato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Questo codice di notifica consente a un'applicazione di implementare la funzionalità di trascinamento della selezione per i pulsanti della barra degli strumenti. Durante l'elaborazione di questo codice di notifica, l'applicazione inizierà l'operazione di trascinamento della selezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





