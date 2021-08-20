---
title: TDN_NAVIGATED codice di notifica (Commctrl.h)
description: Inviato da una finestra di dialogo attività quando si è verificato lo spostamento. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il metodo TaskDialogIndirect.
ms.assetid: e7668ab3-3a11-4bf4-8cb4-067d3204fb3f
keywords:
- TDN_NAVIGATED codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TDN_NAVIGATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ee3daa29fa0f85db2dfb2a5991e0db9c9dba46938e69ad8d16153a97d400284
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166894"
---
# <a name="tdn_navigated-notification-code"></a>Codice di notifica \_ TDN NAVIGATED

Inviato da una finestra di dialogo attività quando si è verificato lo spostamento. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il [**metodo TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)


```C++
TDN_NAVIGATED
     
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
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





