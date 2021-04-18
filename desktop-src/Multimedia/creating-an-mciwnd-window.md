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
# <a name="creating-an-mciwnd-window"></a><span data-ttu-id="168d0-105">Creazione di una finestra MCIWnd</span><span class="sxs-lookup"><span data-stu-id="168d0-105">Creating an MCIWnd Window</span></span>

<span data-ttu-id="168d0-106">La funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) registra e crea una finestra di MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="168d0-106">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function registers and creates an MCIWnd window.</span></span> <span data-ttu-id="168d0-107">La finestra può essere padre, figlio o finestra popup.</span><span class="sxs-lookup"><span data-stu-id="168d0-107">The window can be a parent, child, or pop-up window.</span></span> <span data-ttu-id="168d0-108">Nell'esempio seguente viene creata una finestra MCIWnd come finestra figlio che consente all'utente di controllare la riproduzione fornendo l'accesso ai pulsanti TrackBar e **Play**, **Stop** e **menu** .</span><span class="sxs-lookup"><span data-stu-id="168d0-108">The following example creates an MCIWnd window as a child window and lets the user control playback by providing access to the trackbar and the **Play**, **Stop**, and **Menu** buttons.</span></span> <span data-ttu-id="168d0-109">Nell'esempio viene specificato un handle di una finestra padre e viene specificato **null** per gli stili della finestra, pertanto vengono utilizzati gli stili di finestra predefiniti di WS \_ child, WS \_ Border e WS \_ Visible per creare la finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="168d0-109">The example specifies a handle of a parent window and specifies **NULL** for the window styles, so the default window styles of WS\_CHILD, WS\_BORDER, and WS\_VISIBLE are used to create the MCIWnd window.</span></span>


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
> <span data-ttu-id="168d0-110">È anche possibile specificare **null** sia per l'handle della finestra padre che per gli stili della finestra. in tal caso, gli stili predefiniti della finestra sarebbero WS \_ OVERLAPPED e WS \_ Visible.</span><span class="sxs-lookup"><span data-stu-id="168d0-110">You could also specify **NULL** for both the parent window handle and the window styles, in which case the default window styles would be WS\_OVERLAPPED and WS\_VISIBLE.</span></span>

 

 

 




