---
title: PSN_QUERYINITIALFOCUS codice di notifica (Prsht.h)
description: Inviato da una finestra delle proprietà per fornire a una pagina della finestra delle proprietà la possibilità di specificare quale controllo della finestra di dialogo deve ricevere lo stato attivo iniziale. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 29b5e598-75b2-4b6f-acdb-171b1f7a1850
keywords:
- PSN_QUERYINITIALFOCUS codice di notifica Windows controlli
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
ms.openlocfilehash: ffc82fe11893e728fbc9301868d9acdca5f7110bedfd37b4a16b473de0821f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169641"
---
# <a name="psn_queryinitialfocus-notification-code"></a>Codice di notifica \_ QUERYINITIALFOCUS PSN

Inviato da una finestra delle proprietà per fornire a una pagina della finestra delle proprietà la possibilità di specificare quale controllo della finestra di dialogo deve ricevere lo stato attivo iniziale. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_QUERYINITIALFOCUS

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura PSHNOTIFY.**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) Eseguire il cast del membro **lParam** di questa struttura a un **tipo HWND** per recuperare l'handle del controllo a cui verrà assegnato lo stato attivo per impostazione predefinita. La struttura contiene [**una struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **hdr**. Il **membro hwndFrom** di questa **struttura NMHDR** contiene l'handle per la finestra delle proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per specificare quale controllo deve ricevere lo stato attivo, restituire l'handle del controllo. In caso contrario, restituisce zero e lo stato attivo passa al controllo predefinito. Per impostare il valore restituito, la routine della finestra di dialogo deve chiamare la [**funzione SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con un **valore \_ MSGRESULT DWL** e restituire **TRUE.**

## <a name="remarks"></a>Commenti

Un'applicazione non deve chiamare la [**funzione SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) durante la gestione di questo codice di notifica. Restituisce l'handle del controllo che deve ricevere lo stato attivo e il gestore della finestra delle proprietà gestirà la modifica dello stato attivo.

Il codice di notifica PSN QUERYINITIALFOCUS non viene inviato se il gestore della finestra delle proprietà determina che nessun controllo nella \_ pagina deve ricevere lo stato attivo.

Questo frammento di codice implementa un gestore semplice per PSN \_ QUERYINITIALFOCUS. Richiede che lo stato attivo iniziale sia assegnato al controllo Posizione (**IDC \_ LOCATION**).

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
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

