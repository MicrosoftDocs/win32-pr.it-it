---
title: Codice di notifica NM_KEYDOWN (COMmctrl. h)
description: Inviato da un controllo quando il controllo ha lo stato attivo della tastiera e l'utente preme un tasto. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: e3b38096-797d-4948-9595-a252cf33dcdd
keywords:
- Controlli di Windows per il codice di notifica NM_KEYDOWN
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 222a47733a60590e7d56ca0adba038164c430fab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873298"
---
# <a name="nm_keydown-notification-code"></a>\_Codice di notifica KeyDown di Nm

Inviato da un controllo quando il controllo ha lo stato attivo della tastiera e l'utente preme un tasto. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) che contiene informazioni aggiuntive sulla chiave che ha causato il codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero per impedire l'elaborazione della chiave da parte del controllo. in caso contrario, zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





