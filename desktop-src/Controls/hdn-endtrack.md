---
title: Codice di notifica HDN_ENDTRACK (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che l'utente ha terminato il trascinamento di un divisore. Questo codice di notifica è stato inviato sotto forma di \_ messaggio di notifica WM.
ms.assetid: d9b25871-7bd6-439c-91b8-e8249d9be67d
keywords:
- Controlli di Windows per il codice di notifica HDN_ENDTRACK
topic_type:
- apiref
api_name:
- HDN_ENDTRACK
- HDN_ENDTRACKA
- HDN_ENDTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ab7625690a2de0414f1da391f26f919c1c2617
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047938"
---
# <a name="hdn_endtrack-notification-code"></a>\_Codice di notifica ENDTRACK di HDN

Notifica alla finestra padre di un controllo di intestazione che l'utente ha terminato il trascinamento di un divisore. Questo codice di notifica è stato inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
HDN_ENDTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenente informazioni sul controllo intestazione e sull'elemento il cui divisore è stato trascinato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HDN \_ ENDTRACKW** (Unicode) e **HDN \_ ENDTRACKA** (ANSI)<br/>                 |



 

 





