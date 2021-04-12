---
title: Esame di un dispositivo formati di pixel supportati
description: La funzione DescribePixelFormat ottiene i dati in formato pixel per un contesto di dispositivo.
ms.assetid: 1ebeb051-2dc9-4753-a0f3-7d2737b5f7f2
keywords:
- OpenGL per Windows, pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ee45212111354d79b7a23fd35490a08f0aead4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396631"
---
# <a name="examining-a-devices-supported-pixel-formats"></a><span data-ttu-id="36657-104">Esame di un dispositivo formati di pixel supportati</span><span class="sxs-lookup"><span data-stu-id="36657-104">Examining a Devices Supported Pixel Formats</span></span>

<span data-ttu-id="36657-105">La funzione [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) ottiene i dati in formato pixel per un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36657-105">The [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) function obtains pixel format data for a device context.</span></span> <span data-ttu-id="36657-106">Restituisce anche un numero intero che rappresenta l'indice di formato pixel massimo per il contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36657-106">It also returns an integer that is the maximum pixel format index for the device context.</span></span> <span data-ttu-id="36657-107">Nell'esempio di codice seguente viene illustrato come utilizzare tale risultato per esaminare ed esaminare i formati pixel supportati da un dispositivo:</span><span class="sxs-lookup"><span data-stu-id="36657-107">The following code sample shows how to use that result to step through and examine the pixel formats supported by a device:</span></span>


```C++
// local variables  
int                      iMax ; 
PIXELFORMATDESCRIPTOR    pfd; 
int                      iPixelFormat ; 
 
// initialize a pixel format index variable  
iPixelFormat = 1; 
 
// keep obtaining and examining pixel format data...  
do { 
    // try to obtain some pixel format data  
    iMax = DescribePixelFormat(hdc, iPixelFormat, sizeof(pfd), &pfd); 
 
    // if there was some problem with that...   
    if (iMax == 0) 
     
        // return indicating failure  
        return(FALSE); 
     
    // we have successfully obtained pixel format data  
 
    // let's examine the pixel format data...  
    myPixelFormatExaminer (&pfd); 
    }  
 
// ...until we've looked at all the device context's pixel formats  
while (++iPixelFormat <= iMax);
```



 

 




