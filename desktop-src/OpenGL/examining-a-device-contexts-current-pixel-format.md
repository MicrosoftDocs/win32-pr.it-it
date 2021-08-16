---
title: Analisi del formato pixel corrente dei contesti di dispositivo
description: Usare le funzioni GetPixelFormat e DescribePixelFormat per esaminare il formato pixel corrente di un contesto di dispositivo, come illustrato nel frammento di codice seguente.
ms.assetid: 1da8c8e0-9444-421a-9c2e-c196b5a9db36
keywords:
- OpenGL su Windows,pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b76dd8db71356b16a5a258669ffe2938d0982ab5e1417389840610c57a0fcdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361371"
---
# <a name="examining-a-device-contexts-current-pixel-format"></a>Analisi del formato pixel corrente dei contesti di dispositivo

Usare le [**funzioni GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) e [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) per esaminare il formato pixel corrente di un contesto di dispositivo, come illustrato nel frammento di codice seguente.


```C++
PIXELFORMATDESCRIPTOR  pfd;
HDC    hdc;
int    iPixelFormat;
 
// if the device context has a current pixel format ...  
if (iPixelFormat = GetPixelFormat(hdc)) { 
 
    // obtain a detailed description of that pixel format  
    DescribePixelFormat(hdc, iPixelFormat, 
                             sizeof(PIXELFORMATDESCRIPTOR), &pfd); 
    }
```



 

 




