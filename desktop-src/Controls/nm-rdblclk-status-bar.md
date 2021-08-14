---
title: NM_RDBLCLK (barra di stato) codice di notifica (Commctrl.h)
description: Notifica alle finestre padre di un controllo barra di stato che l'utente ha fatto doppio clic con il pulsante destro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 57d8c5a7-e179-4b65-a3aa-5566d5780c18
keywords:
- NM_RDBLCLK di notifica (barra di stato) Windows controlli
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8aa5c754eed028d050f1f42ab6ab7ae652bfb3a3dc8bedb49df81357db6b5af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410682"
---
# <a name="nm_rdblclk-status-bar-notification-code"></a>Codice \_ di notifica NM RDBLCLK (barra di stato)

Notifica alle finestre padre di un controllo barra di stato che l'utente ha fatto doppio clic con il pulsante destro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RDBLCLK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni aggiuntive su questa notifica. Il **membro dwItemSpec** contiene l'indice della sezione su cui è stato fatto clic.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** per indicare che il clic del mouse è stato gestito ed elimina l'elaborazione predefinita dal sistema. Restituisce **FALSE** per consentire l'elaborazione predefinita del clic.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





