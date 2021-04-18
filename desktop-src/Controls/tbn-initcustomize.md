---
title: Codice di notifica TBN_INITCUSTOMIZE (COMmctrl. h)
description: Notifica alla finestra padre di una barra degli strumenti che la personalizzazione è stata avviata. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: f4b9a1b0-94f7-4b2b-81b3-772da09134d2
keywords:
- Controlli di Windows per il codice di notifica TBN_INITCUSTOMIZE
topic_type:
- apiref
api_name:
- TBN_INITCUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5e855374699a100bf78019f1ca3d89857bc7c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300972"
---
# <a name="tbn_initcustomize-notification-code"></a>\_Codice di notifica INITCUSTOMIZE di TBN

Notifica alla finestra padre di una barra degli strumenti che la personalizzazione è stata avviata. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TBN_INITCUSTOMIZE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore alla struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) della barra degli strumenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce TBNRF \_ HIDEHELP per disattivare il pulsante della guida.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





