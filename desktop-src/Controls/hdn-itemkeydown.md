---
title: Codice di notifica HDN_ITEMKEYDOWN (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che è stato premuto un tasto con un elemento selezionato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ab6922ab-907d-44fc-8606-28f395118405
keywords:
- Controlli di Windows per il codice di notifica HDN_ITEMKEYDOWN
topic_type:
- apiref
api_name:
- HDN_ITEMKEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4415eb5a026bf96d53884fe2735f3a3fa2e494
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048749"
---
# <a name="hdn_itemkeydown-notification-code"></a>\_Codice di notifica ITEMKEYDOWN di HDN

Notifica alla finestra padre di un controllo di intestazione che è stato premuto un tasto con un elemento selezionato. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
HDN_ITEMKEYDOWN

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che contiene informazioni aggiuntive sulla chiave da premere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





