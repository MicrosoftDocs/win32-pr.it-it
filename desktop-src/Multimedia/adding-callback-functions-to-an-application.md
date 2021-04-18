---
title: Aggiunta di funzioni di callback a un'applicazione
description: Aggiunta di funzioni di callback a un'applicazione
ms.assetid: b7bde1be-b229-4e00-8906-22d7dcf9ea04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d4f5f3dc43227f92305032decaf917bf521d95b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515793"
---
# <a name="adding-callback-functions-to-an-application"></a><span data-ttu-id="a96e7-103">Aggiunta di funzioni di callback a un'applicazione</span><span class="sxs-lookup"><span data-stu-id="a96e7-103">Adding Callback Functions to an Application</span></span>

<span data-ttu-id="a96e7-104">Un'applicazione può registrare le funzioni di callback con la finestra di acquisizione in modo da notificare l'applicazione nelle circostanze seguenti:</span><span class="sxs-lookup"><span data-stu-id="a96e7-104">An application can register callback functions with the capture window so that it notifies the application in the following circumstances:</span></span>

-   <span data-ttu-id="a96e7-105">Lo stato cambia</span><span class="sxs-lookup"><span data-stu-id="a96e7-105">The status changes</span></span>
-   <span data-ttu-id="a96e7-106">Si verificano errori</span><span class="sxs-lookup"><span data-stu-id="a96e7-106">Errors occur</span></span>
-   <span data-ttu-id="a96e7-107">Il frame video e i buffer audio diventano disponibili</span><span class="sxs-lookup"><span data-stu-id="a96e7-107">Video frame and audio buffers become available</span></span>
-   <span data-ttu-id="a96e7-108">L'applicazione deve cedere durante l'acquisizione di flussi</span><span class="sxs-lookup"><span data-stu-id="a96e7-108">The application should yield during streaming capture</span></span>

<span data-ttu-id="a96e7-109">Nell'esempio seguente viene creata una finestra di acquisizione e vengono registrate le funzioni stato, errore, flusso video e callback frame nel ciclo di elaborazione dei messaggi di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a96e7-109">The following example creates a capture window and registers status, error, video stream, and frame callback functions in the message-processing loop of an application.</span></span> <span data-ttu-id="a96e7-110">Include inoltre un'istruzione di esempio per la disabilitazione di una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="a96e7-110">It also includes a sample statement for disabling a callback function.</span></span> <span data-ttu-id="a96e7-111">Gli esempi successivi mostrano semplici funzioni di callback di stato, errore e frame.</span><span class="sxs-lookup"><span data-stu-id="a96e7-111">Subsequent examples show simple status, error, and frame callback functions.</span></span>


```C++
case WM_CREATE: 
{ 
    char    achDeviceName[80] ; 
    char    achDeviceVersion[100] ; 
    char    achBuffer[100] ; 
    WORD    wDriverCount = 0 ; 
    WORD    wIndex ; 
    WORD    wError ; 
    HMENU   hMenu ; 
 
    // Create a capture window using the capCreateCaptureWindow macro.
    ghWndCap = capCreateCaptureWindow((LPSTR)"Capture Window", 
        WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, (HWND) hWnd, (int) 0); 
 
    // Register the error callback function using the 
    // capSetCallbackOnError macro. 
    capSetCallbackOnError(ghWndCap, fpErrorCallback); 
 
    // Register the status callback function using the 
    // capSetCallbackOnStatus macro. 
    capSetCallbackOnStatus(ghWndCap, fpStatusCallback); 
 
    // Register the video-stream callback function using the
    // capSetCallbackOnVideoStream macro. 
    capSetCallbackOnVideoStream(ghWndCap, fpVideoCallback); 
 
    // Register the frame callback function using the
    // capSetCallbackOnFrame macro. 
    capSetCallbackOnFrame(ghWndCap, fpFrameCallback); 
 
    // Connect to a capture driver 

    break; 
} 
case WM_CLOSE: 
{ 
// Use the capSetCallbackOnFrame macro to 
// disable the frame callback. Similar calls exist for the other 
// callback functions.

    capSetCallbackOnFrame(ghWndCap, NULL); 

    break; 
} 
 
```



## <a name="related-topics"></a><span data-ttu-id="a96e7-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a96e7-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a96e7-113">Uso di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="a96e7-113">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




