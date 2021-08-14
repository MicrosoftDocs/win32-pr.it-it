---
title: CBEN_INSERTITEM codice di notifica (Commctrl.h)
description: Inviato quando è stato inserito un nuovo elemento nel controllo . Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: caf60156-10d2-4cfb-91c4-def6ee99c471
keywords:
- CBEN_INSERTITEM codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- CBEN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a58c1f8b14f4983e2f7e7444a8110f0407220b0c5bc682cfc73f72bee078ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413667"
---
# <a name="cben_insertitem-notification-code"></a>Codice di notifica \_ CBEN INSERTITEM

Inviato quando è stato inserito un nuovo elemento nel controllo . Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
CBEN_INSERTITEM

    pNMInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) contenente informazioni sul codice di notifica e sull'elemento inserito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'applicazione che elabora questo codice di notifica deve restituire zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





