---
description: Non tutti i dispositivi di output supportano l'intero set di funzioni grafiche.
ms.assetid: 7989d393-7be4-47fc-af8d-26dd549c48be
title: Recupero delle funzionalità di una stampante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d84db8d46255f4dfd33ce62ab4ab6735b0f2a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978298"
---
# <a name="retrieving-the-capabilities-of-a-printer"></a><span data-ttu-id="08f47-103">Recupero delle funzionalità di una stampante</span><span class="sxs-lookup"><span data-stu-id="08f47-103">Retrieving the Capabilities of a Printer</span></span>

<span data-ttu-id="08f47-104">Non tutti i dispositivi di output supportano l'intero set di funzioni grafiche.</span><span class="sxs-lookup"><span data-stu-id="08f47-104">Not every output device supports the entire set of graphics functions.</span></span> <span data-ttu-id="08f47-105">Ad esempio, a causa delle limitazioni hardware, la maggior parte dei plotter di vettori non supporta i trasferimenti di blocchi di bit.</span><span class="sxs-lookup"><span data-stu-id="08f47-105">For example, because of hardware limitations, most vector plotters do not support bit-block transfers.</span></span> <span data-ttu-id="08f47-106">Un'applicazione può determinare se un dispositivo supporta una particolare funzione grafica chiamando la funzione [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , specificando l'indice appropriato ed esaminando il valore restituito.</span><span class="sxs-lookup"><span data-stu-id="08f47-106">An application can determine whether a device supports a particular graphics function by calling the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function, specifying the appropriate index, and examining the return value.</span></span>

<span data-ttu-id="08f47-107">Nell'esempio seguente viene illustrato il modo in cui un'applicazione testa una stampante per determinare se supporta i trasferimenti di blocchi di bit.</span><span class="sxs-lookup"><span data-stu-id="08f47-107">The following example shows how an application tests a printer to determine whether it supports bit-block transfers.</span></span>


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



 

 



