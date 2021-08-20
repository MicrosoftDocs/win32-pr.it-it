---
title: TBN_GETINFOTIP di notifica (Commctrl.h)
description: Recupera le informazioni della descrizione comandi per un elemento della barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 877de60c-f6e1-440a-81f0-d66ab443c985
keywords:
- TBN_GETINFOTIP del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TBN_GETINFOTIP
- TBN_GETINFOTIPA
- TBN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6adb47a940ce6795047a1aca8bb7cbdc0899a142c132ab8f6f39e6bb089f1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077905"
---
# <a name="tbn_getinfotip-notification-code"></a>Codice di \_ notifica TBN GETINFOTIP

Recupera le informazioni della descrizione comandi per un elemento della barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_GETINFOTIP

    lptbgit = (LPNMTBGETINFOTIP) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) che contiene informazioni sull'elemento e riceve informazioni di suggerimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato dal controllo .

## <a name="remarks"></a>Commenti

Il supporto della descrizione comandi nella barra degli strumenti consente alla barra degli strumenti di visualizzare le descrizioni comando per gli elementi di grandi dimensioni, come i caratteri INFOTIPSIZE. Se questo codice di notifica non viene elaborato, la barra degli strumenti userà il testo dell'elemento per la descrizione comandi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TBN \_ GETINFOTIPW** (Unicode) e **TBN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





