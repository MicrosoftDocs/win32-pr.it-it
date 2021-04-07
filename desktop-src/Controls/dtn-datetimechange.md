---
title: Codice di notifica DTN_DATETIMECHANGE (COMmctrl. h)
description: Inviato da un controllo di selezione data e ora (DTP) ogni volta che viene apportata una modifica. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 65cdd8fb-1f07-4447-b503-d40fdfa37202
keywords:
- Controlli di Windows per il codice di notifica DTN_DATETIMECHANGE
topic_type:
- apiref
api_name:
- DTN_DATETIMECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40072a54732a0a3575e3153ddb901ca1df291b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874166"
---
# <a name="dtn_datetimechange-notification-code"></a>\_Codice di notifica DATETIMECHANGE di DTN

Inviato da un controllo di selezione data e ora (DTP) ogni volta che viene apportata una modifica. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
DTN_DATETIMECHANGE

    lpChange = (LPNMDATETIMECHANGE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) contenente informazioni sulla modifica che ha avuto luogo nel controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il proprietario del controllo deve restituire zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





