---
description: Definisce unità di 100 nanosecondi.
ms.assetid: 9273ff1f-382e-4c58-b571-4852545915b3
title: MFTIME (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51a08ac4e82c5cb97615b47430baa1c3388677ac160487c132dd41b7454ce985
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240209"
---
# <a name="mftime"></a>MFTIME

Definisce unità di 100 nanosecondi.


```C++
typedef LONGLONG MFTIME;
```



## <a name="examples"></a>Esempio


```C++
const MFTIME ONE_SECOND = 10000000; // One second.
const LONG   ONE_MSEC = 1000;       // One millisecond

// Convert 100-nanosecond units to milliseconds.

inline LONG MFTimeToMsec(const LONGLONG& time)
{
    return (LONG)(time / (ONE_SECOND / ONE_MSEC));
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation di dati](media-foundation-datatypes.md)
</dt> </dl>

 

 




