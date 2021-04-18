---
description: Implementazione di una barra di ricerca
ms.assetid: 384f0732-e0c5-4b1f-b590-195e0acf90e1
title: Implementazione di una barra di ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd3f2440c011267c792c79c8bc3550926c5767f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522210"
---
# <a name="implementing-a-seek-bar"></a><span data-ttu-id="bd1e5-103">Implementazione di una barra di ricerca</span><span class="sxs-lookup"><span data-stu-id="bd1e5-103">Implementing a Seek Bar</span></span>

<span data-ttu-id="bd1e5-104">In questa sezione viene descritto come implementare una barra di ricerca per un'applicazione Media Player.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-104">This section describes how to implement a seek bar for a media-player application.</span></span> <span data-ttu-id="bd1e5-105">La barra di ricerca viene implementata come controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-105">The seek bar is implemented as a trackbar control.</span></span> <span data-ttu-id="bd1e5-106">Per una panoramica della ricerca in DirectShow, vedere [seeking the Filter Graph](seeking-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="bd1e5-106">For an overview of seeking in DirectShow, see [Seeking the Filter Graph](seeking-the-filter-graph.md).</span></span>

<span data-ttu-id="bd1e5-107">All'avvio dell'applicazione, inizializzare il TrackBar:</span><span class="sxs-lookup"><span data-stu-id="bd1e5-107">When the application starts, initialize the trackbar:</span></span>


```C++
void InitSlider(HWND hwnd) 
{
    // Initialize the trackbar range, but disable the 
    // control until the user opens a file.
    hScroll = GetDlgItem(hwnd, IDC_SLIDER1);
    EnableWindow(hScroll, FALSE);
    SendMessage(hScroll, TBM_SETRANGE, TRUE, MAKELONG(0, 100));
}
```



<span data-ttu-id="bd1e5-108">Il TrackBar viene disabilitato fino a quando l'utente non apre un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-108">The trackbar is disabled until the user opens a media file.</span></span> <span data-ttu-id="bd1e5-109">L'intervallo TrackBar è impostato da 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-109">The trackbar range is set from 0 to 100.</span></span> <span data-ttu-id="bd1e5-110">Durante la riproduzione del file, l'applicazione calcolerà la posizione di riproduzione come percentuale della durata del file e aggiornerà il TrackBar di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-110">During file playback, the application will calculate the playback position as a percentage of the file duration, and update the trackbar accordingly.</span></span> <span data-ttu-id="bd1e5-111">Ad esempio, la posizione di TrackBar "50" corrisponde sempre al centro del file.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-111">For example, trackbar position "50" always corresponds to the middle of the file.</span></span>

<span data-ttu-id="bd1e5-112">Quando l'utente apre un file, compila un grafico di riproduzione file usando **RenderFile**.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-112">When the user opens a file, build a file-playback graph using **RenderFile**.</span></span> <span data-ttu-id="bd1e5-113">Il codice per questa operazione viene illustrato in [come riprodurre un file](how-to-play-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="bd1e5-113">The code for this is shown in [How To Play a File](how-to-play-a-file.md).</span></span> <span data-ttu-id="bd1e5-114">Eseguire quindi una query su Filter Graph Manager per l'interfaccia **IMediaSeeking** e archiviare il puntatore di interfaccia:</span><span class="sxs-lookup"><span data-stu-id="bd1e5-114">Then query the Filter Graph Manager for the **IMediaSeeking** interface and store the interface pointer:</span></span>


```C++
IMediaSeeking *g_pSeek = 0;
hr = pGraph->QueryInterface(IID_IMediaSeeking, (void**)&g_pSeek);
```



