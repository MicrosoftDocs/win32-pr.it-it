---
title: LVN_HOTTRACK codice di notifica (Commctrl.h)
description: Inviato da un controllo di visualizzazione elenco quando l'utente sposta il mouse su un elemento. Questo codice di notifica viene inviato solo dai controlli di visualizzazione elenco con lo stile di visualizzazione elenco esteso LVS \_ EX \_ TRACKSELECT. Viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 6bbfe6b8-9b67-49e4-9481-65abe98608bb
keywords:
- LVN_HOTTRACK codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- LVN_HOTTRACK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ab311b17f287b695a6b21d333f7183fdda272029e2c57dfe468527d765d1602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830432"
---
# <a name="lvn_hottrack-notification-code"></a>Codice di notifica \_ LVN HOTTRACK

Inviato da un controllo di visualizzazione elenco quando l'utente sposta il mouse su un elemento. Questo codice di notifica viene inviato solo dai controlli di visualizzazione elenco con lo stile di visualizzazione elenco esteso [**LVS \_ EX \_ TRACKSELECT.**](extended-list-view-styles.md) Viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_HOTTRACK

    lpnmlv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) che contiene informazioni su questo codice di notifica. I **membri iItem**, **iSubItem** e **ptAction** di questa struttura contengono informazioni sull'elemento. L'applicazione ricevente può modificare **il membro iItem** per specificare l'elemento che verrà selezionato. Se **iItem** è impostato su -1, non verrà selezionato alcun elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituire zero per consentire alla visualizzazione elenco di eseguire la normale elaborazione di selezione della traccia. Se l'applicazione restituisce un valore diverso da zero, l'elemento non verrà selezionato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





