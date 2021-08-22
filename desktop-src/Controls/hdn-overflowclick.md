---
title: HDN_OVERFLOWCLICK di notifica (Commctrl.h)
description: Inviato da un controllo intestazione al relativo elemento padre quando si fa clic sul pulsante di overflow dell'intestazione. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 770ae00a-b87f-4de2-b869-2a233f2c493e
keywords:
- HDN_OVERFLOWCLICK del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- HDN_OVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61cee31369bfa1574ba4690f952bc60fb0dde1e5a9bf2f41e98b659356a79625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576221"
---
# <a name="hdn_overflowclick-notification-code"></a>Codice di notifica OVERFLOWCLICK DI HDN \_

Inviato da un controllo intestazione al relativo elemento padre quando si fa clic sul pulsante di overflow dell'intestazione. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_OVERFLOWCLICK

    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che descrive il codice di notifica. Il processo chiamante è responsabile dell'allocazione di questa struttura, inclusa la [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenuta. Impostare i membri della struttura **NMHDR,** incluso il membro *di* codice che deve essere impostato su HDN \_ OVERFLOWCLICK.

Impostare il **membro iItem** della [**struttura NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) sull'indice del primo elemento di intestazione che non è visibile e pertanto deve essere visualizzato in caso di overflow.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il ricevitore della notifica esegue il cast **di LPARAM** per recuperare [**la struttura NMHEADER.**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) **WPARAM** contiene l'ID del controllo che invia la notifica.

Questo messaggio viene inviato solo quando lo stile [**HDS \_ OVERFLOW**](header-control-styles.md) è impostato sul controllo intestazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





