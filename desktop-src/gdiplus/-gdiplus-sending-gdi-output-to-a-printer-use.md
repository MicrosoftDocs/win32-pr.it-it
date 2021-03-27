---
description: L'utilizzo di Windows GDI+ per la stampa su una stampante è analogo all'utilizzo di GDI+ per l'estrazione di uno schermo del computer. Per creare una stampante, ottenere un handle del contesto di dispositivo per la stampante e quindi passare tale handle a un costruttore di grafica.
ms.assetid: a76cca57-6ed8-44cd-a9f6-f2692d14b68a
title: Invio di un output GDI+ a una stampante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c1c4f6c05e4918663284e6d7747952040dcddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049859"
---
# <a name="sending-gdi-output-to-a-printer"></a>Invio di un output GDI+ a una stampante

L'utilizzo di Windows GDI+ per la stampa su una stampante è analogo all'utilizzo di GDI+ per l'estrazione di uno schermo del computer. Per creare una stampante, ottenere un handle del contesto di dispositivo per la stampante e quindi passare tale handle a un costruttore di [**grafica**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

La seguente applicazione console disegna una linea, un rettangolo e un'ellisse in una stampante denominata di stampa:


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



Nel codice precedente, i tre comandi di disegno GDI+ si trovano tra le chiamate alle funzioni [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) e [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc) , ognuna delle quali riceve l'handle di contesto del dispositivo stampante. Tutti i comandi grafici tra StartDoc e EndDoc vengono instradati a un metafile temporaneo. Dopo la chiamata a EndDoc, il driver della stampante converte i dati nel metafile nel formato richiesto dalla stampante specifica in uso.

> [!Note]  
> Se lo spooling non è abilitato per la stampante utilizzata, l'output della grafica non viene indirizzato a un metafile. Al contrario, i singoli comandi grafici vengono elaborati dal driver della stampante e quindi inviati alla stampante.

 

In genere non è necessario impostare come hardcoded il nome di una stampante come è stato fatto nell'applicazione console precedente. Un'alternativa al nome a livello di codice consiste nel chiamare [GetDefaultPrinter](../printdocs/getdefaultprinter.md) per ottenere il nome della stampante predefinita. Prima di chiamare GetDefaultPrinter, è necessario allocare un buffer sufficientemente grande da mantenere il nome della stampante. È possibile determinare le dimensioni del buffer necessario chiamando GetDefaultPrinter, passando **null** come primo argomento.

> [!Note]  
> La funzione [GetDefaultPrinter](../printdocs/getdefaultprinter.md) è supportata solo in Windows 2000 e versioni successive.

 

La seguente applicazione console ottiene il nome della stampante predefinita, quindi disegna un rettangolo e un'ellisse sulla stampante. La chiamata di [**Graphics::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) è compresa tra le chiamate a [Startpage](/windows/win32/api/wingdi/nf-wingdi-startpage) e [EndPage](/windows/win32/api/wingdi/nf-wingdi-endpage), pertanto il rettangolo si trova in una pagina da sola. Analogamente, l'ellisse si trova in una pagina da sola.


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



 

 
