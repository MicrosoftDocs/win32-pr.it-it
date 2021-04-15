---
title: Codice di notifica TBN_DRAGOVER (COMmctrl. h)
description: Verifica se \_ deve essere inviato un messaggio TB MARKBUTTON per un pulsante trascinato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- Controlli di Windows per il codice di notifica TBN_DRAGOVER
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa02aa8fabf89ea27fce628d3d63165255bbd66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475904"
---
# <a name="tbn_dragover-notification-code"></a>Codice di notifica di TBN \_ DRAGOVER

Verifica se deve essere inviato un messaggio [**TB \_ MARKBUTTON**](tb-markbutton.md) per un pulsante trascinato. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) che specifica l'elemento da trascinare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**False** se la barra degli strumenti deve inviare un \_ messaggio TB MARKBUTTON; in caso contrario **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





