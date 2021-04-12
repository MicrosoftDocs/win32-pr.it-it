---
title: Codice di notifica HDN_ITEMDBLCLICK (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che l'utente ha fatto doppio clic sul controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM. Solo i controlli header impostati sullo \_ stile dei pulsanti HDS inviano il codice di notifica.
ms.assetid: 72bb00b9-226f-4409-b788-b623868f78b6
keywords:
- Controlli di Windows per il codice di notifica HDN_ITEMDBLCLICK
topic_type:
- apiref
api_name:
- HDN_ITEMDBLCLICK
- HDN_ITEMDBLCLICKA
- HDN_ITEMDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e61117303ecc478a998da8799867988dbc1ca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225235"
---
# <a name="hdn_itemdblclick-notification-code"></a>\_Codice di notifica ITEMDBLCLICK di HDN

Notifica alla finestra padre di un controllo di intestazione che l'utente ha fatto doppio clic sul controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . Solo i controlli header impostati sullo stile dei [**\_ pulsanti HDS**](header-control-styles.md) inviano il codice di notifica.


```C++
HDN_ITEMDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che contiene informazioni su questo codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HDN \_ ITEMDBLCLICKW** (Unicode) e **HDN \_ ITEMDBLCLICKA** (ANSI)<br/>         |



 

 





