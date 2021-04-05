---
title: Codice di notifica CBEN_DELETEITEM (COMmctrl. h)
description: Inviato quando un elemento è stato eliminato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 8b0d03ff-57fa-44dc-ab3e-05089b876e3c
keywords:
- Controlli di Windows per il codice di notifica CBEN_DELETEITEM
topic_type:
- apiref
api_name:
- CBEN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c7ca7329898c9dd0c6bba76cba9d3524b017e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874425"
---
# <a name="cben_deleteitem-notification-code"></a>\_Codice di notifica DeleteItem di CBEN

Inviato quando un elemento è stato eliminato. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
CBEN_DELETEITEM

    pCBEx = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) contenente informazioni sul codice di notifica e sull'elemento eliminato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'elaborazione dell'applicazione del codice di notifica deve restituire zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





