---
title: Codice di notifica TBN_HOTITEMCHANGE (COMmctrl. h)
description: Inviato da un controllo Toolbar quando viene modificato l'elemento attivo (evidenziato). Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 49e68e2a-d9c0-463d-954d-34c9adfad62b
keywords:
- Controlli di Windows per il codice di notifica TBN_HOTITEMCHANGE
topic_type:
- apiref
api_name:
- TBN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d314a7250128a0f3e6b3fed54e5765487619d8e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739890"
---
# <a name="tbn_hotitemchange-notification-code"></a>\_Codice di notifica HOTITEMCHANGE di TBN

Inviato da un controllo Toolbar quando viene modificato l'elemento attivo (evidenziato). Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TBN_HOTITEMCHANGE

    lpnmhi = (LPNMTBHOTITEM) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) che contiene informazioni su questo codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero per consentire l'evidenziazione dell'elemento o un valore diverso da zero per impedire che l'elemento venga evidenziato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





