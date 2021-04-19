---
description: Il \_ tipo di dati time di riferimento definisce le unità per i tempi di riferimento in DirectShow. Ogni unità di tempo di riferimento è di 100 nanosecondi.
ms.assetid: 862c95bc-2e0a-42c0-b907-45f64f27bd41
title: REFERENCE_TIME (Strmif. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab88576f611674f5b208c5c39d328c77dcf57aec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332182"
---
# <a name="reference_time"></a>\_ora riferimento

Il tipo di dati **\_ time di riferimento** definisce le unità per i tempi di riferimento in DirectShow. Ogni unità di tempo di riferimento è di 100 nanosecondi.


```C++
typedef LONGLONG REFERENCE_TIME;
```



## <a name="remarks"></a>Commenti

Il tipo di dati **\_ time di riferimento** è un Integer a 64 bit.

I tempi di riferimento vengono in genere misurati in base a una delle linee di base seguenti:

-   Tempo di clock assoluto. In questo caso, la linea di base dipenderà dall'implementazione del clock. Per altre informazioni, vedere [clock di riferimento](reference-clocks.md).
-   Relativo all'inizio della riproduzione.

Per altre informazioni sui tempi di riferimento, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Strmif. h (include dshow. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di dati DirectShow](directshow-data-types.md)
</dt> </dl>

 

 




