---
title: Codice di notifica NM_RETURN (COMmctrl. h)
description: Notifica alla finestra padre di un controllo che il controllo ha lo stato attivo per l'input e che l'utente ha premuto il tasto INVIO. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 2c4839bc-6b23-469b-978f-cdf5f7bc0549
keywords:
- Controlli di Windows per il codice di notifica NM_RETURN
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
ms.openlocfilehash: 4c6cebd089873df5471c9b25710efafaab4d246f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518454"
---
# <a name="nm_return-notification-code"></a>\_Codice di notifica restituito da Nm

Notifica alla finestra padre di un controllo che il controllo ha lo stato attivo per l'input e che l'utente ha premuto il tasto INVIO. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


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

Il valore restituito viene ignorato dal controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





