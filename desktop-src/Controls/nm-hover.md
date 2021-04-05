---
title: Codice di notifica NM_HOVER (COMmctrl. h)
description: Inviato da un controllo quando il mouse viene spostato su un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0eef3e88-c1f0-4f9c-9ccf-580d8e464157
keywords:
- Controlli di Windows per il codice di notifica NM_HOVER
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69344b1aae78ebee99b86c78f4442df20f66187a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739927"
---
# <a name="nm_hover-notification-code"></a>\_Codice di notifica del passaggio del puntatore a Nm

Inviato da un controllo quando il mouse viene spostato su un elemento. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se non diversamente specificato, restituisce zero per consentire al controllo di elaborare normalmente il passaggio del mouse o un valore diverso da zero per impedire l'elaborazione del passaggio del mouse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





