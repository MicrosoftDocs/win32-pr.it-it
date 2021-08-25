---
title: TDN_DESTROYED di notifica (Commctrl.h)
description: Inviato da una finestra di dialogo attività quando viene eliminato e il relativo handle di finestra non è più valido. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il metodo TaskDialogIndirect.
ms.assetid: bbebb77f-e078-46bf-a42d-65dab4f8a972
keywords:
- TDN_DESTROYED del codice di notifica Windows controlli
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
ms.openlocfilehash: cad0bb08d8d3693f7e9168454526306b3d1d8643431ba16d851e9c259cfd0580
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875801"
---
# <a name="tdn_destroyed-notification-code"></a>Codice di notifica TDN \_ DESTROYED

Inviato da una finestra di dialogo attività quando viene eliminato e il relativo handle di finestra non è più valido. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il [**metodo TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)


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
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





