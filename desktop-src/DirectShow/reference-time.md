---
description: Il tipo \_ di dati REFERENCE TIME definisce le unità per i tempi di riferimento in DirectShow. Ogni unità di tempo di riferimento è di 100 nanosecondi.
ms.assetid: 862c95bc-2e0a-42c0-b907-45f64f27bd41
title: REFERENCE_TIME (Strmif.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f1600e820ac59c53144743933701a61e4a7b753f814dde06c5c663a760938d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747321"
---
# <a name="reference_time"></a>TEMPO DI \_ RIFERIMENTO

Il **tipo di dati REFERENCE \_ TIME** definisce le unità per i tempi di riferimento in DirectShow. Ogni unità di tempo di riferimento è di 100 nanosecondi.


```C++
typedef LONGLONG REFERENCE_TIME;
```



## <a name="remarks"></a>Commenti

Il **tipo di dati REFERENCE \_ TIME** è un integer a 64 bit.

I tempi di riferimento vengono in genere misurati da una delle baseline seguenti:

-   Ora di clock assoluta. In questo caso, la linea di base dipenderà dall'implementazione dell'orologio. Per altre informazioni, vedere [Clock di riferimento.](reference-clocks.md)
-   Relativo all'inizio della riproduzione.

Per altre informazioni sui tempi di riferimento, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Strmif.h (includere Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Tipi di dati](directshow-data-types.md)
</dt> </dl>

 

 




