---
title: Codice di notifica PSN_APPLY (Prsht. h)
description: Inviato a ogni pagina della finestra delle proprietà per indicare che l'utente ha fatto clic sul pulsante OK, Chiudi o applica e desidera che tutte le modifiche abbiano effetto. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 18da6bdb-9409-49b6-8116-580fedd99a02
keywords:
- Controlli di Windows per il codice di notifica PSN_APPLY
topic_type:
- apiref
api_name:
- PSN_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d8206b4e423fb01be3277a9dd0ca3a49b59129
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477548"
---
# <a name="psn_apply-notification-code"></a>PSN \_ applicare il codice di notifica

Inviato a ogni pagina della finestra delle proprietà per indicare che l'utente ha fatto clic sul pulsante OK, Chiudi o applica e desidera che tutte le modifiche abbiano effetto. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
PSN_APPLY 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contenente informazioni sul codice di notifica, incluso l'ID della pagina.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Impostare PSNRET \_ NOERROR per indicare che le modifiche apportate a questa pagina sono valide e sono state applicate. Se tutte le pagine impostano PSNRET \_ NOERROR, la finestra delle proprietà può essere eliminata definitivamente. Per indicare che le modifiche apportate a questa pagina non sono valide e per impedire che la finestra delle proprietà venga distrutta, impostare uno dei valori restituiti seguenti:

-   PSNRET \_ non valido. La finestra delle proprietà non verrà eliminata definitivamente e lo stato attivo verrà restituito a questa pagina.
-   \_NOCHANGEPAGE PSNRET non valido \_ . La finestra delle proprietà non verrà eliminata definitivamente e lo stato attivo verrà restituito alla pagina con lo stato attivo quando è stato premuto il pulsante.

Per impostare il valore restituito, la routine della finestra di dialogo per la pagina deve chiamare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il \_ valore MSGRESULT di DWL e la routine della finestra di dialogo deve restituire **true**.

## <a name="remarks"></a>Commenti

Quando l'utente fa clic sul pulsante OK, applica o Chiudi, la finestra delle proprietà Invia una notifica [ \_ KILLACTIVE PSN](psn-killactive.md) alla pagina attiva, offrendo la possibilità di convalidare le modifiche apportate dall'utente. Se le modifiche sono valide, la finestra delle proprietà Invia un \_ codice di notifica di applicazione PSN a ogni pagina, indirizzando l'applicazione alle nuove proprietà all'elemento corrispondente.

> [!Note]  
> La finestra delle proprietà è in corso di modifica dell'elenco di pagine quando \_ viene inviato il codice di notifica dell'applicazione PSN. Non tentare di aggiungere, rimuovere o inserire pagine durante la gestione della notifica. In questo modo si otterranno risultati imprevedibili.

 

Il membro **lParam** della struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) a cui punta *lParam* è impostato su **true** se l'utente fa clic sul pulsante OK. Viene inoltre impostata su **true** se il messaggio [**PSM \_ CANCELTOCLOSE**](psm-canceltoclose.md) è stato inviato e l'utente fa clic sul pulsante Chiudi. Viene impostato su **false** se l'utente fa clic sul pulsante Applica.

La struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà.

Non chiamare la funzione [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) durante l'elaborazione del codice di notifica.

Una finestra delle proprietà modale viene distrutta se l'utente fa clic sul pulsante OK e ogni pagina restituisce il \_ valore PSNRET NOERROR in risposta a **PSN \_ Apply**. Se una pagina restituisce PSNRET \_ non valido o \_ PSNRET \_ NOCHANGEPAGE non valido, il processo Apply viene annullato immediatamente. Le pagine dopo la pagina di annullamento non riceveranno un codice di notifica per l'applicazione di PSN \_ .

Per ricevere il codice di notifica, una pagina deve impostare il \_ valore DWL MSGRESULT su **false** in risposta al codice di notifica [ \_ KILLACTIVE di PSN](psn-killactive.md) .

> [!Note]  
> Questo codice di notifica non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

