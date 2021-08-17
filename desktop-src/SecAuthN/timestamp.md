---
description: Il tipo di dati TimeStamp contiene informazioni sulla validità temporale dei token di sicurezza. Il formato del valore del tipo di dati TimeStamp è lo stesso della struttura FILETIME.
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: TimeStamp (Sspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e521818c9001213396c0046b92f8f0bd9727dddfeaf99b2e23b652a48f8ff95d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786366"
---
# <a name="timestamp"></a>TimeStamp

Il **tipo di dati TimeStamp** contiene informazioni sulla validità temporale dei token di sicurezza. Il formato del valore del tipo di dati **TimeStamp** è lo stesso della struttura [**FILETIME.**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Sspi.h (include Security.h)</dt> </dl> |



 

 
