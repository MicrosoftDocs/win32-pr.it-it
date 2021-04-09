---
title: Codice di notifica EN_STARTCOMPOSITION (RichEdit. h)
description: Notifica a una finestra padre del controllo Rich Edit che l'utente ha iniziato a digitare con IME o il Framework dei servizi di testo.
ms.assetid: 755C0C5F-061B-44AF-98A5-776AEE1B7AF8
keywords:
- Controlli di Windows per il codice di notifica EN_STARTCOMPOSITION
topic_type:
- apiref
api_name:
- EN_STARTCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a103431427a9325a6b74c27927fb56e65f6fe771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121022"
---
# <a name="en_startcomposition-notification-code"></a>\_Codice di notifica en STARTCOMPOSITION

Notifica a una finestra padre del controllo Rich Edit che l'utente ha iniziato a digitare con IME o il [Framework dei servizi di testo](/windows/desktop/TSF/text-services-framework).


```C++
EN_STARTCOMPOSITION

    pStartComp = (NMDHR *) lParam;
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
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

