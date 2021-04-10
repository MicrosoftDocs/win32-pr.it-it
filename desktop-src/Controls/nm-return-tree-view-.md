---
title: Codice di notifica di NM_RETURN (visualizzazione albero) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che il controllo ha lo stato attivo per l'input e che l'utente ha premuto il tasto. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: e4a048ec-4643-458a-bf75-f5b08163d6c6
keywords:
- NM_RETURN (visualizzazione albero) controlli di Windows per il codice di notifica
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a0abf3152a9236103301f1c74acfcac69d43f07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964643"
---
# <a name="nm_return-tree-view-notification-code"></a>\_Codice di notifica restituito da Nm (visualizzazione albero)

Notifica alla finestra padre di un controllo di visualizzazione albero che il controllo ha lo stato attivo per l'input e che l'utente ha premuto il tasto. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_RETURN

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero per impedire l'elaborazione predefinita oppure zero per consentire l'elaborazione predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





