---
title: TDN_RADIO_BUTTON_CLICKED di notifica (Commctrl.h)
description: Inviato da una finestra di dialogo attività quando l'utente seleziona un pulsante di opzione o un collegamento di comando nella finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il metodo TaskDialogIndirect.
ms.assetid: d9a29874-6755-4754-bcaf-94746b218b47
keywords:
- TDN_RADIO_BUTTON_CLICKED del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TDN_RADIO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea1917a1523cdc3a106398d07912d3fff5295f7da18a59055f059a13007f98b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875761"
---
# <a name="tdn_radio_button_clicked-notification-code"></a>Codice di notifica \_ \_ \_ CLICKED del pulsante di opzione TDN

Inviato da una finestra di dialogo attività quando l'utente seleziona un pulsante di opzione o un collegamento di comando nella finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il [**metodo TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)


```C++
TDN_RADIO_BUTTON_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore **int** che specifica l'ID corrispondente al pulsante di opzione selezionato.

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



 

 





