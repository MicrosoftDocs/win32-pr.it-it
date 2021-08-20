---
title: Automazione della riproduzione per MCIWnd
description: Automazione della riproduzione per MCIWnd
ms.assetid: 7e38e8b1-f56d-4008-83a7-4fba8333e328
keywords:
- Macro MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27328367e58ffa21a2f83abe8ecab9d9a4259e6fb61b7b0a36d3104adaea5d9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065601"
---
# <a name="automating-playback-for-mciwnd"></a>Automazione della riproduzione per MCIWnd

È possibile automatizzare la riproduzione per MCIWnd specificando determinati stili di finestra nella [**funzione MCIWndCreate.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) Per riprodurre il dispositivo, la finestra richiede una finestra padre per elaborare i messaggi di notifica, un'area di riproduzione per riprodurre i file AVI e la notifica delle modifiche della modalità del dispositivo per identificare l'arresto della riproduzione. La finestra non richiede una barra degli strumenti. È possibile impostare queste caratteristiche specificando gli stili appropriati in **MCIWndCreate.**

L'esempio seguente usa i comandi di menu per creare una finestra MCIWnd per riprodurre contenuto da diversi tipi di dispositivi. La **funzione MCIWndCreate** crea la finestra MCIWnd e i dispositivi e i file vengono caricati usando la macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) nei comandi specifici del dispositivo. Al termine della riproduzione di un dispositivo, chiudere il dispositivo trasponendo il messaggio [**\_ NOTIFYMODE MCIWNDM**](mciwndm-notifymode.md) ed emettendo la macro [**MCIWndClose.**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose)


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            dwMCIWndStyle = WS_CHILD |     // child window
                WS_VISIBLE |               // visible
                MCIWNDF_NOTIFYMODE |       // notifies of mode changes
                MCIWNDF_NOPLAYBAR;            // hides toolbar 
            g_hwndMCIWnd = MCIWndCreate(hwnd, 
                g_hinst, dwMCIWndStyle, NULL); 
            break; 
        case IDM_PLAYCDA: 
            LoadNGoMCIWnd(hwnd, "CDAudio"); 
            break; 
        case IDM_PLAYWAVE: 
            LoadNGoMCIWnd(hwnd, "SoundWave.WAV"); 
            break; 
        case IDM_PLAYMIDI: 
            LoadNGoMCIWnd(hwnd, "MIDIFile.MID"); 
            break; 
        case IDM_PLAYAVI: 
            LoadNGoMCIWnd(hwnd, "AVIFile.AVI"); 
            break; 
        case IDM_EXIT: 
            MCIWndDestroy(g_hwndMCIWnd); 
            DestroyWindow(hwnd); 
            break; 
    } 
    break; 
 
case MCIWNDM_NOTIFYMODE: 
    if (lParam == MCI_MODE_STOP)  // device stopped
    { 
        MessageBox(hwnd,"","Closing Device",MB_OK); 
        MCIWndClose(g_hwndMCIWnd); 
    } 
    break; 

// Handle other messages here. 
 
// LoadNGoMCIWnd - automatically loads and plays a multimedia device 
// 
// hwnd -  handle to the parent window 
// lpstr - pointer to device or filename played by device 
// 
// Global variable 
// extern HINSTANCE g_hwndMCIWnd;  instance handle to MCIWnd window 
 
VOID LoadNGoMCIWnd(HWND hwnd, LPSTR lpstr) 
{ 
    MessageBox(hwnd, lpstr, "Loading Device", MB_OK); 
    MCIWndOpen(g_hwndMCIWnd, lpstr, NULL);   // new device in window 
    MCIWndPlay(g_hwndMCIWnd);                // plays device 
} 
```



 

 




