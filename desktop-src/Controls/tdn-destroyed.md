---
title: Codice di notifica TDN_DESTROYED (COMmctrl. h)
description: Inviato da una finestra di dialogo attività quando viene eliminato definitivamente e il relativo handle di finestra non è più valido. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo TaskDialogIndirect.
ms.assetid: bbebb77f-e078-46bf-a42d-65dab4f8a972
keywords:
- Controlli di Windows per il codice di notifica TDN_DESTROYED
topic_type:
- apiref
api_name:
- TDN_DESTROYED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d3da93435371e696de3d4dce8deeea43926b73b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874562"
---
# <a name="tdn_destroyed-notification-code"></a>TDN \_ codice di notifica distrutto

Inviato da una finestra di dialogo attività quando viene eliminato definitivamente e il relativo handle di finestra non è più valido. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .


```C++
TDN_DESTROYED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





