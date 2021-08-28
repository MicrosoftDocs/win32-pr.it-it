---
title: NM_DBLCLK (barra degli strumenti) codice di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo barra degli strumenti che l'utente ha fatto doppio clic sul pulsante sinistro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: c6198245-cfd4-4e1f-877d-94c1d47e09d2
keywords:
- NM_DBLCLK di notifica (barra degli strumenti) Windows controlli
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75abaf61938fbf377dbe8b6c5eaca99ff5ab027abe08c670de72a218dd51f1b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919661"
---
# <a name="nm_dblclk-toolbar-notification-code"></a>Codice \_ di notifica NM DBLCLK (barra degli strumenti)

Notifica alla finestra padre di un controllo barra degli strumenti che l'utente ha fatto doppio clic sul pulsante sinistro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_DBLCLK

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni su questo codice di notifica. Se è stato fatto clic con il mouse su un elemento della barra degli strumenti, il membro **dwItemSpec** contiene l'identificatore dell'elemento e il membro **dwItemData** contiene i dati dell'elemento. Se è stato fatto clic con il mouse su un separatore o su uno spazio vuoto nella barra degli strumenti, il membro **dwItemSpec** conterrà -1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **FALSE** per consentire al controllo barra degli strumenti di eseguire l'elaborazione predefinita dell'evento oppure **TRUE** per impedire al controllo di elaborare l'evento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





