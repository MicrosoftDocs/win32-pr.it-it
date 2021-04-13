---
description: MFPlay è un'API per la creazione di applicazioni per la riproduzione di file multimediali in C++.
ms.assetid: 55612f49-5995-4bdf-aa12-8a853e5a2b24
title: Introduzione con MFPlay
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9e0405d3138a22e0d20e94849d416b29d62945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484061"
---
# <a name="getting-started-with-mfplay"></a><span data-ttu-id="90a49-103">Introduzione con MFPlay</span><span class="sxs-lookup"><span data-stu-id="90a49-103">Getting Started with MFPlay</span></span>

<span data-ttu-id="90a49-104">\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="90a49-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="90a49-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="90a49-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="90a49-106">\]</span><span class="sxs-lookup"><span data-stu-id="90a49-106">\]</span></span>

<span data-ttu-id="90a49-107">MFPlay è un'API per la creazione di applicazioni per la riproduzione di file multimediali in C++.</span><span class="sxs-lookup"><span data-stu-id="90a49-107">MFPlay is an API for creating media playback applications in C++.</span></span>

<span data-ttu-id="90a49-108">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="90a49-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="90a49-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90a49-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="90a49-110">Informazioni su MFPlay</span><span class="sxs-lookup"><span data-stu-id="90a49-110">About MFPlay</span></span>](#about-mfplay)
-   [<span data-ttu-id="90a49-111">Riproduzione di un file multimediale</span><span class="sxs-lookup"><span data-stu-id="90a49-111">Playing a Media File</span></span>](#playing-a-media-file)
-   [<span data-ttu-id="90a49-112">Controllo della riproduzione</span><span class="sxs-lookup"><span data-stu-id="90a49-112">Controlling Playback</span></span>](#controlling-playback)
-   [<span data-ttu-id="90a49-113">Ricezione di eventi dal lettore</span><span class="sxs-lookup"><span data-stu-id="90a49-113">Receiving Events From the Player</span></span>](#receiving-events-from-the-player)
-   [<span data-ttu-id="90a49-114">Recupero di informazioni su un file multimediale</span><span class="sxs-lookup"><span data-stu-id="90a49-114">Getting Information About a Media File</span></span>](#getting-information-about-a-media-file)
-   [<span data-ttu-id="90a49-115">Gestione della riproduzione video</span><span class="sxs-lookup"><span data-stu-id="90a49-115">Managing Video Playback</span></span>](#managing-video-playback)
-   [<span data-ttu-id="90a49-116">Limitazioni di MFPlay</span><span class="sxs-lookup"><span data-stu-id="90a49-116">Limitations of MFPlay</span></span>](#limitations-of-mfplay)
-   [<span data-ttu-id="90a49-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="90a49-117">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="90a49-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90a49-118">Requirements</span></span>

<span data-ttu-id="90a49-119">MFPlay richiede Windows 7.</span><span class="sxs-lookup"><span data-stu-id="90a49-119">MFPlay requires Windows 7.</span></span>

## <a name="about-mfplay"></a><span data-ttu-id="90a49-120">Informazioni su MFPlay</span><span class="sxs-lookup"><span data-stu-id="90a49-120">About MFPlay</span></span>

<span data-ttu-id="90a49-121">MFPlay dispone di un semplice modello di programmazione, fornendo il set di base di funzionalità necessarie per la maggior parte delle applicazioni di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="90a49-121">MFPlay has a simple programming model, while providing the core set of features that most playback applications need.</span></span> <span data-ttu-id="90a49-122">Un'applicazione crea un oggetto *Player* che controlla la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="90a49-122">An application creates a *player* object that controls playback.</span></span> <span data-ttu-id="90a49-123">Per riprodurre un file multimediale, l'oggetto Player crea un *elemento multimediale*, che può essere usato per ottenere informazioni sul contenuto del file multimediale.</span><span class="sxs-lookup"><span data-stu-id="90a49-123">To play a media file, the player object creates a *media item*, which can be used to get information about the contents of the media file.</span></span> <span data-ttu-id="90a49-124">L'applicazione controlla la riproduzione tramite metodi nell'interfaccia [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) dell'oggetto Player.</span><span class="sxs-lookup"><span data-stu-id="90a49-124">The application controls playback through methods on the player object's [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span> <span data-ttu-id="90a49-125">Facoltativamente, l'applicazione può ottenere le notifiche degli eventi tramite un'interfaccia di callback. il diagramma seguente illustra questo processo.</span><span class="sxs-lookup"><span data-stu-id="90a49-125">Optionally, the application can get event notifications through a callback interface The following diagram illustrates this process.</span></span>

![diagramma concettuale: l'applicazione e il giocatore puntano l'uno all'altro, entrambi puntano a un elemento multimediale, che punta al file multimediale](images/mfplay.png)

## <a name="playing-a-media-file"></a><span data-ttu-id="90a49-127">Riproduzione di un file multimediale</span><span class="sxs-lookup"><span data-stu-id="90a49-127">Playing a Media File</span></span>

<span data-ttu-id="90a49-128">Per riprodurre un file multimediale, chiamare la funzione [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="90a49-128">To play a media file, call the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span>


```C++
// Global variables
IMFPMediaPlayer *g_pPlayer = NULL;

const WCHAR *sURL = L"C:\\Users\\Public\\Videos\\example.wmv";

HRESULT PlayVideo(HWND hwnd, const WCHAR* sURL)
{
    // Create the player object and play a video file.

    return MFPCreateMediaPlayer(
        sURL,
        TRUE,   // Start playback automatically?
        0,      // Flags.
        NULL,   // Callback pointer.
        hwnd,
        &g_pPlayer
        );
}
```



<span data-ttu-id="90a49-129">La funzione [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) crea una nuova istanza dell'oggetto MFPlay Player.</span><span class="sxs-lookup"><span data-stu-id="90a49-129">The [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function creates a new instance of the MFPlay player object.</span></span> <span data-ttu-id="90a49-130">La funzione accetta i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="90a49-130">The function takes the following parameters:</span></span>

-   <span data-ttu-id="90a49-131">Il primo parametro è l'URL del file da aprire.</span><span class="sxs-lookup"><span data-stu-id="90a49-131">The first parameter is the URL of the file to open.</span></span> <span data-ttu-id="90a49-132">Può trattarsi di un file locale o di un file in un server multimediale.</span><span class="sxs-lookup"><span data-stu-id="90a49-132">This can be a local file or a file on a media server.</span></span>
-   <span data-ttu-id="90a49-133">Il secondo parametro specifica se la riproduzione viene avviata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="90a49-133">The second parameter specifies whether playback starts automatically.</span></span> <span data-ttu-id="90a49-134">Impostando questo rndSrc su **true**, il file verrà riprodotto non appena MFPlay lo carica.</span><span class="sxs-lookup"><span data-stu-id="90a49-134">By setting this paremeter to **TRUE**, the file will play as soon as MFPlay loads it.</span></span>
-   <span data-ttu-id="90a49-135">Il terzo parametro imposta varie opzioni.</span><span class="sxs-lookup"><span data-stu-id="90a49-135">The third parameter sets various options.</span></span> <span data-ttu-id="90a49-136">Per le opzioni predefinite, passare zero (0).</span><span class="sxs-lookup"><span data-stu-id="90a49-136">For the default options, pass zero (0).</span></span>
-   <span data-ttu-id="90a49-137">Il quarto parametro è un puntatore a un'interfaccia di callback facoltativa.</span><span class="sxs-lookup"><span data-stu-id="90a49-137">The fourth parameter is a pointer to an optional callback interface.</span></span> <span data-ttu-id="90a49-138">Questo parametro può essere **null**, come illustrato.</span><span class="sxs-lookup"><span data-stu-id="90a49-138">This parameter can be **NULL**, as shown.</span></span> <span data-ttu-id="90a49-139">Il callback è descritto nella sezione [ricezione di eventi dal lettore](#receiving-events-from-the-player).</span><span class="sxs-lookup"><span data-stu-id="90a49-139">The callback is described in the section [Receiving Events From the Player](#receiving-events-from-the-player).</span></span>
-   <span data-ttu-id="90a49-140">Il quinto parametro è un handle per la finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="90a49-140">The fifth parameter is a handle to the application window.</span></span> <span data-ttu-id="90a49-141">Se il file multimediale contiene un flusso video, il video verrà visualizzato all'interno dell'area client di questa finestra.</span><span class="sxs-lookup"><span data-stu-id="90a49-141">If the media file contains a video stream, the video will appear inside the client area of this window.</span></span> <span data-ttu-id="90a49-142">Per la riproduzione solo audio, questo parametro può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="90a49-142">For audio-only playback, this parameter can be **NULL**.</span></span>

<span data-ttu-id="90a49-143">L'ultimo parametro riceve un puntatore all'interfaccia [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) dell'oggetto Player.</span><span class="sxs-lookup"><span data-stu-id="90a49-143">The last parameter receives a pointer to the player object's [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span>

<span data-ttu-id="90a49-144">Prima di arrestare l'applicazione, assicurarsi di rilasciare il puntatore [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="90a49-144">Before the application shuts down, be sure to release the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) pointer.</span></span> <span data-ttu-id="90a49-145">Questa operazione può essere eseguita nel gestore di messaggi **WM \_ Close** .</span><span class="sxs-lookup"><span data-stu-id="90a49-145">You can do this in your **WM\_CLOSE** message handler.</span></span>


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



> [!Note]  
> <span data-ttu-id="90a49-146">Questo esempio usa la funzione [SafeRelease](saferelease.md) per rilasciare i puntatori a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="90a49-146">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

<span data-ttu-id="90a49-147">Per una semplice riproduzione video, questo è tutto il codice necessario.</span><span class="sxs-lookup"><span data-stu-id="90a49-147">For simple video playback, that's all the code you need.</span></span> <span data-ttu-id="90a49-148">Nella parte restante di questa esercitazione verrà illustrato come aggiungere altre funzionalità, a partire da come controllare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="90a49-148">The rest of this tutorial will show how to add more features, starting with how to control playback.</span></span>

## <a name="controlling-playback"></a><span data-ttu-id="90a49-149">Controllo della riproduzione</span><span class="sxs-lookup"><span data-stu-id="90a49-149">Controlling Playback</span></span>

<span data-ttu-id="90a49-150">Il codice illustrato nella sezione precedente riproduce il file multimediale fino a quando non raggiunge la fine del file.</span><span class="sxs-lookup"><span data-stu-id="90a49-150">The code shown in the previous section will play the media file until it reaches the end of the file.</span></span> <span data-ttu-id="90a49-151">È possibile arrestare e avviare la riproduzione chiamando i metodi seguenti sull'interfaccia [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) :</span><span class="sxs-lookup"><span data-stu-id="90a49-151">You can stop and start playback by calling the following methods on the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface:</span></span>

-   <span data-ttu-id="90a49-152">[**IMFPMediaPlayer::P ause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) sospende la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="90a49-152">[**IMFPMediaPlayer::Pause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) pauses playback.</span></span> <span data-ttu-id="90a49-153">Mentre la riproduzione viene sospesa, viene visualizzato il frame video più recente e l'audio è invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="90a49-153">While playback is paused, the most recent video frame is displayed, and audio is silent.</span></span>
-   <span data-ttu-id="90a49-154">[**IMFPMediaPlayer:: Stop**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) arresta la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="90a49-154">[**IMFPMediaPlayer::Stop**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) stops playback.</span></span> <span data-ttu-id="90a49-155">Non viene visualizzato alcun video e la posizione di riproduzione viene reimpostata all'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="90a49-155">No video is displayed, and the playback position resets to the start of the file.</span></span>
-   <span data-ttu-id="90a49-156">[**IMFPMediaPlayer::P Lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) riprende la riproduzione dopo l'arresto o la sospensione.</span><span class="sxs-lookup"><span data-stu-id="90a49-156">[**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) resumes playback after stopping or pausing.</span></span>

<span data-ttu-id="90a49-157">Il codice seguente sospende o riprende la riproduzione quando si preme la **barra spaziatrice**.</span><span class="sxs-lookup"><span data-stu-id="90a49-157">The following code pauses or resumes playback when you press the **SPACEBAR**.</span></span>


```C++
//-------------------------------------------------------------------
// OnKeyDown
//
// Handles the WM_KEYDOWN message.
//-------------------------------------------------------------------

void OnKeyDown(HWND hwnd, UINT vk, BOOL fDown, int cRepeat, UINT flags)
{
    HRESULT hr = S_OK;

    switch (vk)
    {
    case VK_SPACE:

        // Toggle between playback and paused/stopped.
        if (g_pPlayer)
        {
            MFP_MEDIAPLAYER_STATE state = MFP_MEDIAPLAYER_STATE_EMPTY;
            
            g_pPlayer->GetState(&state);

            if (state == MFP_MEDIAPLAYER_STATE_PAUSED ||  
                state == MFP_MEDIAPLAYER_STATE_STOPPED)
            {
                g_pPlayer->Play();
            }
            else if (state == MFP_MEDIAPLAYER_STATE_PLAYING)
            {
                g_pPlayer->Pause();
            }
        }
        break;
    }
}
```



<span data-ttu-id="90a49-158">In questo esempio viene chiamato il metodo [**IMFPMediaPlayer:: GetState**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) per ottenere lo stato di riproduzione corrente (sospeso, interrotto o in riproduzione), che viene sospeso o ripreso di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="90a49-158">This example calls the [**IMFPMediaPlayer::GetState**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) method to get the current playback state (paused, stopped, or playing) and pauses or resumes accordingly.</span></span>

## <a name="receiving-events-from-the-player"></a><span data-ttu-id="90a49-159">Ricezione di eventi dal lettore</span><span class="sxs-lookup"><span data-stu-id="90a49-159">Receiving Events From the Player</span></span>

<span data-ttu-id="90a49-160">MFPlay usa un'interfaccia di callback per inviare eventi all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="90a49-160">MFPlay uses a callback interface to send events to your application.</span></span> <span data-ttu-id="90a49-161">Esistono due motivi per questo callback:</span><span class="sxs-lookup"><span data-stu-id="90a49-161">There are two reasons for this callback:</span></span>

-   <span data-ttu-id="90a49-162">La riproduzione avviene in un thread separato.</span><span class="sxs-lookup"><span data-stu-id="90a49-162">Playback occurs on a separate thread.</span></span> <span data-ttu-id="90a49-163">Durante la riproduzione, è possibile che si verifichino determinati eventi, ad esempio il raggiungimento della fine del file.</span><span class="sxs-lookup"><span data-stu-id="90a49-163">During playback, certain events might occur, such as reaching the end of the file.</span></span> <span data-ttu-id="90a49-164">MFPlay usa il callback per notificare all'applicazione l'evento.</span><span class="sxs-lookup"><span data-stu-id="90a49-164">MFPlay uses the callback to notify your application of the event.</span></span>
-   <span data-ttu-id="90a49-165">Molti dei metodi [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) sono asincroni, ovvero restituiscono prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="90a49-165">Many of the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) methods are asynchronous, meaning they return before the operation completes.</span></span> <span data-ttu-id="90a49-166">I metodi asincroni consentono di avviare un'operazione dal thread dell'interfaccia utente che potrebbe richiedere molto tempo per il completamento, senza causare il blocco dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="90a49-166">Asynchronous methods let you start an operation from your UI thread that might take a long time to complete, without it causing your UI to block.</span></span> <span data-ttu-id="90a49-167">Al termine dell'operazione, MFPlay segnala il callback.</span><span class="sxs-lookup"><span data-stu-id="90a49-167">After the operation completes, MFPlay signals the callback.</span></span>

<span data-ttu-id="90a49-168">Per ricevere le notifiche di callback, implementare l'interfaccia [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="90a49-168">To receive callback notifications, implement the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="90a49-169">Questa interfaccia eredita **IUnknown** e definisce un solo metodo, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span><span class="sxs-lookup"><span data-stu-id="90a49-169">This interface inherits **IUnknown** and defines a single method, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span></span> <span data-ttu-id="90a49-170">Per impostare il callback, passare un puntatore all'implementazione di **IMFPMediaPlayerCallback** nel parametro *PCallback* della funzione [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="90a49-170">To set up the callback, pass a pointer to your **IMFPMediaPlayerCallback** implementation in the *pCallback* parameter of the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span>

<span data-ttu-id="90a49-171">Ecco il primo esempio di questa esercitazione, modificato per includere il callback.</span><span class="sxs-lookup"><span data-stu-id="90a49-171">Here is the first example from this tutorial, modified to include the callback.</span></span>


```
// Global variables.
IMFPMediaPlayer *g_pPlayer = NULL;
IMFPMediaPlayerCallback *g_pCallback = NULL;

// Call an application-defined function to create the callback object.
hr = CreateMyCallback(&g_pCallback);

// Create the player object and play a video file.

const WCHAR *sURL = L"C:\\Users\\Public\\Videos\\example.wmv";

if (SUCCEEDED(hr))
{
    hr = MFPCreateMediaPlayer(
        sURL,
        TRUE,        // Start playback automatically?
        0,           // Flags.
        g_pCallback, // Callback pointer.
        hwnd,
        &g_pPlayer
        );
}
```



<span data-ttu-id="90a49-172">Il metodo [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) dispone di un solo parametro, ovvero un puntatore alla struttura [**dell' \_ \_ intestazione dell'evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) .</span><span class="sxs-lookup"><span data-stu-id="90a49-172">The [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method has a single parameter, which is a pointer to the [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="90a49-173">Il membro **eEventType** della struttura indica l'evento che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="90a49-173">The **eEventType** member of this structure tells you which event occurred.</span></span> <span data-ttu-id="90a49-174">Ad esempio, quando viene avviata la riproduzione, MFPlay invia l'evento di **\_ riproduzione del \_ tipo \_ di evento MFP** .</span><span class="sxs-lookup"><span data-stu-id="90a49-174">For example, when playback starts, MFPlay sends the **MFP\_EVENT\_TYPE\_PLAY** event.</span></span>

<span data-ttu-id="90a49-175">Ogni tipo di evento dispone di una struttura di dati corrispondente che contiene informazioni per l'evento.</span><span class="sxs-lookup"><span data-stu-id="90a49-175">Each event type has a corresponding data structure that contains information for that event.</span></span> <span data-ttu-id="90a49-176">Ognuna di queste strutture inizia con una struttura di [**\_ \_ intestazione di evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) .</span><span class="sxs-lookup"><span data-stu-id="90a49-176">Each of these structures starts with an [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="90a49-177">Nel callback eseguire il cast del puntatore dell' **\_ \_ intestazione dell'evento MFP** alla struttura di dati specifica dell'evento.</span><span class="sxs-lookup"><span data-stu-id="90a49-177">In your callback, cast the **MFP\_EVENT\_HEADER** pointer to the event-specific data structure.</span></span> <span data-ttu-id="90a49-178">Ad esempio, se il tipo di evento è l' **\_ \_ evento di riproduzione MFP**, la struttura dei dati è l' [**\_ \_ evento di riproduzione MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event).</span><span class="sxs-lookup"><span data-stu-id="90a49-178">For example, if the event type is **MFP\_PLAY\_EVENT**, the data structure is [**MFP\_PLAY\_EVENT**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event).</span></span> <span data-ttu-id="90a49-179">Nel codice seguente viene illustrato come gestire questo evento nel callback.</span><span class="sxs-lookup"><span data-stu-id="90a49-179">The following code shows how to handle this event in the callback.</span></span>


```
void STDMETHODCALLTYPE MediaPlayerCallback::OnMediaPlayerEvent(
    MFP_EVENT_HEADER *pEventHeader
    )
{
    switch (pEventHeader->eEventType)
    {
    case MFP_EVENT_TYPE_PLAY:
        OnPlay(MFP_GET_PLAY_EVENT(pEventHeader));
        break;

    // Other event types (not shown).

    }
}

// Function to handle the event.
void OnPlay(MFP_PLAY_EVENT *pEvent)
{
    if (FAILED(pEvent->header.hrEvent))
    {  
        // Error occurred during playback.
    }  
}
```



<span data-ttu-id="90a49-180">Questo esempio usa l'evento dell' [**\_ evento di \_ riproduzione \_ MFP Get**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) per eseguire il cast del puntatore *pEventHeader* a una struttura di [**\_ \_ eventi Play di MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) .</span><span class="sxs-lookup"><span data-stu-id="90a49-180">This example uses the [**MFP\_GET\_PLAY\_EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) event to cast the *pEventHeader* pointer to an [**MFP\_PLAY\_EVENT**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) structure.</span></span> <span data-ttu-id="90a49-181">Il valore **HRESULT** dall'operazione che ha generato l'evento viene archiviato nel campo **hrEvent** della struttura.</span><span class="sxs-lookup"><span data-stu-id="90a49-181">The **HRESULT** from the operation that triggered the event is stored in the **hrEvent** field of the structure.</span></span>

<span data-ttu-id="90a49-182">Per un elenco di tutti i tipi di evento e le strutture di dati corrispondenti, vedere [**\_ \_ tipo di evento MFP**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).</span><span class="sxs-lookup"><span data-stu-id="90a49-182">For a list of all the event types and the corresponding data structures, see [**MFP\_EVENT\_TYPE**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).</span></span>

<span data-ttu-id="90a49-183">Nota sul threading: per impostazione predefinita, MFPlay richiama il callback dallo stesso thread che ha chiamato [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer).</span><span class="sxs-lookup"><span data-stu-id="90a49-183">A note about threading: By default, MFPlay invokes the callback from the same thread that called [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer).</span></span> <span data-ttu-id="90a49-184">Questo thread deve avere un ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="90a49-184">This thread must have a message loop.</span></span> <span data-ttu-id="90a49-185">In alternativa, è possibile passare il flag di **\_ \_ \_ \_ callback a thread libero dell'opzione MFP** nel parametro *creationOptions* di **MFPCreateMediaPlayer**.</span><span class="sxs-lookup"><span data-stu-id="90a49-185">Alternatively, you can pass the **MFP\_OPTION\_FREE\_THREADED\_CALLBACK** flag in the *creationOptions* parameter of **MFPCreateMediaPlayer**.</span></span> <span data-ttu-id="90a49-186">Questo flag fa in modo che MFPlay richiami i callback da un thread separato.</span><span class="sxs-lookup"><span data-stu-id="90a49-186">This flag causes MFPlay to invoke callbacks from a separate thread.</span></span> <span data-ttu-id="90a49-187">Entrambe le opzioni hanno implicazioni per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="90a49-187">Either option has implications for your application.</span></span> <span data-ttu-id="90a49-188">L'opzione default indica che il callback non può eseguire operazioni che attendono il ciclo di messaggi, ad esempio l'attesa di un'azione dell'interfaccia utente, perché in questo modo si bloccherà la routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="90a49-188">The default option means your callback cannot do anything that waits on your message loop, such as waiting for a UI action, because that will block your window procedure.</span></span> <span data-ttu-id="90a49-189">L'opzione a thread libero significa che è necessario usare le sezioni critiche per proteggere tutti i dati a cui si accede nel callback.</span><span class="sxs-lookup"><span data-stu-id="90a49-189">The free-threaded option means you need to use critical sections to protect any data that you access in your callback.</span></span> <span data-ttu-id="90a49-190">Nella maggior parte dei casi, l'opzione predefinita è più semplice.</span><span class="sxs-lookup"><span data-stu-id="90a49-190">In most cases, the default option is simplest.</span></span>

## <a name="getting-information-about-a-media-file"></a><span data-ttu-id="90a49-191">Recupero di informazioni su un file multimediale</span><span class="sxs-lookup"><span data-stu-id="90a49-191">Getting Information About a Media File</span></span>

<span data-ttu-id="90a49-192">Quando si apre un file multimediale in MFPlay, il lettore crea un oggetto denominato *elemento multimediale* che rappresenta il file multimediale.</span><span class="sxs-lookup"><span data-stu-id="90a49-192">When you open a media file in MFPlay, the player creates an object called a *media item* that represents the media file.</span></span> <span data-ttu-id="90a49-193">Questo oggetto espone l'interfaccia [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) , che è possibile usare per ottenere informazioni sul file multimediale.</span><span class="sxs-lookup"><span data-stu-id="90a49-193">This object exposes the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface, which you can use to get information about the media file.</span></span> <span data-ttu-id="90a49-194">Molte delle strutture di evento MFPlay contengono un puntatore all'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="90a49-194">Many of the MFPlay event structures contain a pointer to the current media item.</span></span> <span data-ttu-id="90a49-195">È anche possibile ottenere l'elemento multimediale corrente chiamando [**IMFPMediaPlayer:: GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) sul lettore.</span><span class="sxs-lookup"><span data-stu-id="90a49-195">You can also get the current media item by calling [**IMFPMediaPlayer::GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) on the player.</span></span>

<span data-ttu-id="90a49-196">Due metodi particolarmente utili sono [**IMFPMediaItem:: HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) e [**IMFPMediaItem:: HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio).</span><span class="sxs-lookup"><span data-stu-id="90a49-196">Two particularly useful methods are [**IMFPMediaItem::HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) and [**IMFPMediaItem::HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio).</span></span> <span data-ttu-id="90a49-197">Questi metodi eseguono una query se l'origine del supporto contiene video o audio.</span><span class="sxs-lookup"><span data-stu-id="90a49-197">These methods query whether the media source contains video or audio.</span></span>

<span data-ttu-id="90a49-198">Il codice seguente, ad esempio, verifica se il file multimediale corrente contiene un flusso video.</span><span class="sxs-lookup"><span data-stu-id="90a49-198">For example, the following code tests whether the current media file contains a video stream.</span></span>


```
IMFPMediaItem *pItem;
BOOL bHasVideo = FALSE;
BOOL bIsSelected = FALSE;

hr = g_pPlayer->GetMediaItem(TRUE, &pItem);
if (SUCCEEDED(hr))
{
    hr = pItem->HasVideo(&bHasVideo, &bIsSelected);
    pItem->Release();
}
```



<span data-ttu-id="90a49-199">Se il file di origine contiene un flusso video selezionato per la riproduzione, *bHasVideo* e *bIsSelected* sono entrambi impostati su **true**.</span><span class="sxs-lookup"><span data-stu-id="90a49-199">If the source file contains a video stream that is selected for playback, *bHasVideo* and *bIsSelected* are both set to **TRUE**.</span></span>

## <a name="managing-video-playback"></a><span data-ttu-id="90a49-200">Gestione della riproduzione video</span><span class="sxs-lookup"><span data-stu-id="90a49-200">Managing Video Playback</span></span>

<span data-ttu-id="90a49-201">Quando MFPlay riproduce un file video, disegna il video nella finestra specificata nella funzione [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="90a49-201">When MFPlay plays a video file, it draws the video in the window that you specified in the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span> <span data-ttu-id="90a49-202">Questo problema si verifica in un thread separato di proprietà della pipeline di riproduzione Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="90a49-202">This occurs on a separate thread owned by the Microsoft Media Foundation playback pipeline.</span></span> <span data-ttu-id="90a49-203">Nella maggior parte dei casi, non è necessario che l'applicazione gestisca questo processo.</span><span class="sxs-lookup"><span data-stu-id="90a49-203">For the most part, your application does not need to manage this process.</span></span> <span data-ttu-id="90a49-204">Tuttavia, esistono due situazioni in cui l'applicazione deve inviare una notifica a MFPlay per aggiornare il video.</span><span class="sxs-lookup"><span data-stu-id="90a49-204">However, there are two situations where the application must notify MFPlay to update the video.</span></span>

-   <span data-ttu-id="90a49-205">Se la riproduzione viene sospesa o arrestata, MFPlay deve ricevere una notifica ogni volta che la finestra video dell'applicazione riceve un \_ messaggio di disegno WM.</span><span class="sxs-lookup"><span data-stu-id="90a49-205">If playback is paused or stopped, MFPlay must be notified whenever the application's video window receives a WM\_PAINT message.</span></span> <span data-ttu-id="90a49-206">Questo consente a MFPlay di ridisegnare la finestra.</span><span class="sxs-lookup"><span data-stu-id="90a49-206">This allows MFPlay to repaint the window.</span></span>
-   <span data-ttu-id="90a49-207">Se la finestra viene ridimensionata, MFPlay deve ricevere una notifica in modo che possa ridimensionare il video in base alla nuova dimensione della finestra.</span><span class="sxs-lookup"><span data-stu-id="90a49-207">If the window is resized, MFPlay must be notified so that it can scale the video to match the new window size.</span></span>

<span data-ttu-id="90a49-208">Il metodo [**IMFPMediaPlayer:: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) gestisce entrambi i casi.</span><span class="sxs-lookup"><span data-stu-id="90a49-208">The [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) method handles both cases.</span></span> <span data-ttu-id="90a49-209">Chiamare questo metodo all'interno dei \_ \_ gestori di messaggi per la finestra di disegno WM e le dimensioni WM.</span><span class="sxs-lookup"><span data-stu-id="90a49-209">Call this method inside both the WM\_PAINT and WM\_SIZE message handlers for the video window.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="90a49-210">Chiamare la funzione **BEGINPAINT** GDI prima di chiamare [**UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span><span class="sxs-lookup"><span data-stu-id="90a49-210">Call the GDI **BeginPaint** function before calling [**UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span></span>

 


```
IMFPMediaPlayer *g_pPlayer;   // MFPlay player object

void OnSize(HWND hwnd, UINT state, int cx, int cy)
{
    HDC hdc;
    PAINTSTRUCT ps;

    if (g_pPlayer && (state == SIZE_RESTORED))
    {
        hdc = BeginPaint(hwnd, &ps);
        g_pPlayer->UpdateVideo();
         EndPaint(hwnd, &ps);
    }
}

void OnPaint(HWND hwnd)
{
    HDC hdc;
    PAINTSTRUCT ps;

    hdc = BeginPaint(hwnd, &ps);
    if (g_pPlayer)
    {
        g_pPlayer->UpdateVideo();
    }
      EndPaint(hwnd, &ps);
}
```



<span data-ttu-id="90a49-211">Se non diversamente specificato, MFPlay Visualizza il video con le proporzioni corrette, se necessario.</span><span class="sxs-lookup"><span data-stu-id="90a49-211">Unless you specify otherwise, MFPlay shows the video at the correct aspect ratio, using letterboxing if needed.</span></span> <span data-ttu-id="90a49-212">Se non si desidera mantenere le proporzioni, chiamare [**IMFPMediaPlayer:: SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) con il flag **MFVideoARMode \_ None** .</span><span class="sxs-lookup"><span data-stu-id="90a49-212">If you do not want to preserve the aspect ratio, call [**IMFPMediaPlayer::SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) with the **MFVideoARMode\_None** flag.</span></span> <span data-ttu-id="90a49-213">In questo modo, MFPlay estenderà il video per riempire l'intero rettangolo, senza alcuna letterbox.</span><span class="sxs-lookup"><span data-stu-id="90a49-213">This will cause MFPlay to stretch the video to fill the entire rectangle, with no letterboxing.</span></span> <span data-ttu-id="90a49-214">In genere è consigliabile usare l'impostazione predefinita e consentire a MFPlay letterbox il video.</span><span class="sxs-lookup"><span data-stu-id="90a49-214">Typically you should use the default setting and let MFPlay letterbox the video.</span></span> <span data-ttu-id="90a49-215">Il colore letterbox predefinito è nero, ma è possibile modificarlo chiamando [**IMFPMediaPlayer:: SetBorderColor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor).</span><span class="sxs-lookup"><span data-stu-id="90a49-215">The default letterbox color is black, but you can change this by calling [**IMFPMediaPlayer::SetBorderColor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor).</span></span>

## <a name="limitations-of-mfplay"></a><span data-ttu-id="90a49-216">Limitazioni di MFPlay</span><span class="sxs-lookup"><span data-stu-id="90a49-216">Limitations of MFPlay</span></span>

<span data-ttu-id="90a49-217">La versione corrente di MFPlay presenta le limitazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="90a49-217">The current version of MFPlay has the following limitations:</span></span>

-   <span data-ttu-id="90a49-218">MFPlay non supporta il contenuto protetto da DRM.</span><span class="sxs-lookup"><span data-stu-id="90a49-218">MFPlay does not support DRM-protected content.</span></span>
-   <span data-ttu-id="90a49-219">Per impostazione predefinita, MFPlay non supporta i protocolli di streaming di rete.</span><span class="sxs-lookup"><span data-stu-id="90a49-219">By default, MFPlay does not support network streaming protocols.</span></span> <span data-ttu-id="90a49-220">Per ulteriori informazioni, vedere [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span><span class="sxs-lookup"><span data-stu-id="90a49-220">For more information, see [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span></span>
-   <span data-ttu-id="90a49-221">MFPlay non supporta le playlist lato server (SSPLs) o altri tipi di origine che svolgono più di un segmento.</span><span class="sxs-lookup"><span data-stu-id="90a49-221">MFPlay does not support server-side playlists (SSPLs) or other types of source that play more than one segment.</span></span> <span data-ttu-id="90a49-222">In termini tecnici, MFPlay interrompe la riproduzione dopo la prima presentazione e ignora gli eventi [MENewPresentation](menewpresentation.md) dall'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="90a49-222">In technical terms, MFPlay stops playback after the first presentation, and ignores any [MENewPresentation](menewpresentation.md) events from the media source.</span></span>
-   <span data-ttu-id="90a49-223">MFPlay non supporta transizioni senza problemi tra origini multimediali.</span><span class="sxs-lookup"><span data-stu-id="90a49-223">MFPlay does not support seamless transitions between media sources.</span></span>
-   <span data-ttu-id="90a49-224">MFPlay non supporta la combinazione di più flussi video.</span><span class="sxs-lookup"><span data-stu-id="90a49-224">MFPlay does not support mixing multiple video streams.</span></span>
-   <span data-ttu-id="90a49-225">Solo i formati multimediali supportati in modo nativo in Media Foundation sono supportati da MFPlay.</span><span class="sxs-lookup"><span data-stu-id="90a49-225">Only media formats supported natively in Media Foundation are supported by MFPlay.</span></span> <span data-ttu-id="90a49-226">Sono inclusi componenti Media Foundation di terze parti che possono essere installati nel sistema.</span><span class="sxs-lookup"><span data-stu-id="90a49-226">(This includes third-party Media Foundation components that might be installed on the system.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="90a49-227">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="90a49-227">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90a49-228">Uso di MFPlay per la riproduzione audio/video</span><span class="sxs-lookup"><span data-stu-id="90a49-228">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



