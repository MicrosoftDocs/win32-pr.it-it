---
title: Codice di notifica TDN_EXPANDO_BUTTON_CLICKED (COMmctrl. h)
description: Inviato dalla finestra di dialogo attività quando l'utente fa clic sul pulsante expando della finestra di dialogo. Questa notifica viene ricevuta solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo TaskDialogIndirect.
ms.assetid: 15e2a9d0-9986-4fb1-a15e-dd4839e45146
keywords:
- Controlli di Windows per il codice di notifica TDN_EXPANDO_BUTTON_CLICKED
topic_type:
- apiref
api_name:
- TDN_EXPANDO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f3c36379a8efc40c7873d817b832705b3c1e084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302638"
---
# <a name="tdn_expando_button_clicked-notification-code"></a>Il \_ pulsante TDN expando ha \_ \_ fatto clic sul codice di notifica

Inviato dalla finestra di dialogo attività quando l'utente fa clic sul pulsante expando della finestra di dialogo. Questa notifica viene ricevuta solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .


```C++
TDN_EXPANDO_BUTTON_CLICKED
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**Bool** che è **true** se la finestra di dialogo è espansa o **false** in caso contrario.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Nell'esempio nella sezione Syntax viene illustrato il cast a wParam prima di inviare la notifica. **LParam** non viene utilizzato e deve essere zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





