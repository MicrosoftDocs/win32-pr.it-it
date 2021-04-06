---
title: Codice di notifica LVN_BEGINLABELEDIT (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco l'inizio della modifica dell'etichetta per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: c13a9e95-22a9-476e-aeee-4928b8b096b0
keywords:
- Controlli di Windows per il codice di notifica LVN_BEGINLABELEDIT
topic_type:
- apiref
api_name:
- LVN_BEGINLABELEDIT
- LVN_BEGINLABELEDITA
- LVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f77550b474534cee096b610a0805bce547d9b429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963802"
---
# <a name="lvn_beginlabeledit-notification-code"></a>\_Codice di notifica BEGINLABELEDIT di LVN

Notifica alla finestra padre di un controllo di visualizzazione elenco l'inizio della modifica dell'etichetta per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_BEGINLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . Il membro dell' **elemento** di questa struttura è una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) il cui membro **iItem** identifica l'elemento da modificare. Si noti che gli elementi secondari non possono essere modificati; il membro **iSubItem** è sempre impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per consentire all'utente di modificare l'etichetta, restituire **false**.

Per impedire all'utente di modificare l'etichetta, restituire **true**.

## <a name="remarks"></a>Commenti

Quando viene avviata la modifica dell'etichetta, viene creato, posizionato e inizializzato un controllo di modifica. Prima che venga visualizzato, il controllo elenco-visualizzazione Invia la finestra padre di un \_ codice di notifica BEGINLABELEDIT LVN.

Per personalizzare la modifica delle etichette, implementare un gestore per LVN \_ BEGINLABELEDIT e inviare un messaggio [**LVM \_ GETEDITCONTROL**](lvm-geteditcontrol.md) al controllo List-View. Se è in corso la modifica di un'etichetta, il valore restituito sarà un handle per il controllo di modifica. Utilizzare questo handle per personalizzare il controllo di modifica inviando i normali messaggi **em \_ xxx** .

Quando l'utente annulla o completa la modifica, la finestra padre riceve un codice di [notifica \_ ENDLABELEDIT LVN](lvn-endlabeledit.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVN \_ BEGINLABELEDITW** (Unicode) e **LVN \_ BEGINLABELEDITA** (ANSI)<br/>     |



 

 





