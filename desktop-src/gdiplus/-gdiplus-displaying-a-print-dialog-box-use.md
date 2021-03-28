---
description: Un modo per ottenere un handle di contesto di dispositivo per una stampante consiste nel visualizzare una finestra di dialogo Stampa e consentire all'utente di scegliere una stampante.
ms.assetid: 73a74186-c916-4ad9-b768-6bc887fd5231
title: Visualizzazione di una finestra di dialogo Stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0d40365c36e3e554812ff137475ab7c6405e91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994277"
---
# <a name="displaying-a-print-dialog-box"></a>Visualizzazione di una finestra di dialogo Stampa

Un modo per ottenere un handle di contesto di dispositivo per una stampante consiste nel visualizzare una finestra di dialogo Stampa e consentire all'utente di scegliere una stampante. La funzione [PrintDlg](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) (che visualizza la finestra di dialogo) ha un parametro che è l'indirizzo di una struttura [PrintDlg](/windows/win32/api/commdlg/ns-commdlg-printdlga?redirectedfrom=MSDN) . La struttura PRINTDLG include diversi membri, ma è possibile lasciare la maggior parte di essi impostati sui valori predefiniti. I due membri che è necessario impostare sono **lStructSize** e **Flags**. Impostare **lStructSize** sulla dimensione di una variabile PrintDlg e impostare i **flag** su PD \_ RETURNDC. L'impostazione dei **flag** su PC \_ RETURNDC specifica che si vuole che la funzione PrintDlg occupi il campo **HDC** con un handle di contesto di dispositivo per la stampante scelta dall'utente.


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



 

 
