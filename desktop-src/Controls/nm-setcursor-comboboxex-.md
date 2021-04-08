---
title: Codice di notifica di NM_SETCURSOR (ComboBoxEx) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo ComboBoxEx che il controllo sta impostando il cursore in risposta a un \_ messaggio del cursore WM. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: a1c617fa-8eb2-444f-88d1-9913de7a42d1
keywords:
- NM_SETCURSOR (ComboBoxEx) (codice di notifica) controlli Windows
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbd5e10f06e74af0778521d31c69e63586a6476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742666"
---
# <a name="nm_setcursor-comboboxex-notification-code"></a>\_Codice di notifica del SECURSORE Nm (ComboBoxEx)

Notifica alla finestra padre di un controllo ComboBoxEx che il controllo sta impostando il cursore in risposta a un messaggio del [**\_ cursore WM**](/windows/desktop/menurc/wm-setcursor) . Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero per consentire al controllo di impostare il cursore o un valore diverso da zero per impedire al controllo di impostare il cursore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

