---
title: Codice di notifica LVN_HOTTRACK (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco quando l'utente sposta il puntatore del mouse su un elemento. Questo codice di notifica viene inviato solo da controlli visualizzazione elenco con \_ \_ stile di visualizzazione elenco esteso LVS ex TRACKSELECT. Viene inviato sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 6bbfe6b8-9b67-49e4-9481-65abe98608bb
keywords:
- Controlli di Windows per il codice di notifica LVN_HOTTRACK
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
ms.openlocfilehash: c677b69fa21cdbe3680442304f6745cfb3a907de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874702"
---
# <a name="lvn_hottrack-notification-code"></a>\_Codice di notifica HOTTRACK di LVN

Inviato da un controllo di visualizzazione elenco quando l'utente sposta il puntatore del mouse su un elemento. Questo codice di notifica viene inviato solo da controlli visualizzazione elenco con stile di visualizzazione elenco esteso [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) . Viene inviato sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
LVN_HOTTRACK

    lpnmlv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) che contiene informazioni su questo codice di notifica. I membri **iItem**, **iSubItem** e **ptAction** di questa struttura contengono informazioni sull'elemento. L'applicazione ricevente può modificare il membro **iItem** per specificare l'elemento che verrà selezionato. Se **iItem** è impostato su-1, non verrà selezionato alcun elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero per consentire alla visualizzazione elenco di eseguire la normale elaborazione SELECT di selezione. Se l'applicazione restituisce un valore diverso da zero, l'elemento non verrà selezionato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





