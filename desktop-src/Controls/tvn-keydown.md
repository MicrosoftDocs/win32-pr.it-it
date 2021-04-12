---
title: Codice di notifica TVN_KEYDOWN (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che l'utente ha premuto una chiave e che il controllo di visualizzazione albero ha lo stato attivo per l'input. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: da0d2b62-2295-4dce-9b37-a250f3be087f
keywords:
- Controlli di Windows per il codice di notifica TVN_KEYDOWN
topic_type:
- apiref
api_name:
- TVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ccb18c3bf7dc03056abb55575850821e11eb9bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475124"
---
# <a name="tvn_keydown-notification-code"></a>Codice di notifica di TVN \_ KeyDown

Notifica alla finestra padre di un controllo di visualizzazione albero che l'utente ha premuto una chiave e che il controllo di visualizzazione albero ha lo stato attivo per l'input. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TVN_KEYDOWN 

    ptvkd = (LPNMTVKEYDOWN) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) . Il membro **wVKey** specifica il codice della chiave virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il membro **wVKey** di *lParam* è un codice del tasto carattere, il carattere verrà utilizzato come parte di una ricerca incrementale. Restituisce un valore diverso da zero per escludere il carattere dalla ricerca incrementale oppure zero per includere il carattere nella ricerca. Per tutte le altre chiavi, il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





