---
title: PSN_KILLACTIVE di notifica (Prsht.h)
description: Notifica a una pagina che sta per perdere l'attivazione perché è in corso l'attivazione di un'altra pagina o l'utente ha fatto clic sul pulsante OK. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 470cd6ff-73ad-451a-a861-4d3324a8a8db
keywords:
- PSN_KILLACTIVE del codice di notifica Windows controlli
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
ms.openlocfilehash: 5eaf1a5221e186ebe5f01f942ec99d82906ea87ef7f1b8f73860bade24ab1751
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169651"
---
# <a name="psn_killactive-notification-code"></a>Codice di notifica KILLACTIVE psn \_

Notifica a una pagina che sta per perdere l'attivazione perché è in corso l'attivazione di un'altra pagina o l'utente ha fatto clic sul pulsante OK. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_KILLACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) che contiene informazioni sul codice di notifica. Questa struttura contiene una [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **hdr**. Il **membro hwndFrom** di questa **struttura NMHDR** contiene l'handle per la finestra delle proprietà. Il **membro lParam** della **struttura PSHNOTIFY** non contiene informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** per impedire che la pagina perda l'attivazione o **FALSE** per consentirla.

## <a name="remarks"></a>Commenti

Un'applicazione gestisce questo codice di notifica per convalidare le informazioni immesse dall'utente.

> [!Note]  
> La finestra delle proprietà è in corso di modifica dell'elenco di pagine quando viene inviato il codice di notifica \_ KILLACTIVE psn. Non tentare di aggiungere, rimuovere o inserire pagine durante la gestione di questo codice di notifica. Questa operazione avrà risultati imprevedibili.

 

Per impostare un valore restituito, la routine della finestra di dialogo per la pagina deve chiamare la [**funzione SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con un valore MSGRESULT DWL impostato \_ sul valore restituito. La routine della finestra di dialogo deve restituire **TRUE.**

Se la procedura della finestra di dialogo imposta DWL MSGRESULT su TRUE, verrà visualizzata una finestra di messaggio per spiegare \_ il problema all'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

