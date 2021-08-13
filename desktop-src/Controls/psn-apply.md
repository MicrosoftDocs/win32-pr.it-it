---
title: PSN_APPLY codice di notifica (Prsht.h)
description: Inviato a ogni pagina nella finestra delle proprietà per indicare che l'utente ha fatto clic sul pulsante OK, Chiudi o Applica e vuole che tutte le modifiche appartienino effettive. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 18da6bdb-9409-49b6-8116-580fedd99a02
keywords:
- PSN_APPLY codice di notifica Windows controlli
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
ms.openlocfilehash: 522d4a0ea52f4cee495e689e8f0cdc91d7362ec3a1ee37ab81a911bc980d3209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410037"
---
# <a name="psn_apply-notification-code"></a>Codice di notifica \_ PSN APPLY

Inviato a ogni pagina nella finestra delle proprietà per indicare che l'utente ha fatto clic sul pulsante OK, Chiudi o Applica e vuole che tutte le modifiche appartienino effettive. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_APPLY 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) che contiene informazioni sul codice di notifica, incluso l'ID della pagina.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Impostare PSNRET NOERROR per indicare che le modifiche apportate a questa pagina sono \_ valide e sono state applicate. Se tutte le pagine impostano PSNRET \_ NOERROR, la finestra delle proprietà può essere distrutta. Per indicare che le modifiche apportate a questa pagina non sono valide e per impedire l'eliminazione della finestra delle proprietà, impostare uno dei valori restituiti seguenti:

-   PSNRET \_ NON VALIDO. La finestra delle proprietà non verrà distrutta e lo stato attivo verrà restituito a questa pagina.
-   PSNRET \_ \_ NOCHANGEPAGE NON VALIDO. La finestra delle proprietà non verrà distrutta e lo stato attivo verrà restituito alla pagina con lo stato attivo quando è stato premuto il pulsante.

Per impostare il valore restituito, la routine della finestra di dialogo per la pagina deve chiamare la [**funzione SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il valore MSGRESULT DWL e la routine della finestra di dialogo deve \_ restituire **TRUE.**

## <a name="remarks"></a>Commenti

Quando l'utente fa clic sul pulsante OK, Applica o Chiudi, la finestra delle proprietà invia una notifica [PSN \_ KILLACTIVE](psn-killactive.md) alla pagina attiva, offrendo la possibilità di convalidare le modifiche dell'utente. Se le modifiche sono valide, la finestra delle proprietà invia un codice di notifica PSN APPLY a ogni pagina, indirizzando l'applicazione delle nuove proprietà \_ all'elemento corrispondente.

> [!Note]  
> La finestra delle proprietà è in corso di modifica dell'elenco di pagine quando viene inviato il codice di notifica PSN \_ APPLY. Non tentare di aggiungere, rimuovere o inserire pagine durante la gestione di questa notifica. Questa operazione avrà risultati imprevedibili.

 

Il **membro lParam** della struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) a cui punta *lParam* è impostato su **TRUE** se l'utente fa clic sul pulsante OK. Viene inoltre impostato su **TRUE se** è stato inviato il [**messaggio PSM \_ CANCELTOCLOSE**](psm-canceltoclose.md) e l'utente fa clic sul pulsante Chiudi. È impostato su **FALSE se** l'utente fa clic sul pulsante Applica.

La [**struttura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contiene una [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **hdr**. Il **membro hwndFrom** di questa **struttura NMHDR** contiene l'handle per la finestra delle proprietà.

Non chiamare la funzione [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) durante l'elaborazione di questo codice di notifica.

Una finestra delle proprietà modale viene distrutta se l'utente fa clic sul pulsante OK e ogni pagina restituisce il valore PSNRET NOERROR in risposta a \_ **PSN \_ APPLY.** Se una pagina restituisce PSNRET \_ INVALID o PSNRET \_ INVALID \_ NOCHANGEPAGE, il processo Apply viene annullato immediatamente. Le pagine successive alla pagina di annullamento non riceveranno un codice di notifica PSN \_ APPLY.

Per ricevere questo codice di notifica, una pagina deve impostare il valore DWL MSGRESULT su FALSE in risposta al codice di notifica \_ [PSN \_ KILLACTIVE.](psn-killactive.md) 

> [!Note]  
> Questo codice di notifica non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

