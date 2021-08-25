---
title: PSN_TRANSLATEACCELERATOR codice di notifica (Prsht.h)
description: Notifica a una finestra delle proprietà che è stato ricevuto un messaggio della tastiera. Offre alla pagina l'opportunità di eseguire la traduzione privata dell'acceleratore di tastiera. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 04d67326-92f9-4b92-a27e-354815f3c1a8
keywords:
- PSN_TRANSLATEACCELERATOR codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- PSN_TRANSLATEACCELERATOR
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ca25ed7dd2a2fa2b11e0854f7fe9e4bb4afb9aa47ec52c21bc1c6e346ebf16d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914491"
---
# <a name="psn_translateaccelerator-notification-code"></a>Codice di \_ notifica PSN TRANSLATEACCELERATOR

Notifica a una finestra delle proprietà che è stato ricevuto un messaggio della tastiera. Offre alla pagina l'opportunità di eseguire la traduzione privata dell'acceleratore di tastiera. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_TRANSLATEACCELERATOR 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) che contiene informazioni sul codice di notifica. Questa struttura contiene una [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **hdr**. Il **membro hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà. Il **membro lParam** della **struttura PSHNOTIFY** è un puntatore al messaggio [**MSG**](/windows/win32/api/winuser/ns-winuser-msg). È possibile eseguire il cast a un **tipo LPMSG** per ottenere l'accesso ai parametri del messaggio da convertire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce PSNRET \_ MESSAGEHANDLED per indicare che non sono necessarie ulteriori elaborazioni. Restituisce PSNRET \_ NOERROR per richiedere una normale elaborazione.

## <a name="remarks"></a>Commenti

Per impostare il valore restituito, la routine della finestra di dialogo per la pagina deve usare la [**funzione SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il valore \_ MSGRESULT DWL. La routine della finestra di dialogo deve restituire **TRUE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

