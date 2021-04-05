---
title: Registrazione con i controlli MCIWnd
description: Registrazione con i controlli MCIWnd
ms.assetid: 65a57400-aeea-4a27-8d51-37d3d9e9bd55
keywords:
- MCIWndCreate (funzione)
- MCIWndNew (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814bd9f92b895c03ccbb073f830dbf31dcd2e3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955183"
---
# <a name="recording-with-mciwnd-controls"></a><span data-ttu-id="b5598-105">Registrazione con i controlli MCIWnd</span><span class="sxs-lookup"><span data-stu-id="b5598-105">Recording with MCIWnd Controls</span></span>

<span data-ttu-id="b5598-106">L'esempio seguente registra l'audio della forma d'onda usando i controlli predefiniti della finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="b5598-106">The following example records waveform audio using the built-in controls of the MCIWnd window.</span></span> <span data-ttu-id="b5598-107">Nell'esempio viene creata una finestra MCIWnd usando lo \_ stile della finestra record MCIWNDF con la funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) per aggiungere un pulsante di **registrazione** alla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="b5598-107">The example creates an MCIWnd window by using the MCIWNDF\_RECORD window style with the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function to add a **Record** button to the toolbar.</span></span> <span data-ttu-id="b5598-108">La macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) indica che un nuovo file è associato alla finestra MCIWnd e che un dispositivo audio Waveform fornirà il contenuto.</span><span class="sxs-lookup"><span data-stu-id="b5598-108">The [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro indicates a new file is associated with the MCIWnd window and that a waveform-audio device will provide its content.</span></span> <span data-ttu-id="b5598-109">Un secondo comando di menu, IDM \_ SAVEMCIWND, consente all'utente di salvare la registrazione e selezionare un nome di file usando la macro [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) .</span><span class="sxs-lookup"><span data-stu-id="b5598-109">A second menu command, IDM\_SAVEMCIWND, lets the user save the recording and select a filename by using the [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) macro.</span></span>


```C++
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, 
            WS_VISIBLE | MCIWNDF_RECORD, NULL); 
        MCIWndNew(g_hwndMCIWnd, "waveaudio"); 
        break;    
    case IDM_SAVEMCIWND: 
        MCIWndSaveDialog(g_hwndMCIWnd); 
        break; 
    } 
```



 

 




