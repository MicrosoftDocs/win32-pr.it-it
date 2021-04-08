---
title: Acquisizione video un approccio minimo
description: Acquisizione video un approccio minimo
ms.assetid: e39ff590-69c0-4927-90c2-786c6082068f
keywords:
- Video per Windows (VFW), acquisizione video
- VFW (video per Windows), acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a65d5d5bbdc00dfd947c5d917e514d72e3ac069
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872401"
---
# <a name="video-capture-a-minimal-approach"></a><span data-ttu-id="13523-105">Acquisizione video: approccio minimo</span><span class="sxs-lookup"><span data-stu-id="13523-105">Video Capture: A Minimal Approach</span></span>

<span data-ttu-id="13523-106">Acquisizione video digitalizza un flusso di dati video e audio e lo archivia in un disco rigido o in un altro tipo di dispositivo di archiviazione permanente.</span><span class="sxs-lookup"><span data-stu-id="13523-106">Video capture digitizes a stream of video and audio data, and stores it on a hard disk or some other type of persistent storage device.</span></span> <span data-ttu-id="13523-107">In questa sezione viene descritto come aggiungere un semplice modulo di acquisizione video a un'applicazione utilizzando tre istruzioni di codice.</span><span class="sxs-lookup"><span data-stu-id="13523-107">This section describes how to add a simple form of video capture to an application using three statements of code.</span></span> <span data-ttu-id="13523-108">Viene inoltre descritto come terminare o interrompere una sessione di acquisizione inviando messaggi alla finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="13523-108">It also describes how to end or abort a capture session by sending messages to the capture window.</span></span>

<span data-ttu-id="13523-109">Una finestra di acquisizione di AVICap gestisce i dettagli dell'acquisizione audio e video di streaming in file AVI.</span><span class="sxs-lookup"><span data-stu-id="13523-109">An AVICap capture window handles the details of streaming audio and video capture to AVI files.</span></span> <span data-ttu-id="13523-110">Questo consente di liberare l'applicazione dal coinvolgimento del formato di file AVI, della gestione del buffer audio e video e dell'accesso di basso livello ai driver di dispositivo audio e video.</span><span class="sxs-lookup"><span data-stu-id="13523-110">This frees your application from involvement in the AVI file format, video and audio buffer management, and the low-level access of video and audio device drivers.</span></span> <span data-ttu-id="13523-111">AVICap fornisce un'interfaccia flessibile per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="13523-111">AVICap provides a flexible interface for applications.</span></span> <span data-ttu-id="13523-112">È possibile aggiungere l'acquisizione video all'applicazione usando solo le righe di codice seguenti:</span><span class="sxs-lookup"><span data-stu-id="13523-112">You can add video capture to your application, using only the following lines of code:</span></span>


```C++
hWndC = capCreateCaptureWindow ( "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE , 0, 0, 160, 120, hwndParent, nID);

SendMessage (hWndC, WM_CAP_DRIVER_CONNECT, 0 /* wIndex */, 0L);

SendMessage (hWndC, WM_CAP_SEQUENCE, 0, 0L);
 
```



<span data-ttu-id="13523-113">È disponibile anche un'interfaccia macro che fornisce un'alternativa all'uso della funzione [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) e migliora la leggibilità di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="13523-113">A macro interface is also available that provides an alternative to using the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function and improves the readability of an application.</span></span> <span data-ttu-id="13523-114">Nell'esempio seguente viene usata l'interfaccia macro per aggiungere un'acquisizione video a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="13523-114">The following example uses the macro interface to add video capture to an application.</span></span>


```C++
hWndC = capCreateCaptureWindow (   "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE ,   0, 0, 160, 120, hwndParent, nID);

capDriverConnect (hWndC, 0);

capCaptureSequence (hWndC); 
 
```



<span data-ttu-id="13523-115">Dopo che l'applicazione crea una finestra di acquisizione della classe della finestra AVICap e la connette a un driver video, la finestra di acquisizione è pronta per l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="13523-115">After your application creates a capture window of the AVICap window class and connects it to a video driver, the capture window is ready to capture data.</span></span> <span data-ttu-id="13523-116">A questo punto, l'applicazione può semplicemente inviare il messaggio di [**\_ \_ sequenza Cap WM**](wm-cap-sequence.md) (o la macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) ) per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="13523-116">At this point, your application can simply send the [**WM\_CAP\_SEQUENCE**](wm-cap-sequence.md) message (or the [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) macro) to begin capturing.</span></span>

<span data-ttu-id="13523-117">Con le impostazioni predefinite, WM \_ Cap \_ Sequence avvia l'acquisizione di input audio e video in un file denominato CAPTURE.AVI.</span><span class="sxs-lookup"><span data-stu-id="13523-117">Using default settings, WM\_CAP\_SEQUENCE initiates the capture of video and audio input to a file named CAPTURE.AVI.</span></span> <span data-ttu-id="13523-118">L'acquisizione continua fino a quando non si verifica uno degli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="13523-118">Capture continues until one of the following events occurs:</span></span>

-   <span data-ttu-id="13523-119">L'utente preme il tasto ESC o il pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="13523-119">The user presses the ESC key or a mouse button.</span></span>
-   <span data-ttu-id="13523-120">L'applicazione interrompe o interrompe l'operazione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="13523-120">Your application stops or aborts capture operation.</span></span>
-   <span data-ttu-id="13523-121">Il disco diventa pieno.</span><span class="sxs-lookup"><span data-stu-id="13523-121">The disk becomes full.</span></span>

<span data-ttu-id="13523-122">In un'applicazione, è possibile arrestare il flusso di dati acquisiti in un file inviando il messaggio di [**\_ \_ arresto del Cap WM**](wm-cap-stop.md) (o la macro [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) ) a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="13523-122">In an application, you can stop streaming captured data to a file by sending the [**WM\_CAP\_STOP**](wm-cap-stop.md) (or the [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) macro) message to a capture window.</span></span> <span data-ttu-id="13523-123">È anche possibile interrompere l'operazione di acquisizione inviando il messaggio [**WM \_ Cap \_ Abort**](wm-cap-abort.md) (o la macro [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) ) a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="13523-123">You can also abort the capture operation by sending the [**WM\_CAP\_ABORT**](wm-cap-abort.md) message (or the [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) macro) to a capture window.</span></span>

 

 