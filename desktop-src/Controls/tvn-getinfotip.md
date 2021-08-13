---
title: TVN_GETINFOTIP di notifica (Commctrl.h)
description: Inviato da un controllo di visualizzazione albero con lo stile \_ INFOTIP TVS. Questo codice di notifica viene inviato quando il controllo richiede la visualizzazione di informazioni di testo aggiuntive in una descrizione comando. Il codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 20576710-e279-4e61-be6b-bf1d8ea79555
keywords:
- TVN_GETINFOTIP del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TVN_GETINFOTIP
- TVN_GETINFOTIPA
- TVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5129e1fa97397cfa9c037c7c65099ee3bd961f184b1bf9b43d2dc87e35880f9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261161"
---
# <a name="tvn_getinfotip-notification-code"></a>Codice di notifica \_ TVN GETINFOTIP

Inviato da un controllo di visualizzazione albero con lo stile [**\_ INFOTIP TVS.**](tree-view-control-window-styles.md) Questo codice di notifica viene inviato quando il controllo richiede la visualizzazione di informazioni di testo aggiuntive in una descrizione comando. Il codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_GETINFOTIP

    lpGetInfoTip = (LPNMTVGETINFOTIP)lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) che contiene informazioni su questo codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il controllo ignora il valore restituito per questo codice di notifica.

## <a name="remarks"></a>Commenti

Questo codice di notifica viene inviato solo da controlli di visualizzazione albero con lo stile [**\_ INFOTIP TVS.**](tree-view-control-window-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ GETINFOTIPW** (Unicode) e **TVN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





