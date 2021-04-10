---
title: Codice di notifica TBN_QUERYINSERT (COMmctrl. h)
description: Notifica alla finestra padre della barra degli strumenti se un pulsante può essere inserito a sinistra del pulsante specificato mentre l'utente sta personalizzando una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- Controlli di Windows per il codice di notifica TBN_QUERYINSERT
topic_type:
- apiref
api_name:
- TBN_QUERYINSERT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a21e9ade8f54ffe27ebffdfc2a8b535b4b3630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964853"
---
# <a name="tbn_queryinsert-notification-code"></a>\_Codice di notifica QUERYINSERT di TBN

Notifica alla finestra padre della barra degli strumenti se un pulsante può essere inserito a sinistra del pulsante specificato mentre l'utente sta personalizzando una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TBN_QUERYINSERT 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) . Il membro **iItem** contiene l'indice in base zero del pulsante da inserire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** per consentire l'inserimento di un pulsante davanti al pulsante specificato o **false** per impedire l'inserimento del pulsante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





