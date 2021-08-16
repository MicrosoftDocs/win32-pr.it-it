---
title: LVN_GETINFOTIP di notifica (Commctrl.h)
description: Inviato da un controllo visualizzazione elenco di visualizzazione icone di grandi dimensioni con lo stile esteso LVS \_ EX \_ INFOTIP.
ms.assetid: 62be5087-7e49-4722-a63a-1768e030af48
keywords:
- LVN_GETINFOTIP del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- LVN_GETINFOTIP
- LVN_GETINFOTIPA
- LVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f7477230913ec5efd0827bc48e1a6021619aa4cdbbad252426d1af364b5b36b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830442"
---
# <a name="lvn_getinfotip-notification-code"></a>Codice di notifica \_ LVN GETINFOTIP

Inviato da un controllo visualizzazione elenco di visualizzazione icone di grandi dimensioni con lo stile [**esteso LVS \_ EX \_ INFOTIP.**](extended-list-view-styles.md) Questo codice di notifica viene inviato quando il controllo visualizzazione elenco richiede la visualizzazione di informazioni di testo aggiuntive in una descrizione comando. Viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_GETINFOTIP

    pGetInfoTip = (LPNMLVGETINFOTIP) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) che contiene informazioni su questo codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene utilizzato.

## <a name="remarks"></a>Commenti

Questo codice di notifica viene inviato solo dai controlli di visualizzazione elenco con lo stile [**esteso LVS \_ EX \_ INFOTIP.**](extended-list-view-styles.md) Il codice di notifica \_ LVN GETINFOTIP viene inviato solo per l'elemento secondario 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVN \_ GETINFOTIPW** (Unicode) e **LVN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





