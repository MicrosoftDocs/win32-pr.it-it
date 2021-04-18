---
title: Codice di notifica MCN_VIEWCHANGE (COMmctrl. h)
description: Inviato da un controllo di calendario mensile quando cambia la visualizzazione corrente. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ee35ac1d-9aeb-4d75-9cef-016487f23602
keywords:
- Controlli di Windows per il codice di notifica MCN_VIEWCHANGE
topic_type:
- apiref
api_name:
- MCN_VIEWCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbcad3fdda355ac2795dbe49a89fa4e7c2c5cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475550"
---
# <a name="mcn_viewchange-notification-code"></a>\_Codice di notifica VIEWCHANGE di MCN

Inviato da un controllo di calendario mensile quando cambia la visualizzazione corrente. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
MCN_VIEWCHANGE

    lpNMViewChange = (LPNMVIEWCHANGE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) contenente informazioni sulla visualizzazione corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





