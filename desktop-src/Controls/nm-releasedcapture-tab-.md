---
title: Codice di notifica del NM_RELEASEDCAPTURE (scheda) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo struttura a schede che il controllo sta rilasciando l'acquisizione del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 17f87666-692c-4c2f-9ef5-6d2593e0de97
keywords:
- Codice di notifica di NM_RELEASEDCAPTURE (tabulazione) controlli di Windows
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad9c9049b63afb18413aea9fa77b7947e97e93b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477554"
---
# <a name="nm_releasedcapture-tab-notification-code"></a>\_Codice di notifica RELEASEDCAPTURE (TAB) Nm

Notifica alla finestra padre di un controllo struttura a schede che il controllo sta rilasciando l'acquisizione del mouse. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





