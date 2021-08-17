---
title: EN_STARTCOMPOSITION di notifica (Richedit.h)
description: Notifica a una finestra padre del controllo Rich Edit che l'utente ha iniziato a digitare con IME o Framework servizi di testo.
ms.assetid: 755C0C5F-061B-44AF-98A5-776AEE1B7AF8
keywords:
- EN_STARTCOMPOSITION del codice di notifica Windows controlli
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
ms.openlocfilehash: 4b182322175d03ab1c6906132c8f5970ce1d716e7e1c745406b009e5b224ec2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436671"
---
# <a name="en_startcomposition-notification-code"></a>Codice \_ di notifica EN STARTCOMPOSITION

Notifica a una finestra padre del controllo Rich Edit che l'utente ha iniziato a digitare con IME [o Framework servizi di testo](/windows/desktop/TSF/text-services-framework).


```C++
EN_STARTCOMPOSITION

    pStartComp = (NMDHR *) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**NMHDR.**](/windows/desktop/api/richedit/ns-richedit-nmhdr)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

