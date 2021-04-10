---
title: Codice di notifica PSN_QUERYCANCEL (Prsht. h)
description: Indica che l'utente ha annullato la finestra delle proprietà. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 4a789e08-065a-485c-87e3-f7958e2dc544
keywords:
- Controlli di Windows per il codice di notifica PSN_QUERYCANCEL
topic_type:
- apiref
api_name:
- PSN_QUERYCANCEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27d39a7a02d80235db5f8fbe31809dcc913d51c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964111"
---
# <a name="psn_querycancel-notification-code"></a>\_Codice di notifica QUERYCANCEL PSN

Indica che l'utente ha annullato la finestra delle proprietà. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
PSN_QUERYCANCEL 

    lppsn = (LPPSHNOTIFY) lParam;  
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contenente informazioni sul codice di notifica. Questa struttura contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà. Il membro **lParam** della struttura **PSHNOTIFY** non contiene informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** per evitare l'operazione di annullamento o **false** per consentirne l'esecuzione.

## <a name="remarks"></a>Commenti

Questo codice di notifica viene in genere inviato quando un utente fa clic sul pulsante **Annulla** . Viene inoltre inviato quando un utente fa clic sul pulsante **X** nell'angolo superiore destro della finestra delle proprietà oppure preme il tasto di escape. Una pagina della finestra delle proprietà può gestire questo codice di notifica per richiedere all'utente di verificare l'operazione di annullamento.

Per impostare un valore restituito, la routine della finestra di dialogo per la pagina deve chiamare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con DWL \_ MSGRESULT impostato sul valore restituito. La routine della finestra di dialogo deve restituire **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

