---
title: Codice di notifica CBEN_INSERTITEM (COMmctrl. h)
description: Inviato quando un nuovo elemento è stato inserito nel controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: caf60156-10d2-4cfb-91c4-def6ee99c471
keywords:
- Controlli di Windows per il codice di notifica CBEN_INSERTITEM
topic_type:
- apiref
api_name:
- CBEN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63ccd05ea75015479ef32415d920bbe639664ac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743818"
---
# <a name="cben_insertitem-notification-code"></a>Codice di notifica di CBEN \_ INSERTITEM

Inviato quando un nuovo elemento è stato inserito nel controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
CBEN_INSERTITEM

    pNMInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) contenente informazioni sul codice di notifica e sull'elemento inserito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'elaborazione dell'applicazione del codice di notifica deve restituire zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





