---
description: L Windows GDI+ per disegnare su una stampante è simile all'uso di GDI+ per disegnare sullo schermo di un computer. Per disegnare su una stampante, ottenere un handle del contesto di dispositivo per la stampante e quindi passare tale handle a un costruttore Graphics.
ms.assetid: a76cca57-6ed8-44cd-a9f6-f2692d14b68a
title: Invio di un output GDI+ a una stampante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51116e27f3ef4e457d2d3cf8d39b26c1a5e2275da4b964bd4de58ec273db1e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943781"
---
# <a name="sending-gdi-output-to-a-printer"></a>Invio di un output GDI+ a una stampante

L Windows GDI+ per disegnare su una stampante è simile all'uso di GDI+ per disegnare sullo schermo di un computer. Per disegnare su una stampante, ottenere un handle del contesto di dispositivo per la stampante e quindi passare tale handle a un [**costruttore Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)

L'applicazione console seguente disegna una linea, un rettangolo e un'ellisse su una stampante denominata MyPrinter:


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

   // Get a device context for the printer.
   HDC hdcPrint = CreateDC(NULL, TEXT("\\\\printserver\\print1"), NULL, NULL);

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   StartDoc(hdcPrint, &docInfo);
   StartPage(hdcPrint);
      Graphics* graphics = new Graphics(hdcPrint);
      Pen* pen = new Pen(Color(255, 0, 0, 0));
      graphics->DrawLine(pen, 50, 50, 350, 550);
      graphics->DrawRectangle(pen, 50, 50, 300, 500);
      graphics->DrawEllipse(pen, 50, 50, 300, 500);
      delete pen;
      delete graphics;
   EndPage(hdcPrint);
   EndDoc(hdcPrint);
   
   DeleteDC(hdcPrint);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



Nel codice precedente i tre comandi GDI+ di disegno sono compresi tra le chiamate alle funzioni [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) ed [EndDoc,](/windows/win32/api/wingdi/nf-wingdi-enddoc) ognuno dei quali riceve l'handle del contesto di dispositivo della stampante. Tutti i comandi grafici compresi tra StartDoc ed EndDoc vengono instradati a un metafile temporaneo. Dopo la chiamata a EndDoc, il driver della stampante converte i dati nel metafile nel formato richiesto dalla stampante specifica in uso.

> [!Note]  
> Se lo spooling non è abilitato per la stampante in uso, l'output grafico non viene indirizzato a un metafile. I singoli comandi grafici vengono invece elaborati dal driver della stampante e quindi inviati alla stampante.

 

In genere non è consigliabile impostare come hard coded il nome di una stampante come è stato fatto nell'applicazione console precedente. Un'alternativa alla codifica hard-coding del nome consiste nel chiamare [GetDefaultPrinter](../printdocs/getdefaultprinter.md) per ottenere il nome della stampante predefinita. Prima di chiamare GetDefaultPrinter, è necessario allocare un buffer sufficientemente grande da contenere il nome della stampante. È possibile determinare le dimensioni del buffer richiesto chiamando GetDefaultPrinter, passando **NULL** come primo argomento.

> [!Note]  
> La [funzione GetDefaultPrinter](../printdocs/getdefaultprinter.md) è supportata solo in Windows 2000 e versioni successive.

 

L'applicazione console seguente ottiene il nome della stampante predefinita e quindi disegna un rettangolo e un'ellisse su tale stampante. La [**chiamata Graphics::D rawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) si trova tra le chiamate a [StartPage](/windows/win32/api/wingdi/nf-wingdi-startpage) ed [EndPage,](/windows/win32/api/wingdi/nf-wingdi-endpage)quindi il rettangolo si trova in una pagina da sola. Analogamente, l'ellisse si trova in una pagina da sola.


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

   DWORD size;
   HDC hdcPrint;

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   // Get the size of the default printer name.
   GetDefaultPrinter(NULL, &size);

   // Allocate a buffer large enough to hold the printer name.
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

      StartDoc(hdcPrint, &docInfo);
         Graphics* graphics;
         Pen* pen = new Pen(Color(255, 0, 0, 0));

         StartPage(hdcPrint);
            graphics = new Graphics(hdcPrint);
            graphics->DrawRectangle(pen, 50, 50, 200, 300);
            delete graphics;
         EndPage(hdcPrint);

         StartPage(hdcPrint);
            graphics = new Graphics(hdcPrint);
            graphics->DrawEllipse(pen, 50, 50, 200, 300);
            delete graphics;
         EndPage(hdcPrint);

         delete pen;
      EndDoc(hdcPrint);

      DeleteDC(hdcPrint);
   }

   delete buffer;

   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
