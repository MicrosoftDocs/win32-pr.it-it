---
title: Codice di notifica TBN_QUERYDELETE (COMmctrl. h)
description: Notifica alla finestra padre della barra degli strumenti se un pulsante può essere eliminato da una barra degli strumenti mentre l'utente personalizza la barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- Controlli di Windows per il codice di notifica TBN_QUERYDELETE
topic_type:
- apiref
api_name:
- TBN_QUERYDELETE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a416545ecf7ad8562c1327160d683a109eccb3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517361"
---
# <a name="tbn_querydelete-notification-code"></a>\_Codice di notifica QUERYDELETE di TBN

Notifica alla finestra padre della barra degli strumenti se un pulsante può essere eliminato da una barra degli strumenti mentre l'utente personalizza la barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TBN_QUERYDELETE 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) . Il membro **iItem** contiene l'indice in base zero del pulsante da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** per consentire l'eliminazione del pulsante o **false** per impedire che il pulsante venga eliminato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