<span data-ttu-id="bd1e5-115">Per determinare se il file è ricercabile, chiamare il metodo [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) o [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="bd1e5-115">To determine whether the file is seekable, call either the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method or the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span> <span data-ttu-id="bd1e5-116">Questi metodi eseguono quasi la stessa operazione, ma la loro semantica è leggermente diversa.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-116">These methods do almost the same thing, but their semantics are slightly different.</span></span> <span data-ttu-id="bd1e5-117">L'esempio seguente usa **CheckCapabilites**:</span><span class="sxs-lookup"><span data-stu-id="bd1e5-117">The following example uses **CheckCapabilites**:</span></span>


```C++
// Determine if the source is seekable.
BOOL  bCanSeek = FALSE;
DWORD caps = AM_SEEKING_CanSeekAbsolute | AM_SEEKING_CanGetDuration; 
bCanSeek = (S_OK == pSeek->CheckCapabilities(&caps));
if (bCanSeek)
{
    // Enable the trackbar.
    EnableWindow(hScroll, TRUE);

    // Find the file duration.
    pSeek->GetDuration(&g_rtTotalTime);
}
```



<span data-ttu-id="bd1e5-118">Il \_ \_ flag CanSeekAbsolute seeking controlla se il file di origine è ricercabile e il \_ flag CanGetDuration seeking \_ Controlla se è possibile determinare in anticipo la durata del file.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-118">The AM\_SEEKING\_CanSeekAbsolute flag checks whether the source file is seekable, and the AM\_SEEKING\_CanGetDuration flag checks whether the duration of the file can be determined in advance.</span></span> <span data-ttu-id="bd1e5-119">Se entrambe le funzionalità sono supportate, l'applicazione Abilita il TrackBar e recupera la durata del file.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-119">If both of the capabilities are supported, the application enables the trackbar and retrieves the file duration.</span></span>

<span data-ttu-id="bd1e5-120">Se il grafico è ricercabile, l'applicazione userà un timer per aggiornare la posizione di TrackBar durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-120">If the graph is seekable, the application will use a timer to update the trackbar position during playback.</span></span> <span data-ttu-id="bd1e5-121">Quando si esegue il grafico del filtro per riprodurre il file, avviare l'evento del timer chiamando una delle funzioni timer di Windows, ad esempio **setimer**.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-121">When you run the filter graph to play the file, start the timer event by calling one of the Windows timer functions, such as **SetTimer**.</span></span> <span data-ttu-id="bd1e5-122">Per ulteriori informazioni sui timer, vedere l'argomento "timer" in Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-122">For more information about timers, see the topic "Timers" in the Platform SDK.</span></span>


```C++
void StartPlayback(HWND hwnd) 
{
    pControl->Run();
    if (bCanSeek)
    {
        StopTimer(); // Make sure an old timer is not still active.
        nTimerID = SetTimer(hwnd, IDT_TIMER1, TICK_FREQ, (TIMERPROC)NULL);
        if (nTimerID == 0)
        {
            /* Handle Error */
        }
    }
}

void StopTimer() 
{
    if (wTimerID != 0)
    {
        KillTimer(g_hwnd, wTimerID);
        wTimerID = 0;
    }
}
```



<span data-ttu-id="bd1e5-123">Utilizzare l'evento timer per aggiornare la posizione del TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-123">Use the timer event to update the position of the trackbar.</span></span> <span data-ttu-id="bd1e5-124">Chiamare [**IMediaSeeking:: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) per recuperare la posizione di riproduzione ribes, quindi calcolare la posizione come percentuale della durata del file:</span><span class="sxs-lookup"><span data-stu-id="bd1e5-124">Call [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) to retrieve the currant playback position, and then calculate the position as a percentage of the file duration:</span></span>


```C++
case WM_TIMER:
    if (wParam == IDT_TIMER1)
    {
        // Timer should not be running unless we really can seek.
        ASSERT(bCanSeek == TRUE);

        REFERENCE_TIME timeNow;
        if (SUCCEEDED(pSeek->GetCurrentPosition(&timeNow)))
        {
            long sliderTick = (long)((timeNow * 100) / g_rtTotalTime);
            SendMessage( hScroll, TBM_SETPOS, TRUE, sliderTick );
        }
    }
    break;
```



<span data-ttu-id="bd1e5-125">L'utente può anche spostare il TrackBar per cercare il file.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-125">The user can also move the trackbar to seek the file.</span></span> <span data-ttu-id="bd1e5-126">Quando l'utente trascina o fa clic sul controllo TrackBar, l'applicazione riceve un \_ evento HSCROLL di WM.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-126">When the user drags or clicks the trackbar control, the application receives a WM\_HSCROLL event.</span></span> <span data-ttu-id="bd1e5-127">La parola bassa del parametro *wParam* è il messaggio di notifica TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-127">The low word of the *wParam* parameter is the trackbar notification message.</span></span> <span data-ttu-id="bd1e5-128">Ad esempio, TB \_ ENDTRACK viene inviato alla fine dell'azione TrackBar e TB \_ THUMBTRACK viene inviato continuamente mentre l'utente trascina il TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-128">For example, TB\_ENDTRACK is sent at the end of the trackbar action, and TB\_THUMBTRACK is sent continuously while the user drags the trackbar.</span></span> <span data-ttu-id="bd1e5-129">Il codice seguente illustra un modo per gestire il \_ messaggio HSCROLL di WM:</span><span class="sxs-lookup"><span data-stu-id="bd1e5-129">The following code shows one way to handle the WM\_HSCROLL message:</span></span>


```C++
static OAFilterState state;
static BOOL bStartOfScroll = TRUE;

case WM_HSCROLL:
    short int userReq = LOWORD(wParam);
    if (userReq == TB_ENDTRACK || userReq == TB_THUMBTRACK)
    {
        DWORD dwPosition  = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
        // Pause when the scroll action begins.
        if (bStartOfScroll) 
        {
            pControl->GetState(10, &state);
            bStartOfScroll = FALSE;
            pControl->Pause();
        }
        // Update the position continuously.
        REFERENCE_TIME newTime = (g_rtTotalTime/100) * dwPosition;
        pSeek->SetPositions(&newTime, AM_SEEKING_AbsolutePositioning,
            NULL, AM_SEEKING_NoPositioning);

        // Restore the state at the end.
        if (userReq == TB_ENDTRACK)
        {
            if (state == State_Stopped)
                pControl->Stop();
            else if (state == State_Running) 
                pControl->Run();
            bStartOfScroll = TRUE;
        }
    }
}
```



<span data-ttu-id="bd1e5-130">Se l'utente trascina il TrackBar, l'applicazione emette una serie di comandi Seek, uno per ogni \_ messaggio THUMBTRACK TB che riceve.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-130">If the user drags the trackbar, the application issues a series of seek commands, one for each TB\_THUMBTRACK message that it receives.</span></span> <span data-ttu-id="bd1e5-131">Per fare in modo che le operazioni di ricerca siano più agevoli possibile, l'applicazione sospende il grafo.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-131">To make the seek operations as smooth as possible, the application pauses the graph.</span></span> <span data-ttu-id="bd1e5-132">La sospensione del grafico interrompe la riproduzione ma garantisce che la finestra video venga aggiornata.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-132">Pausing the graph halts playback but ensures that the video window is updated.</span></span> <span data-ttu-id="bd1e5-133">Quando l'applicazione riceve il \_ messaggio TB ENDTRACK, ripristina lo stato originale del grafico.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-133">When the application receives the TB\_ENDTRACK message, it restores the graph to its original state.</span></span>

 

 



