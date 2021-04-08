---
title: Codice di notifica TDN_BUTTON_CLICKED (COMmctrl. h)
description: Inviato da una finestra di dialogo attività quando l'utente seleziona un pulsante o un collegamento al comando nella finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo TaskDialogIndirect.
ms.assetid: eefe48f8-8a80-4280-8a7e-244d9b699ec7
keywords:
- Controlli di Windows per il codice di notifica TDN_BUTTON_CLICKED
topic_type:
- apiref
api_name:
- TDN_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7a0b799f4163633194306edaa1703e068e93c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964934"
---
# <a name="tdn_button_clicked-notification-code"></a>\_Codice di \_ notifica fatto clic sul pulsante TDN

Inviato da una finestra di dialogo attività quando l'utente seleziona un pulsante o un collegamento al comando nella finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .


```C++
TDN_BUTTON_CLICKED  

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore **int** che specifica l'ID del pulsante o del collegamento di Comand selezionato.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per evitare la chiusura della finestra di dialogo attività, l'applicazione deve restituire **S \_ false**. in caso contrario, la finestra di dialogo attività viene chiusa e l'ID del pulsante viene restituito tramite la chiamata all'applicazione originale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





