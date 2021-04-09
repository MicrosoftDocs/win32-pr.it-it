---
title: Codice di notifica PSN_KILLACTIVE (Prsht. h)
description: Notifica a una pagina che sta per perdere l'attivazione perché è in corso l'attivazione di un'altra pagina o se l'utente ha fatto clic sul pulsante OK. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 470cd6ff-73ad-451a-a861-4d3324a8a8db
keywords:
- Controlli di Windows per il codice di notifica PSN_KILLACTIVE
topic_type:
- apiref
api_name:
- PSN_KILLACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae5f90670c79797ef8576c5e6e3911255ab5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964113"
---
# <a name="psn_killactive-notification-code"></a>\_Codice di notifica KILLACTIVE PSN

Notifica a una pagina che sta per perdere l'attivazione perché è in corso l'attivazione di un'altra pagina o se l'utente ha fatto clic sul pulsante OK. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
PSN_KILLACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contenente informazioni sul codice di notifica. Questa struttura contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà. Il membro **lParam** della struttura **PSHNOTIFY** non contiene informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** per evitare che la pagina perda l'attivazione o **false** per consentirne l'attivazione.

## <a name="remarks"></a>Commenti

Un'applicazione gestisce questo codice di notifica per convalidare le informazioni immesse dall'utente.

> [!Note]  
> La finestra delle proprietà è in corso di modifica dell'elenco di pagine quando \_ viene inviato il codice di notifica KILLACTIVE PSN. Non tentare di aggiungere, rimuovere o inserire pagine durante la gestione del codice di notifica. In questo modo si otterranno risultati imprevedibili.

 

Per impostare un valore restituito, la routine della finestra di dialogo per la pagina deve chiamare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con un \_ valore DWL MSGRESULT impostato sul valore restituito. La routine della finestra di dialogo deve restituire **true**.

Se la routine della finestra di dialogo Imposta DWL \_ MSGRESULT su **true**, verrà visualizzata una finestra di messaggio per spiegare il problema all'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

