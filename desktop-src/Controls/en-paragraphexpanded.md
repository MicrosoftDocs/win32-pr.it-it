---
title: Codice di notifica EN_PARAGRAPHEXPANDED (RichEdit. h)
description: Notifica all'elemento padre di un controllo Rich Edit che è stata espansa una struttura. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: D33EB118-FC79-4284-820B-3424F13722C4
keywords:
- Controlli di Windows per il codice di notifica EN_PARAGRAPHEXPANDED
topic_type:
- apiref
api_name:
- EN_PARAGRAPHEXPANDEDC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f862260c0653d23b0b53649a2c05e59820e3808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476979"
---
# <a name="en_paragraphexpanded-notification-code"></a>\_Codice di notifica en PARAGRAPHEXPANDED

Notifica all'elemento padre di un controllo Rich Edit che è stata espansa una struttura. Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
EN_PARAGRAPHEXPANDED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





