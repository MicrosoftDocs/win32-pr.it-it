---
title: TDN_HELP di notifica (Commctrl.h)
description: Inviato da una finestra di dialogo attività quando l'utente preme F1 sulla tastiera mentre la finestra di dialogo ha lo stato attivo. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il metodo TaskDialogIndirect.
ms.assetid: 207ba231-639d-4906-b5dc-1592f2717f1c
keywords:
- TDN_HELP del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TDN_HELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5944fb136a76b880deb51b461a0e48b8d81ce2aca541cb6fa3717c3d79e9ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104461"
---
# <a name="tdn_help-notification-code"></a>Codice di notifica della \_ Guida TDN

Inviato da una finestra di dialogo attività quando l'utente preme F1 sulla tastiera mentre la finestra di dialogo ha lo stato attivo. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il [**metodo TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)


```C++
TDN_HELP
        
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
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





