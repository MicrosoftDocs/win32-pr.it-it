---
title: Codice di notifica PSN_SETACTIVE (Prsht. h)
description: Notifica a una pagina che sta per essere attivata. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463
keywords:
- Controlli di Windows per il codice di notifica PSN_SETACTIVE
topic_type:
- apiref
api_name:
- PSN_SETACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f38db77c1c60ef60ce713d41a6112b42235b79a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964468"
---
# <a name="psn_setactive-notification-code"></a>\_Codice di notifica SEATTIVO PSN

Notifica a una pagina che sta per essere attivata. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
PSN_SETACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contenente informazioni sul codice di notifica. Questa struttura contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà. Il membro **lParam** della struttura **PSHNOTIFY** non contiene informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero per accettare l'attivazione oppure-1 per attivare la pagina successiva o precedente (a seconda che l'utente abbia fatto clic sul pulsante **Avanti** o **indietro** ). Per impostare l'attivazione su una pagina specifica, restituire l'identificatore di risorsa della pagina.

## <a name="remarks"></a>Commenti

Il \_ codice di notifica SEATTIVO PSN viene inviato prima che la pagina sia visibile. Un'applicazione può usare questo codice di notifica per inizializzare i dati nella pagina.

> [!Note]  
> La finestra delle proprietà è in corso di modifica dell'elenco di pagine quando \_ viene inviato il codice di notifica SEATTIVO PSN. Non tentare di aggiungere, rimuovere o inserire pagine durante la gestione del codice di notifica. In questo modo si otterranno risultati imprevedibili.

 

Per impostare il valore restituito, la routine della finestra di dialogo per la pagina deve utilizzare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il \_ valore MSGRESULT di DWL e la routine della finestra di dialogo deve restituire **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

