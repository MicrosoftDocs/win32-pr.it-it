---
title: Codice di notifica TVN_BEGINLABELEDIT (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero l'inizio della modifica dell'etichetta per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44
keywords:
- Controlli di Windows per il codice di notifica TVN_BEGINLABELEDIT
topic_type:
- apiref
api_name:
- TVN_BEGINLABELEDIT
- TVN_BEGINLABELEDITA
- TVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34eccdeda553d0792a2862e3ca81a0889539d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301702"
---
# <a name="tvn_beginlabeledit-notification-code"></a>\_Codice di notifica BEGINLABELEDIT di TVN

Notifica alla finestra padre di un controllo di visualizzazione albero l'inizio della modifica dell'etichetta per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TVN_BEGINLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**struttura NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) . Il membro dell' **elemento** è una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che contiene informazioni valide sull'elemento da modificare nei membri **Hite**, **state**, **lParam** e **pszText** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** per annullare la modifica dell'etichetta.

## <a name="remarks"></a>Commenti

Quando viene avviata la modifica dell'etichetta, viene creato un controllo di modifica, ma non è posizionato o visualizzato. Prima che venga visualizzato, il controllo di visualizzazione albero Invia la finestra padre a un \_ codice di notifica di TVN BEGINLABELEDIT.

Per personalizzare la modifica delle etichette, implementare un gestore per TVN \_ BEGINLABELEDIT e fare in modo che invii un messaggio [**TVM \_ GETEDITCONTROL**](tvm-geteditcontrol.md) al controllo di visualizzazione albero. Se è in corso la modifica di un'etichetta, il valore restituito sarà un handle per il controllo di modifica. Utilizzare questo handle per personalizzare il controllo di modifica inviando i normali \_ messaggi em xxx.

Quando l'utente annulla o completa la modifica, la finestra padre riceve un codice di [notifica \_ ENDLABELEDIT di TVN](tvn-endlabeledit.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ BEGINLABELEDITW** (Unicode) e **TVN \_ BEGINLABELEDITA** (ANSI)<br/>     |



 

 





