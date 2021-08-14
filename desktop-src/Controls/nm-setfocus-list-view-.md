---
title: NM_SETFOCUS di notifica (visualizzazione elenco) (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione elenco che il controllo ha ricevuto lo stato attivo per l'input. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 43d3b09a-f095-4f30-87a8-2f2e782d6720
keywords:
- NM_SETFOCUS di notifica (visualizzazione elenco) Windows controlli
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312382eb81694bc49a121cd336e76c361a3519222f63723bb8d5203201c996f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410304"
---
# <a name="nm_setfocus-list-view-notification-code"></a>Codice \_ di notifica DI NM SETFOCUS (visualizzazione elenco)

Notifica alla finestra padre di un controllo visualizzazione elenco che il controllo ha ricevuto lo stato attivo per l'input. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





