---
title: Codice di notifica PSN_QUERYINITIALFOCUS (Prsht. h)
description: Inviato da una finestra delle proprietà per fornire una pagina della finestra delle proprietà la possibilità di specificare quale controllo finestra di dialogo deve ricevere lo stato attivo iniziale. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 29b5e598-75b2-4b6f-acdb-171b1f7a1850
keywords:
- Controlli di Windows per il codice di notifica PSN_QUERYINITIALFOCUS
topic_type:
- apiref
api_name:
- PSN_QUERYINITIALFOCUS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc542332440009f6564f384b415657e725edda00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119079"
---
# <a name="psn_queryinitialfocus-notification-code"></a>\_Codice di notifica QUERYINITIALFOCUS PSN

Inviato da una finestra delle proprietà per fornire una pagina della finestra delle proprietà la possibilità di specificare quale controllo finestra di dialogo deve ricevere lo stato attivo iniziale. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
PSN_QUERYINITIALFOCUS

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) . Eseguire il cast del membro **lParam** di questa struttura in un tipo **HWND** per recuperare l'handle del controllo a cui verrà assegnato lo stato attivo per impostazione predefinita. La struttura contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per specificare quale controllo deve ricevere lo stato attivo, restituire l'handle del controllo. In caso contrario, restituirà zero e lo stato attivo passerà al controllo predefinito. Per impostare il valore restituito, è necessario che la routine della finestra di dialogo chiami la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con un valore **\_ MSGRESULT DWL** e restituisca **true**.

## <a name="remarks"></a>Commenti

Un'applicazione non deve chiamare la funzione [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) durante la gestione del codice di notifica. Restituisce l'handle del controllo che deve ricevere lo stato attivo e il gestore della finestra delle proprietà gestirà la modifica dello stato attivo.

Il \_ codice di notifica QUERYINITIALFOCUS PSN non viene inviato se il gestore della finestra delle proprietà determina che nessun controllo nella pagina deve ricevere lo stato attivo.

Questo frammento di codice implementa un semplice gestore per PSN \_ QUERYINITIALFOCUS. Richiede che lo stato attivo iniziale venga assegnato al controllo location (**\_ posizione IDC**).

``` syntax
case PSN_QUERYINITIALFOCUS :
    SetWindowLong(hDlg,DWL_MSGRESULT, (LPARAM)GetDlgItem(hDlg, IDC_LOCATION));
    return TRUE;
...
```

> [!Note]  
> Questo codice di notifica non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

