---
description: Un modo per ottenere un handle del contesto di dispositivo per una stampante è visualizzare una finestra di dialogo di stampa e consentire all'utente di scegliere una stampante.
ms.assetid: 73a74186-c916-4ad9-b768-6bc887fd5231
title: Visualizzazione di una finestra di dialogo Stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113c9235e70712a4923ebdc3ad239f533160eb2f84f76ae729d7fadf203ca612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036829"
---
# <a name="displaying-a-print-dialog-box"></a>Visualizzazione di una finestra di dialogo Stampa

Un modo per ottenere un handle del contesto di dispositivo per una stampante è visualizzare una finestra di dialogo di stampa e consentire all'utente di scegliere una stampante. La [funzione PrintDlg](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) (che visualizza la finestra di dialogo) ha un parametro che corrisponde all'indirizzo di una [struttura PRINTDLG.](/windows/win32/api/commdlg/ns-commdlg-printdlga?redirectedfrom=MSDN) La struttura PRINTDLG ha diversi membri, ma è possibile lasciare la maggior parte di essi impostata sui valori predefiniti. I due membri da impostare sono **lStructSize** e **Flags.** Impostare **lStructSize** sulla dimensione di una variabile PRINTDLG e **impostare Flags** su PD \_ RETURNDC. **L'impostazione di** Flag su PC RETURNDC specifica che si vuole che la funzione PrintDlg riempia il campo hDC con un handle di contesto di dispositivo per la stampante scelta \_ dall'utente. 


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
   
   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";
   
   // Create a PRINTDLG structure, and initialize the appropriate fields.
   PRINTDLG printDlg;
   ZeroMemory(&printDlg, sizeof(printDlg));
   printDlg.lStructSize = sizeof(printDlg);
   printDlg.Flags = PD_RETURNDC;
   
   // Display a print dialog box.
   if(!PrintDlg(&printDlg))
   {
      printf("Failure\n");
   }
   else
   {
      // Now that PrintDlg has returned, a device context handle
      // for the chosen printer is in printDlg->hDC.
      
      StartDoc(printDlg.hDC, &docInfo);
      StartPage(printDlg.hDC);
         Graphics* graphics = new Graphics(printDlg.hDC);
         Pen* pen = new Pen(Color(255, 0, 0, 0));
         graphics->DrawRectangle(pen, 200, 500, 200, 150);
         graphics->DrawEllipse(pen, 200, 500, 200, 150);
         graphics->DrawLine(pen, 200, 500, 400, 650);
         delete pen;
         delete graphics;
      EndPage(printDlg.hDC);
      EndDoc(printDlg.hDC); 
   }
   if(printDlg.hDevMode) 
      GlobalFree(printDlg.hDevMode);
   if(printDlg.hDevNames) 
      GlobalFree(printDlg.hDevNames);
   if(printDlg.hDC)
      DeleteDC(printDlg.hDC);
   
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
