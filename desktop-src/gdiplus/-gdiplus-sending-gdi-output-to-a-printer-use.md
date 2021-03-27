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
# <a name="sending-gdi-output-to-a-printer"></a><span data-ttu-id="ccbae-104">Invio di un output GDI+ a una stampante</span><span class="sxs-lookup"><span data-stu-id="ccbae-104">Sending GDI+ Output to a Printer</span></span>

<span data-ttu-id="ccbae-105">L'utilizzo di Windows GDI+ per la stampa su una stampante è analogo all'utilizzo di GDI+ per l'estrazione di uno schermo del computer.</span><span class="sxs-lookup"><span data-stu-id="ccbae-105">Using Windows GDI+ to draw on a printer is similar to using GDI+ to draw on a computer screen.</span></span> <span data-ttu-id="ccbae-106">Per creare una stampante, ottenere un handle del contesto di dispositivo per la stampante e quindi passare tale handle a un costruttore di [**grafica**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="ccbae-106">To draw on a printer, obtain a device context handle for the printer and then pass that handle to a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span>

<span data-ttu-id="ccbae-107">La seguente applicazione console disegna una linea, un rettangolo e un'ellisse in una stampante denominata di stampa:</span><span class="sxs-lookup"><span data-stu-id="ccbae-107">The following console application draws a line, a rectangle, and an ellipse on a printer named MyPrinter:</span></span>


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



<span data-ttu-id="ccbae-108">Nel codice precedente, i tre comandi di disegno GDI+ si trovano tra le chiamate alle funzioni [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) e [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc) , ognuna delle quali riceve l'handle di contesto del dispositivo stampante.</span><span class="sxs-lookup"><span data-stu-id="ccbae-108">In the preceding code, the three GDI+ drawing commands are in between calls to the [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) and [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc) functions, each of which receives the printer device context handle.</span></span> <span data-ttu-id="ccbae-109">Tutti i comandi grafici tra StartDoc e EndDoc vengono instradati a un metafile temporaneo.</span><span class="sxs-lookup"><span data-stu-id="ccbae-109">All graphics commands between StartDoc and EndDoc are routed to a temporary metafile.</span></span> <span data-ttu-id="ccbae-110">Dopo la chiamata a EndDoc, il driver della stampante converte i dati nel metafile nel formato richiesto dalla stampante specifica in uso.</span><span class="sxs-lookup"><span data-stu-id="ccbae-110">After the call to EndDoc, the printer driver converts the data in the metafile into the format required by the specific printer being used.</span></span>

> [!Note]  
> <span data-ttu-id="ccbae-111">Se lo spooling non è abilitato per la stampante utilizzata, l'output della grafica non viene indirizzato a un metafile.</span><span class="sxs-lookup"><span data-stu-id="ccbae-111">If spooling is not enabled for the printer being used, the graphics output is not routed to a metafile.</span></span> <span data-ttu-id="ccbae-112">Al contrario, i singoli comandi grafici vengono elaborati dal driver della stampante e quindi inviati alla stampante.</span><span class="sxs-lookup"><span data-stu-id="ccbae-112">Instead, individual graphics commands are processed by the printer driver and then sent to the printer.</span></span>

 

<span data-ttu-id="ccbae-113">In genere non è necessario impostare come hardcoded il nome di una stampante come è stato fatto nell'applicazione console precedente.</span><span class="sxs-lookup"><span data-stu-id="ccbae-113">Generally you won't want to hard-code the name of a printer as was done in the preceding console application.</span></span> <span data-ttu-id="ccbae-114">Un'alternativa al nome a livello di codice consiste nel chiamare [GetDefaultPrinter](../printdocs/getdefaultprinter.md) per ottenere il nome della stampante predefinita.</span><span class="sxs-lookup"><span data-stu-id="ccbae-114">One alternative to hard-coding the name is to call [GetDefaultPrinter](../printdocs/getdefaultprinter.md) to obtain the name of the default printer.</span></span> <span data-ttu-id="ccbae-115">Prima di chiamare GetDefaultPrinter, è necessario allocare un buffer sufficientemente grande da mantenere il nome della stampante.</span><span class="sxs-lookup"><span data-stu-id="ccbae-115">Before you call GetDefaultPrinter, you must allocate a buffer large enough to hold the printer name.</span></span> <span data-ttu-id="ccbae-116">È possibile determinare le dimensioni del buffer necessario chiamando GetDefaultPrinter, passando **null** come primo argomento.</span><span class="sxs-lookup"><span data-stu-id="ccbae-116">You can determine the size of the required buffer by calling GetDefaultPrinter, passing **NULL** as the first argument.</span></span>

> [!Note]  
> <span data-ttu-id="ccbae-117">La funzione [GetDefaultPrinter](../printdocs/getdefaultprinter.md) è supportata solo in Windows 2000 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ccbae-117">The [GetDefaultPrinter](../printdocs/getdefaultprinter.md) function is supported only on Windows 2000 and later.</span></span>

 

<span data-ttu-id="ccbae-118">La seguente applicazione console ottiene il nome della stampante predefinita, quindi disegna un rettangolo e un'ellisse sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="ccbae-118">The following console application gets the name of the default printer and then draws a rectangle and an ellipse on that printer.</span></span> <span data-ttu-id="ccbae-119">La chiamata di [**Graphics::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) è compresa tra le chiamate a [Startpage](/windows/win32/api/wingdi/nf-wingdi-startpage) e [EndPage](/windows/win32/api/wingdi/nf-wingdi-endpage), pertanto il rettangolo si trova in una pagina da sola.</span><span class="sxs-lookup"><span data-stu-id="ccbae-119">The [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) call is in between calls to [StartPage](/windows/win32/api/wingdi/nf-wingdi-startpage) and [EndPage](/windows/win32/api/wingdi/nf-wingdi-endpage), so the rectangle is on a page by itself.</span></span> <span data-ttu-id="ccbae-120">Analogamente, l'ellisse si trova in una pagina da sola.</span><span class="sxs-lookup"><span data-stu-id="ccbae-120">Similarly, the ellipse is on a page by itself.</span></span>


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



 

 
