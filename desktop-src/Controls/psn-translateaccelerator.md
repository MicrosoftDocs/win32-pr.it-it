---
title: Codice di notifica PSN_TRANSLATEACCELERATOR (Prsht. h)
description: Notifica a una finestra delle proprietà che è stato ricevuto un messaggio da tastiera. Fornisce alla pagina la possibilità di eseguire la conversione dell'acceleratore di tastiera privata. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 04d67326-92f9-4b92-a27e-354815f3c1a8
keywords:
- Controlli di Windows per il codice di notifica PSN_TRANSLATEACCELERATOR
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
ms.openlocfilehash: 9dc86866be1154bbd0ef1cf76b3535b7b02496e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301016"
---
# <a name="psn_translateaccelerator-notification-code"></a>\_Codice di notifica TRANSLATEACCELERATOR PSN

Notifica a una finestra delle proprietà che è stato ricevuto un messaggio da tastiera. Fornisce alla pagina la possibilità di eseguire la conversione dell'acceleratore di tastiera privata. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
PSN_TRANSLATEACCELERATOR 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) che contiene informazioni sul codice di notifica. Questa struttura contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà. Il membro **lParam** della struttura **PSHNOTIFY** è un puntatore al [**msg**](/windows/win32/api/winuser/ns-winuser-msg)del messaggio. È possibile eseguire il cast a un tipo **lpMsg** per ottenere l'accesso ai parametri del messaggio da tradurre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce PSNRET \_ MESSAGEHANDLED per indicare che non è necessaria alcuna ulteriore elaborazione. Restituisce PSNRET \_ NOERROR per richiedere l'elaborazione normale.

## <a name="remarks"></a>Commenti

Per impostare il valore restituito, la routine della finestra di dialogo per la pagina deve utilizzare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il \_ valore DWL MSGRESULT. La routine della finestra di dialogo deve restituire **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

