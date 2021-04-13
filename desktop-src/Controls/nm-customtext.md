---
title: Codice di notifica NM_CUSTOMTEXT (COMmctrl. h)
description: Notifica alla finestra padre di un controllo informazioni sulle operazioni di testo personalizzate. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b4bde648-3479-4fac-ad32-b34c7272c1fc
keywords:
- Controlli di Windows per il codice di notifica NM_CUSTOMTEXT
topic_type:
- apiref
api_name:
- NM_CUSTOMTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eebc4033a76d137e28a0c4170c5c613c7933562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400226"
---
# <a name="nm_customtext-notification-code"></a>\_Codice di notifica CUSTOMTEXT Nm

Notifica alla finestra padre di un controllo informazioni sulle operazioni di testo personalizzate. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_CUSTOMTEXT

    lpnmct = (NMCUSTOMTEXT) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMCUSTOMTEXT**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato dal controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





