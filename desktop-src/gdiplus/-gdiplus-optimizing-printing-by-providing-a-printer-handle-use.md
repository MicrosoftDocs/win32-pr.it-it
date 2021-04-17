---
description: Uno dei costruttori della classe Graphics riceve un handle del contesto di dispositivo e un handle della stampante.
ms.assetid: 9be67cb2-4bf9-4758-af03-7d92dd04feaf
title: Ottimizzazione della stampa fornendo un handle di stampante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a247af3de037e220432c424c408b4055690ff861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977570"
---
# <a name="optimizing-printing-by-providing-a-printer-handle"></a>Ottimizzazione della stampa fornendo un handle di stampante

Uno dei costruttori della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) riceve un handle del contesto di dispositivo e un handle della stampante. Quando si inviano comandi di Windows GDI+ a determinate stampanti di post-script, le prestazioni sono migliori se si crea l'oggetto **Graphics** con tale costruttore specifico.

La seguente applicazione console chiama [GetDefaultPrinter](../printdocs/getdefaultprinter.md) per ottenere il nome della stampante predefinita. Il codice passa il nome della stampante a [CreateDC](/windows/win32/api/wingdi/nf-wingdi-createdcw) per ottenere un handle del contesto di dispositivo per la stampante. Il codice passa anche il nome della stampante a [OpenPrinter](../printdocs/openprinter.md) per ottenere un handle di stampante. Sia l'handle del contesto di dispositivo che l'handle della stampante vengono passati al costruttore di [**grafica**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Vengono quindi disegnate due figure sulla stampante.

> [!Note]  
> La funzione [GetDefaultPrinter](../printdocs/getdefaultprinter.md) è supportata solo in Windows 2000 e versioni successive.

 


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   DWORD   size;
   HDC     hdcPrint;
   HANDLE  printerHandle;

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   // Get the length of the printer name.
   GetDefaultPrinter(NULL, &size);
   TCHAR* buffer = new TCHAR[size];

   // Get the printer name.
   if(!GetDefaultPrinter(buffer, &size))
   {
      printf("Failure");
   }
   else
   {
      // Get a device context for the printer.
      hdcPrint = CreateDC(NULL, buffer, NULL, NULL);

      // Get a printer handle.
      OpenPrinter(buffer, &printerHandle, NULL);

      StartDoc(hdcPrint, &docInfo);
      StartPage(hdcPrint);
         Graphics* graphics = new Graphics(hdcPrint, printerHandle);
         Pen* pen = new Pen(Color(255, 0, 0, 0));
         graphics->DrawRectangle(pen, 200, 500, 200, 150);
         graphics->DrawEllipse(pen, 200, 500, 200, 150);
         delete(pen);
         delete(graphics);
      EndPage(hdcPrint);
      EndDoc(hdcPrint);

      ClosePrinter(printerHandle);
      DeleteDC(hdcPrint);
   }

   delete buffer;
   
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
