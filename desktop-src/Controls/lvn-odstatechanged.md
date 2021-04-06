---
title: Codice di notifica LVN_ODSTATECHANGED (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco quando lo stato di un elemento o di un intervallo di elementi è stato modificato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: a3aafda5-a3ec-4f84-8153-8d34097e04f1
keywords:
- Controlli di Windows per il codice di notifica LVN_ODSTATECHANGED
topic_type:
- apiref
api_name:
- LVN_ODSTATECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86de2f5e01e15d0a97c49f451914aac5b74b27e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742551"
---
# <a name="lvn_odstatechanged-notification-code"></a>\_Codice di notifica ODSTATECHANGED di LVN

Inviato da un controllo di visualizzazione elenco quando lo stato di un elemento o di un intervallo di elementi è stato modificato. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_ODSTATECHANGED

    lpStateChange = (LPNMLVODSTATECHANGE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLVODSTATECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange) che contiene informazioni sull'elemento o gli elementi che sono stati modificati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'applicazione che riceve il codice di notifica deve restituire zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





