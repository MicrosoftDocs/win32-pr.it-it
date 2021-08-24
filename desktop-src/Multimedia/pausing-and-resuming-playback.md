---
title: Sospensione e ripresa della riproduzione
description: Sospensione e ripresa della riproduzione
ms.assetid: f5a7ef22-993c-4aab-bab0-2700289da7a7
keywords:
- Macro MCIWndPause
- Macro MCIWndResume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce70a95000cda6fc471967e5075b16fe7bad837c71eed4e6216ddeaddddc4508
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805971"
---
# <a name="pausing-and-resuming-playback"></a>Sospensione e ripresa della riproduzione

È possibile interrompere la riproduzione di un dispositivo o di un file associato a una finestra MCIWnd usando la macro [**MCIWndPause.**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) È quindi possibile riavviare la riproduzione usando la macro [**MCIWndResume.**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) Se il dispositivo non supporta la ripresa o se si verifica un errore, è possibile usare la macro [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) per riavviare la riproduzione.

L'esempio seguente crea una finestra MCIWnd e riproduce un file AVI. I comandi di menu Sospendi e riprendi sono disponibili per interrompere e riavviare la riproduzione.

Gli stili della finestra MCIWnd vengono modificati temporaneamente usando la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) per impedire la visualizzazione di una finestra di dialogo di errore MCI se [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) ha esito negativo.


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND:             // creates and plays clip 
            g_hwndMCIWnd = MCIWndCreate(hwnd,  
                g_hinst,                      
                WS_CHILD | WS_VISIBLE |    // standard styles
                MCIWNDF_NOPLAYBAR |        // hides toolbar 
                MCIWNDF_NOTIFYMODE,        // notifies of mode changes
                "sample.avi"); 
 
            MCIWndPlay(g_hwndMCIWnd); 
            break;    
        case IDM_PAUSEMCIWND:              // pauses playback 
            MCIWndPause(g_hwndMCIWnd); 
            MessageBox(hwnd, "MCIWnd", "Pausing Playback", MB_OK); 
            break; 
        case IDM_RESUMEMCIWND:          // resumes playback 
            MCIWndChangeStyles(      // hides error dialog messages
                g_hwndMCIWnd,        // MCIWnd window
                MCIWNDF_NOERRORDLG,  // mask of style to change
                MCIWNDF_NOERRORDLG); // suppresses MCI error dialogs 
 
            lResult = MCIWndResume(g_hwndMCIWnd); 
 
            if(lResult){                   // device doesn't resume 
                MessageBox(hwnd, "MCIWnd", 
                    "Resume with Stop and Play", MB_OK); 
                MCIWndStop(g_hwndMCIWnd); 
                MCIWndPlay(g_hwndMCIWnd); 
 
                MCIWndChangeStyles(        // resumes original styles
                    g_hwndMCIWnd, 
                    MCIWNDF_NOERRORDLG, 
                    NULL); 
        } 
        break; 
    } 
    break; 
 
// Handle other messages here. 
```



 

 




