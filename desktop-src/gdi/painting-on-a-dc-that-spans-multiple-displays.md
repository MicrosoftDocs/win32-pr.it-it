---
description: Per rispondere a un messaggio WM \_ PAINT, usare codice simile al seguente.
ms.assetid: 682d9bc6-8d74-48c4-80fb-bae73d409a6b
title: Disegno su un controller di dominio che si estende su più schermi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550279d003c7d32fc97923ea6ebe4c95364773e514a69e4c66bdb4b100784384
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759482"
---
# <a name="painting-on-a-dc-that-spans-multiple-displays"></a>Disegno su un controller di dominio che si estende su più schermi

Per rispondere a un **messaggio WM \_ PAINT,** usare codice simile al seguente.


```C++
case WM_PAINT:
hdc = BeginPaint(hwnd, &ps);
EnumDisplayMonitors(hdc, NULL, MyPaintEnumProc, 0);
EndPaint(hwnd, &ps);
 
```



Per disegnare la metà superiore di una finestra, usare codice simile al seguente.


```C++
GetClient Rect(hwnd, &rc);
rc.bottom = (rc.bottom - rc.top) / 2;
hdc = GetDC(hwnd);
EnumDisplayMonitors(hdc, &rc, MyPaintEnumProc, 0);
ReleaseDC(hwnd, hdc);
```



Per disegnare l'intero schermo virtuale in modo ottimale per ogni monitoraggio, usare codice simile al seguente.


```C++
hdc = GetDC(NULL);
EnumDisplayMonitors(hdc, NULL, MyPaintScreenEnumProc, 0);
ReleaseDC(NULL, hdc);
```



 

 



