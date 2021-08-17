---
title: NM_RCLICK di notifica (barra degli strumenti) (Commctrl.h)
description: Inviato da un controllo barra degli strumenti quando l'utente fa clic sulla barra degli strumenti con il pulsante destro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: e9d2d871-e922-444d-a76c-e73f249ed410
keywords:
- NM_RCLICK di notifica (barra degli strumenti) Windows controlli
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52fde315a3c68712c58b7e9466c351c6ac9a9117710ee6f285bd9ba9521ba56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958070"
---
# <a name="nm_rclick-toolbar-notification-code"></a>Codice di \_ notifica NM RCLICK (barra degli strumenti)

Inviato da un controllo barra degli strumenti quando l'utente fa clic sulla barra degli strumenti con il pulsante destro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RCLICK

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni su questo codice di notifica. Se è stato fatto clic con il mouse su un elemento della barra degli strumenti, il membro **dwItemSpec** contiene l'identificatore dell'elemento e il membro **dwItemData** contiene i dati dell'elemento. Se è stato fatto clic con il mouse su un separatore o su uno spazio vuoto nella barra degli strumenti, il **membro dwItemSpec** conterrà -1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **FALSE per** consentire al controllo della barra degli strumenti di eseguire l'elaborazione predefinita dell'evento oppure **TRUE per** impedire al controllo di elaborare l'evento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





