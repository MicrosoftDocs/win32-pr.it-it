---
title: TCN_GETOBJECT di notifica (Commctrl.h)
description: Inviato da un controllo Struttura a schede quando ha lo stile esteso TCS EX REGISTERDROP e un oggetto viene trascinato su un elemento della scheda \_ \_ nel controllo. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 0beddabe-0e97-4fe7-bcf7-adaba0d72dfe
keywords:
- TCN_GETOBJECT del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TCN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf5ec3a314a7380ccff5f8613145c890f8f304d73289ad5354b8668a09070b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166904"
---
# <a name="tcn_getobject-notification-code"></a>Codice di notifica \_ TCN GETOBJECT

Inviato da un controllo Struttura a schede quando ha lo stile esteso [**TCS \_ EX \_ REGISTERDROP**](tab-control-extended-styles.md) e un oggetto viene trascinato su un elemento della scheda nel controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TCN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) che contiene informazioni sull'elemento della scheda su cui viene trascinato l'oggetto e riceve i dati restituiti dall'applicazione in risposta a questo messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'applicazione che elabora questo codice di notifica deve restituire zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





