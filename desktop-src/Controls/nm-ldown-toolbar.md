---
title: NM_LDOWN di notifica (barra degli strumenti) (Commctrl.h)
description: Notifica alla finestra padre di una barra degli strumenti che è stato premuto il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: f5b356fb-265b-4eb0-a5a3-2a22d688f847
keywords:
- NM_LDOWN di notifica (barra degli strumenti) Windows controlli
topic_type:
- apiref
api_name:
- NM_LDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf283e8b3e0d1ed780a80d5608849bc42f200b61a5a94692c0924cb2e6241a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919651"
---
# <a name="nm_ldown-toolbar-notification-code"></a>Codice di \_ notifica NM LDOWN (barra degli strumenti)

Notifica alla finestra padre di una barra degli strumenti che è stato premuto il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_LDOWN

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

## <a name="remarks"></a>Commenti

Questa notifica viene inviata dopo l'invio del codice di notifica [TBN \_ DROPDOWN.](tbn-dropdown.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





