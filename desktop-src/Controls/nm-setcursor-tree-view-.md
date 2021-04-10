---
title: Codice di notifica di NM_SETCURSOR (visualizzazione albero) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che il controllo sta impostando il cursore in risposta a un \_ messaggio del cursore WM. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 2b2f2e90-edef-484d-b67a-12983a1cde29
keywords:
- NM_SETCURSOR (visualizzazione albero) controlli di Windows per il codice di notifica
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40b733e32c72abc9620e0fd18a6ef554aee9214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964642"
---
# <a name="nm_setcursor-tree-view-notification-code"></a>\_Codice di notifica del cursore Nm (visualizzazione albero)

Notifica alla finestra padre di un controllo di visualizzazione albero che il controllo sta impostando il cursore in risposta a un messaggio del [**\_ cursore WM**](/windows/desktop/menurc/wm-setcursor) . Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero per consentire al controllo di impostare il cursore o un valore diverso da zero per impedire al controllo di impostare il cursore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

