---
title: Codice di notifica PSN_RESET (Prsht. h)
description: Notifica a una pagina che la finestra delle proprietà sta per essere eliminata definitivamente. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 75448852-8a5e-41a7-92b6-00692e771a06
keywords:
- Controlli di Windows per il codice di notifica PSN_RESET
topic_type:
- apiref
api_name:
- PSN_RESET
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5642a5354d934b37ee58007a9fb260befe201edd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301180"
---
# <a name="psn_reset-notification-code"></a>\_Codice di notifica di reimpostazione di PSN

Notifica a una pagina che la finestra delle proprietà sta per essere eliminata definitivamente. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
PSN_RESET 

    lppsn = (LPPSHNOTIFY) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contenente informazioni sul codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Tutte le modifiche apportate dopo l'ultimo codice di notifica dell' [ \_ applicazione di PSN](psn-apply.md) vengono annullate, tranne nel caso di [**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2), che non supporta tale codice di notifica.

Il membro **lParam** della struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) a cui punta *lParam* verrà impostato su **true** se l'utente ha fatto clic sul pulsante **X** nell'angolo superiore destro della finestra delle proprietà. Sarà **false** se l'utente ha fatto clic sul pulsante **Annulla** . La struttura **PSHNOTIFY** contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà.

Un'applicazione può usare questo codice di notifica come opportunità per eseguire operazioni di pulizia.

> [!Note]  
> La finestra delle proprietà è in corso di modifica dell'elenco di pagine quando \_ viene inviato il codice di notifica di reimpostazione di PSN. Non tentare di aggiungere, rimuovere o inserire pagine durante la gestione del codice di notifica. In questo modo si otterranno risultati imprevedibili.

 

Non chiamare la funzione [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) durante l'elaborazione del codice di notifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

