---
title: Codice di notifica NM_LDOWN (COMmctrl. h)
description: Notifica alla finestra padre di un controllo che è stato premuto il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 59546fc3-f7c5-4b2d-9fd7-2ff89d72cd9f
keywords:
- Controlli di Windows per il codice di notifica NM_LDOWN
topic_type:
- apiref
api_name:
- NM_LDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d62d1570fc0c10ccb64ae6c1f9af6433025ec79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301018"
---
# <a name="nm_ldown-notification-code"></a>\_Codice di notifica LDOWN Nm

Notifica alla finestra padre di un controllo che è stato premuto il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_LDOWN

   lpnmhdr = (LPNMHDR) lParam;
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
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





