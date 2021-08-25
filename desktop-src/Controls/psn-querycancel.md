---
title: PSN_QUERYCANCEL codice di notifica (Prsht.h)
description: Indica che l'utente ha annullato la finestra delle proprietà. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 4a789e08-065a-485c-87e3-f7958e2dc544
keywords:
- PSN_QUERYCANCEL codice di notifica Windows controlli
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
ms.openlocfilehash: bff5ed6203d255a18c40044febb2f7afd9ab42e15c5a9d8ae9fa1a1a56518693
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798621"
---
# <a name="psn_querycancel-notification-code"></a>Codice di notifica \_ PSN QUERYCANCEL

Indica che l'utente ha annullato la finestra delle proprietà. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_QUERYCANCEL 

    lppsn = (LPPSHNOTIFY) lParam;  
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) che contiene informazioni sul codice di notifica. Questa struttura contiene una [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **hdr**. Il **membro hwndFrom** di questa **struttura NMHDR** contiene l'handle per la finestra delle proprietà. Il **membro lParam** della **struttura PSHNOTIFY** non contiene informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** per impedire l'operazione di annullamento o **FALSE** per consentirla.

## <a name="remarks"></a>Commenti

Questo codice di notifica viene in genere inviato quando un utente fa clic sul **pulsante** Annulla. Viene inviato anche quando un utente fa clic sul **pulsante X** nell'angolo superiore destro della finestra delle proprietà o preme il tasto ESCAPE. Una pagina della finestra delle proprietà può gestire questo codice di notifica per chiedere all'utente di verificare l'operazione di annullamento.

Per impostare un valore restituito, la routine della finestra di dialogo per la pagina deve chiamare la [**funzione SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con DWL \_ MSGRESULT impostato sul valore restituito. La routine della finestra di dialogo deve restituire **TRUE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

