---
title: Codice di notifica NM_CLICK (barra degli strumenti) (COMmctrl. h)
description: Inviato da un controllo Toolbar quando l'utente fa clic su un elemento con il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: fa43c9bc-db2a-4460-b193-2b4694d06d83
keywords:
- Codice di notifica di NM_CLICK (barra degli strumenti) controlli Windows
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca31e3553327c94d371617d016a85395519c211d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874690"
---
# <a name="nm_click-toolbar-notification-code"></a>Codice di notifica di NM \_ (barra degli strumenti)

Inviato da un controllo Toolbar quando l'utente fa clic su un elemento con il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni aggiuntive su questa notifica. Il membro **dwItemSpec** contiene l'indice della sezione su cui è stato fatto clic.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** per indicare che il clic del mouse è stato gestito ed Elimina l'elaborazione predefinita dal sistema. Restituisce **false** per consentire l'elaborazione predefinita del clic.

## <a name="remarks"></a>Commenti

Quando si fa clic su un elemento con il pulsante sinistro del mouse, la barra degli strumenti Invia un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) con il codice di notifica [ \_ selezionato BN](bn-clicked.md) alla finestra padre. La \_ notifica di clic su Nm viene inviata dopo il messaggio del **\_ comando WM** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

