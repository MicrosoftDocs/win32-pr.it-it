---
title: Creazione di una finestra MCIWnd
description: Creazione di una finestra MCIWnd
ms.assetid: bd45e813-5807-43cd-bef1-03285df9a018
keywords:
- Finestra MCIWnd, creazione
- MCIWndCreate (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c205e87acf3e5f529d4b5cc9c9163b7fe887fe04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297997"
---
# <a name="creating-an-mciwnd-window"></a>Creazione di una finestra MCIWnd

La funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) registra e crea una finestra di MCIWnd. La finestra può essere padre, figlio o finestra popup. Nell'esempio seguente viene creata una finestra MCIWnd come finestra figlio che consente all'utente di controllare la riproduzione fornendo l'accesso ai pulsanti TrackBar e **Play**, **Stop** e **menu** . Nell'esempio viene specificato un handle di una finestra padre e viene specificato **null** per gli stili della finestra, pertanto vengono utilizzati gli stili di finestra predefiniti di WS \_ child, WS \_ Border e WS \_ Visible per creare la finestra MCIWnd.


```C++
// Global variable and constants 
// extern HINSTANCE g_hinst;       instance handle 
// extern HWND g_hwndMCIWnd;       MCIWnd window handle 
 
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, NULL, 
            "sample.avi"); 
        break;    
    } 
    break; 
```



> [!Note]  
> È anche possibile specificare **null** sia per l'handle della finestra padre che per gli stili della finestra. in tal caso, gli stili predefiniti della finestra sarebbero WS \_ OVERLAPPED e WS \_ Visible.

 

 

 




