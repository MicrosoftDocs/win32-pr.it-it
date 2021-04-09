---
title: Codice di notifica di NM_RELEASEDCAPTURE (TrackBar) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo TrackBar che il controllo sta rilasciando l'acquisizione del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 1e3e4f67-672d-4e3e-84f4-b3fa6221d118
keywords:
- Codice di notifica di NM_RELEASEDCAPTURE (TrackBar)-controlli Windows
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
ms.openlocfilehash: 684f58fb5328cfe0d25fc73ce7c1a2d9a189d86f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120714"
---
# <a name="nm_releasedcapture-trackbar-notification-code"></a>Codice di notifica di NM \_ RELEASEDCAPTURE (TrackBar)

Notifica alla finestra padre di un controllo TrackBar che il controllo sta rilasciando l'acquisizione del mouse. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


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

Il controllo Ignora il valore restituito da questo codice di notifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





