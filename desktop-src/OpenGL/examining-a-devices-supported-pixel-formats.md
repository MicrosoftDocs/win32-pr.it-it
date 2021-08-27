---
title: Analisi di un formato pixel supportato dai dispositivi
description: La funzione DescribePixelFormat ottiene i dati in formato pixel per un contesto di dispositivo.
ms.assetid: 1ebeb051-2dc9-4753-a0f3-7d2737b5f7f2
keywords:
- OpenGL su Windows,pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6deb7dbb0f54a50bea4da5ba8f583a97442648096dbabc937a16a9aeaf49b645
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082471"
---
# <a name="examining-a-devices-supported-pixel-formats"></a>Analisi di un formato pixel supportato dai dispositivi

La [**funzione DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) ottiene i dati in formato pixel per un contesto di dispositivo. Restituisce anche un numero intero che rappresenta l'indice di formato pixel massimo per il contesto di dispositivo. L'esempio di codice seguente illustra come usare tale risultato per esaminare i formati pixel supportati da un dispositivo:


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



 

 




