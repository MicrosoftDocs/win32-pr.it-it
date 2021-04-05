---
title: Codice di notifica di NM_CLICK (barra di stato) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto clic con il pulsante sinistro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 179ccbe9-f51f-4356-b91a-10d7e3607b09
keywords:
- Codice di notifica di NM_CLICK (barra di stato) controlli Windows
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
ms.openlocfilehash: e6066f76a8cf0b6ca34b5298cfcdcba2b11e3fa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874693"
---
# <a name="nm_click-status-bar-notification-code"></a>\_Codice di notifica di clic su Nm (barra di stato)

Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto clic con il pulsante sinistro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


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

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





