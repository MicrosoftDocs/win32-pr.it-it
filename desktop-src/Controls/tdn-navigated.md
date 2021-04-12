---
title: Codice di notifica TDN_NAVIGATED (COMmctrl. h)
description: Inviato da una finestra di dialogo attività quando si è verificata la navigazione. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo TaskDialogIndirect.
ms.assetid: e7668ab3-3a11-4bf4-8cb4-067d3204fb3f
keywords:
- Controlli di Windows per il codice di notifica TDN_NAVIGATED
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
ms.openlocfilehash: 6c9d8e9244889d7e55aad2b89f8ca4bb1c0bb1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519048"
---
# <a name="tdn_navigated-notification-code"></a>TDN \_ codice di notifica navigato

Inviato da una finestra di dialogo attività quando si è verificata la navigazione. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





