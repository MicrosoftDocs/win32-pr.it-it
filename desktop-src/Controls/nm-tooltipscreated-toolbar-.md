---
title: NM_TOOLTIPSCREATED (barra degli strumenti) codice di notifica (Commctrl.h)
description: Notifica alla finestra padre di una barra degli strumenti che la barra degli strumenti ha creato un controllo descrizione comando. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 0e9517c1-aa3f-4b14-82b4-195a4ce99757
keywords:
- NM_TOOLTIPSCREATED di notifica (barra degli strumenti) Windows controlli
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa40313a8b8c11c48b37cf2ae0593cb1bbc85353303f7c8840e7e5eb55ea7ca9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877281"
---
# <a name="nm_tooltipscreated-toolbar-notification-code"></a>CODICE \_ DI NOTIFICA NM TOOLTIPSCREATED (barra degli strumenti)

Notifica alla finestra padre di una barra degli strumenti che la barra degli strumenti ha creato un controllo descrizione comando. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMTOOLTIPSCREATED) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il controllo barra degli strumenti ignora il valore restituito da questo codice di notifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





