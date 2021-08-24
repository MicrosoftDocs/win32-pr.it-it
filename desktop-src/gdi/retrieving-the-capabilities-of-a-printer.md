---
description: Non tutti i dispositivi di output supportano l'intero set di funzioni grafiche.
ms.assetid: 7989d393-7be4-47fc-af8d-26dd549c48be
title: Recupero delle funzionalità di una stampante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c332832efc62f28ee77a5476ef12f706eb2e97a2cd5e86877e4a71a48feb907
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779061"
---
# <a name="retrieving-the-capabilities-of-a-printer"></a>Recupero delle funzionalità di una stampante

Non tutti i dispositivi di output supportano l'intero set di funzioni grafiche. Ad esempio, a causa delle limitazioni hardware, la maggior parte dei plotter vettoriali non supporta i trasferimenti a blocchi di bit. Un'applicazione può determinare se un dispositivo supporta una particolare funzione grafica chiamando la [**funzione GetDeviceCaps,**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) specificando l'indice appropriato ed esaminando il valore restituito.

Nell'esempio seguente viene illustrato come un'applicazione testa una stampante per determinare se supporta i trasferimenti a blocchi di bit.


```C++
// Examine the raster capabilities of the device  
// identified by hdcPrint to verify that it supports  
// the BitBlt function.  
 
if ((GetDeviceCaps(hdcPrint, RASTERCAPS) 
       & RC_BITBLT) == 0) 
{ 
   DeleteDC(hdcPrint); 
   break; 
} 

else 
{ 
    // Print the bitmap using the printer DC.  
}
```



 

 



