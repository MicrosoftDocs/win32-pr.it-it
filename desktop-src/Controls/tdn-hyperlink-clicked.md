---
title: TDN_HYPERLINK_CLICKED di notifica (Commctrl.h)
description: Inviato da una finestra di dialogo attività quando l'utente fa clic su un collegamento ipertestuale nel contenuto della finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il metodo TaskDialogIndirect.
ms.assetid: b769af31-32d0-463e-be15-6abf5dcb425c
keywords:
- TDN_HYPERLINK_CLICKED del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TDN_HYPERLINK_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0adaf5ecf05b22e3ff33aa88e28cb3f8f8c8b78f0b06d2127792b7639942bf7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875771"
---
# <a name="tdn_hyperlink_clicked-notification-code"></a>Codice di notifica TDN \_ HYPERLINK \_ CLICKED

Inviato da una finestra di dialogo attività quando l'utente fa clic su un collegamento ipertestuale nel contenuto della finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il [**metodo TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)


```C++
TDN_HYPERLINK_CLICKED

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

Puntatore a una stringa di caratteri wide contenente l'URL del collegamento ipertestuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





