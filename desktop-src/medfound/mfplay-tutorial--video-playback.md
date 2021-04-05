---
description: Questa esercitazione presenta un'applicazione completa che riproduce video con MFPlay.
ms.assetid: f72a7c1f-b059-474c-96f2-8fad3b1f7035
title: 'Esercitazione su MFPlay: riproduzione video'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30bbadae22e72799c64a42d09b6eed904b56a60d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755295"
---
# <a name="mfplay-tutorial-video-playback"></a><span data-ttu-id="a6252-103">Esercitazione su MFPlay: riproduzione video</span><span class="sxs-lookup"><span data-stu-id="a6252-103">MFPlay Tutorial: Video Playback</span></span>

<span data-ttu-id="a6252-104">\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="a6252-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a6252-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="a6252-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a6252-106">\]</span><span class="sxs-lookup"><span data-stu-id="a6252-106">\]</span></span>

<span data-ttu-id="a6252-107">Questa esercitazione presenta un'applicazione completa che riproduce video con MFPlay.</span><span class="sxs-lookup"><span data-stu-id="a6252-107">This tutorial presents a complete application that plays video using MFPlay.</span></span> <span data-ttu-id="a6252-108">Si basa sull'esempio SDK [SimplePlay](simpleplay-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="a6252-108">It is based on the [SimplePlay](simpleplay-sample.md) SDK sample.</span></span>

<span data-ttu-id="a6252-109">Questa esercitazione contiene le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6252-109">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="a6252-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6252-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="a6252-111">File di intestazione e di libreria</span><span class="sxs-lookup"><span data-stu-id="a6252-111">Header and Library Files</span></span>](#header-and-library-files)
-   [<span data-ttu-id="a6252-112">Variabili globali</span><span class="sxs-lookup"><span data-stu-id="a6252-112">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="a6252-113">Dichiarare la classe callback</span><span class="sxs-lookup"><span data-stu-id="a6252-113">Declare the Callback Class</span></span>](#declare-the-callback-class)
-   [<span data-ttu-id="a6252-114">Dichiarare la funzione SafeRelease</span><span class="sxs-lookup"><span data-stu-id="a6252-114">Declare the SafeRelease Function</span></span>](#declare-the-saferelease-function)
-   [<span data-ttu-id="a6252-115">Aprire un file multimediale</span><span class="sxs-lookup"><span data-stu-id="a6252-115">Open a Media File</span></span>](#open-a-media-file)
-   [<span data-ttu-id="a6252-116">Gestori di messaggi della finestra</span><span class="sxs-lookup"><span data-stu-id="a6252-116">Window Message Handlers</span></span>](#window-message-handlers)
-   [<span data-ttu-id="a6252-117">Implementare il metodo di callback</span><span class="sxs-lookup"><span data-stu-id="a6252-117">Implement the Callback Method</span></span>](#implement-the-callback-method)
-   [<span data-ttu-id="a6252-118">Implementare WinMain</span><span class="sxs-lookup"><span data-stu-id="a6252-118">Implement WinMain</span></span>](#implement-winmain)
-   [<span data-ttu-id="a6252-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a6252-119">Related topics</span></span>](#related-topics)

<span data-ttu-id="a6252-120">Per una descrizione più dettagliata dell'API MFPlay, vedere [Introduzione con MFPlay](getting-started-with-mfplay.md).</span><span class="sxs-lookup"><span data-stu-id="a6252-120">For a more detailed discussion of the MFPlay API, see [Getting Started with MFPlay](getting-started-with-mfplay.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6252-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6252-121">Requirements</span></span>

<span data-ttu-id="a6252-122">MFPlay richiede Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a6252-122">MFPlay requires Windows 7.</span></span>

## <a name="header-and-library-files"></a><span data-ttu-id="a6252-123">File di intestazione e di libreria</span><span class="sxs-lookup"><span data-stu-id="a6252-123">Header and Library Files</span></span>

<span data-ttu-id="a6252-124">Includere i file di intestazione seguenti nel progetto:</span><span class="sxs-lookup"><span data-stu-id="a6252-124">Include the following header files in your project:</span></span>


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <new>
#include <windows.h>
#include <windowsx.h>
#include <mfplay.h>
#include <mferror.h>
#include <shobjidl.h>   // defines IFileOpenDialog
#include <strsafe.h>
#include <Shlwapi.h>
```



<span data-ttu-id="a6252-125">Collegamento alle librerie di codice seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6252-125">Link to the following code libraries:</span></span>

-   <span data-ttu-id="a6252-126">mfplay. lib</span><span class="sxs-lookup"><span data-stu-id="a6252-126">mfplay.lib</span></span>
-   <span data-ttu-id="a6252-127">shlwapi. lib</span><span class="sxs-lookup"><span data-stu-id="a6252-127">shlwapi.lib</span></span>

## <a name="global-variables"></a><span data-ttu-id="a6252-128">Variabili globali</span><span class="sxs-lookup"><span data-stu-id="a6252-128">Global Variables</span></span>

<span data-ttu-id="a6252-129">Dichiarare le variabili globali seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6252-129">Declare the following global variables:</span></span>


```C++
IMFPMediaPlayer         *g_pPlayer = NULL;      // The MFPlay player object.
MediaPlayerCallback     *g_pPlayerCB = NULL;    // Application callback object.

BOOL                    g_bHasVideo = FALSE;
```



<span data-ttu-id="a6252-130">Queste variabili verranno utilizzate come segue:</span><span class="sxs-lookup"><span data-stu-id="a6252-130">These variables will be used as follows:</span></span>

<dl> <dt>

<span data-ttu-id="a6252-131"><span id="g_hwnd"></span><span id="G_HWND"></span>*\_HWND g*</span><span class="sxs-lookup"><span data-stu-id="a6252-131"><span id="g_hwnd"></span><span id="G_HWND"></span>*g\_hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="a6252-132">Handle per la finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a6252-132">A handle to the application window.</span></span>

</dd> <dt>

<span data-ttu-id="a6252-133"><span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g \_ bVideo*</span><span class="sxs-lookup"><span data-stu-id="a6252-133"><span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g\_bVideo*</span></span>
</dt> <dd>

<span data-ttu-id="a6252-134">Valore booleano che indica se il video viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="a6252-134">A Boolean value that tracks whether video is playing.</span></span>

</dd> <dt>

<span data-ttu-id="a6252-135"><span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g \_ pPlayer*</span><span class="sxs-lookup"><span data-stu-id="a6252-135"><span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g\_pPlayer*</span></span>
</dt> <dd>

<span data-ttu-id="a6252-136">Puntatore all'interfaccia [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="a6252-136">A pointer to the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span> <span data-ttu-id="a6252-137">Questa interfaccia viene utilizzata per controllare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="a6252-137">This interface is used to control playback.</span></span>

</dd> <dt>

<span data-ttu-id="a6252-138"><span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g \_ pCallback*</span><span class="sxs-lookup"><span data-stu-id="a6252-138"><span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g\_pCallback*</span></span>
</dt> <dd>

<span data-ttu-id="a6252-139">Puntatore all'interfaccia [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="a6252-139">A pointer to the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="a6252-140">L'applicazione implementa questa interfaccia di callback per ottenere notifiche dall'oggetto Player.</span><span class="sxs-lookup"><span data-stu-id="a6252-140">The application implements this callback interface to get notifications from the player object.</span></span>

</dd> </dl>

## <a name="declare-the-callback-class"></a><span data-ttu-id="a6252-141">Dichiarare la classe callback</span><span class="sxs-lookup"><span data-stu-id="a6252-141">Declare the Callback Class</span></span>

<span data-ttu-id="a6252-142">Per ottenere le notifiche degli eventi dall'oggetto Player, l'applicazione deve implementare l'interfaccia [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="a6252-142">To get event notifications from the player object, the application must implement the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="a6252-143">Nel codice seguente viene dichiarata una classe che implementa l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="a6252-143">The following code declares a class that implements the interface.</span></span> <span data-ttu-id="a6252-144">L'unica variabile membro è *m \_ cref*, che archivia il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="a6252-144">The only member variable is *m\_cRef*, which stores the reference count.</span></span>

<span data-ttu-id="a6252-145">I metodi **IUnknown** sono implementati inline.</span><span class="sxs-lookup"><span data-stu-id="a6252-145">The **IUnknown** methods are implemented inline.</span></span> <span data-ttu-id="a6252-146">L'implementazione del metodo [**IMFPMediaPlayerCallback:: OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) viene visualizzata in un secondo momento; vedere [implementare il metodo di callback](#implement-the-callback-method).</span><span class="sxs-lookup"><span data-stu-id="a6252-146">The implementation of the [**IMFPMediaPlayerCallback::OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method is shown later; see [Implement the Callback Method](#implement-the-callback-method).</span></span>


```C++
// Implements the callback interface for MFPlay events.

class MediaPlayerCallback : public IMFPMediaPlayerCallback
{
    long m_cRef; // Reference count

public:

    MediaPlayerCallback() : m_cRef(1)
    {
    }

    IFACEMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(MediaPlayerCallback, IMFPMediaPlayerCallback),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    IFACEMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    IFACEMETHODIMP_(ULONG) Release()
    {
        ULONG count = InterlockedDecrement(&m_cRef);
        if (count == 0)
        {
            delete this;
            return 0;
        }
        return count;
    }

    // IMFPMediaPlayerCallback methods
    IFACEMETHODIMP_(void) OnMediaPlayerEvent(MFP_EVENT_HEADER *pEventHeader);
};
```



## <a name="declare-the-saferelease-function"></a><span data-ttu-id="a6252-147">Dichiarare la funzione SafeRelease</span><span class="sxs-lookup"><span data-stu-id="a6252-147">Declare the SafeRelease Function</span></span>

<span data-ttu-id="a6252-148">In questa esercitazione viene usata la funzione [SafeRelease](saferelease.md) per rilasciare i puntatori all'interfaccia:</span><span class="sxs-lookup"><span data-stu-id="a6252-148">Throughout this tutorial, the [SafeRelease](saferelease.md) function is used to release interface pointers:</span></span>


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



## <a name="open-a-media-file"></a><span data-ttu-id="a6252-149">Aprire un file multimediale</span><span class="sxs-lookup"><span data-stu-id="a6252-149">Open a Media File</span></span>

<span data-ttu-id="a6252-150">La `PlayMediaFile` funzione apre un file multimediale, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="a6252-150">The `PlayMediaFile` function opens a media file, as follows:</span></span>

1.  <span data-ttu-id="a6252-151">Se *g \_ PPlayer* è **null**, la funzione chiama [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) per creare una nuova istanza dell'oggetto Media Player.</span><span class="sxs-lookup"><span data-stu-id="a6252-151">If *g\_pPlayer* is **NULL**, the function calls [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) to create a new instance of the media player object.</span></span> <span data-ttu-id="a6252-152">I parametri di input per **MFPCreateMediaPlayer** includono un puntatore all'interfaccia di callback e un handle per la finestra video.</span><span class="sxs-lookup"><span data-stu-id="a6252-152">The input parameters to **MFPCreateMediaPlayer** include a pointer to the callback interface and a handle to the video window.</span></span>
2.  <span data-ttu-id="a6252-153">Per aprire il file multimediale, la funzione chiama [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl), passando l'URL del file.</span><span class="sxs-lookup"><span data-stu-id="a6252-153">To open the media file, the function calls [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl), passing in the URL of the file.</span></span> <span data-ttu-id="a6252-154">Questo metodo viene completato in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="a6252-154">This method completes asynchronously.</span></span> <span data-ttu-id="a6252-155">Al termine, viene chiamato il metodo [**IMFPMediaPlayerCallback:: OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a6252-155">When it completes, the application's [**IMFPMediaPlayerCallback::OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method is called.</span></span>


```C++
HRESULT PlayMediaFile(HWND hwnd, PCWSTR pszURL)
{
    HRESULT hr = S_OK;

    // Create the MFPlayer object.
    if (g_pPlayer == NULL)
    {
        g_pPlayerCB = new (std::nothrow) MediaPlayerCallback();

        if (g_pPlayerCB == NULL)
        {
            return E_OUTOFMEMORY;
        }

        hr = MFPCreateMediaPlayer(
            NULL,
            FALSE,          // Start playback automatically?
            0,              // Flags
            g_pPlayerCB,    // Callback pointer
            hwnd,           // Video window
            &g_pPlayer
            );
    }

    // Create a new media item for this URL.

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromURL(pszURL, FALSE, 0, NULL);
    }

    // The CreateMediaItemFromURL method completes asynchronously.
    // The application will receive an MFP_EVENT_TYPE_MEDIAITEM_CREATED
    // event. See MediaPlayerCallback::OnMediaPlayerEvent().

    return hr;
}
```



<span data-ttu-id="a6252-156">La `OnFileOpen` funzione Visualizza la finestra di dialogo file comune, che consente all'utente di selezionare un file per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="a6252-156">The `OnFileOpen` function displays the common file dialog, which enables the user to select a file for playback.</span></span> <span data-ttu-id="a6252-157">L'interfaccia **IFileOpenDialog** viene utilizzata per visualizzare la finestra di dialogo file comune.</span><span class="sxs-lookup"><span data-stu-id="a6252-157">The **IFileOpenDialog** interface is used to display the common file dialog.</span></span> <span data-ttu-id="a6252-158">Questa interfaccia fa parte delle API della shell di Windows. è stata introdotta in Windows Vista come sostituzione per la funzione **GetOpenFileName** precedente.</span><span class="sxs-lookup"><span data-stu-id="a6252-158">This interface is part of the Windows Shell APIs; it was introduced in Windows Vista as a replacement for the older **GetOpenFileName** function.</span></span> <span data-ttu-id="a6252-159">Dopo che l'utente ha selezionato un file, `OnFileOpen` chiama `PlayMediaFile` per avviare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="a6252-159">After the user selects a file, `OnFileOpen` calls `PlayMediaFile` to start playback.</span></span>


```C++
void OnFileOpen(HWND hwnd)
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;
    PWSTR pwszFilePath = NULL;

    // Create the FileOpenDialog object.
    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL,
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->SetTitle(L"Select a File to Play");
    }

    // Show the file-open dialog.
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(hwnd);
    }

    if (hr == HRESULT_FROM_WIN32(ERROR_CANCELLED))
    {
        // User canceled.
        SafeRelease(&pFileOpen);
        return;
    }

    // Get the file name from the dialog.
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pItem->GetDisplayName(SIGDN_URL, &pwszFilePath);
    }

    // Open the media file.
    if (SUCCEEDED(hr))
    {
        hr = PlayMediaFile(hwnd, pwszFilePath);
    }

    if (FAILED(hr))
    {
        ShowErrorMessage(L"Could not open file.", hr);
    }

    CoTaskMemFree(pwszFilePath);

    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
}
```



## <a name="window-message-handlers"></a><span data-ttu-id="a6252-160">Gestori di messaggi della finestra</span><span class="sxs-lookup"><span data-stu-id="a6252-160">Window Message Handlers</span></span>

<span data-ttu-id="a6252-161">Dichiarare quindi i gestori dei messaggi per i messaggi della finestra seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6252-161">Next, declare message handlers for the following window messages:</span></span>

-   <span data-ttu-id="a6252-162">**\_disegno WM**</span><span class="sxs-lookup"><span data-stu-id="a6252-162">**WM\_PAINT**</span></span>
-   <span data-ttu-id="a6252-163">**\_dimensioni WM**</span><span class="sxs-lookup"><span data-stu-id="a6252-163">**WM\_SIZE**</span></span>
-   <span data-ttu-id="a6252-164">**\_chiusura WM**</span><span class="sxs-lookup"><span data-stu-id="a6252-164">**WM\_CLOSE**</span></span>

<span data-ttu-id="a6252-165">Per il messaggio di **\_ disegno WM** , è necessario verificare se il video è attualmente in riproduzione.</span><span class="sxs-lookup"><span data-stu-id="a6252-165">For the **WM\_PAINT** message, you must track whether video is currently playing.</span></span> <span data-ttu-id="a6252-166">In tal caso, chiamare il metodo [**IMFPMediaPlayer:: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) .</span><span class="sxs-lookup"><span data-stu-id="a6252-166">If so, call the [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) method.</span></span> <span data-ttu-id="a6252-167">Questo metodo fa in modo che l'oggetto Player ridisegni il frame video più recente.</span><span class="sxs-lookup"><span data-stu-id="a6252-167">This method causes the player object to redraw the most recent video frame.</span></span>

<span data-ttu-id="a6252-168">Se non è presente alcun video, l'applicazione è responsabile per disegnare la finestra.</span><span class="sxs-lookup"><span data-stu-id="a6252-168">If there is no video, the application is responsible for painting the window.</span></span> <span data-ttu-id="a6252-169">Per questa esercitazione, l'applicazione chiama semplicemente la funzione GDI **fillRect** per riempire l'intera area client.</span><span class="sxs-lookup"><span data-stu-id="a6252-169">For this tutorial, the application simply calls the GDI **FillRect** function to fill the entire client area.</span></span>


```C++
void OnPaint(HWND hwnd)
{
    PAINTSTRUCT ps;
    HDC hdc = BeginPaint(hwnd, &ps);

    if (g_pPlayer && g_bHasVideo)
    {
        // Playback has started and there is video.

        // Do not draw the window background, because the video
        // frame fills the entire client area.

        g_pPlayer->UpdateVideo();
    }
    else
    {
        // There is no video stream, or playback has not started.
        // Paint the entire client area.

        FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
    }

    EndPaint(hwnd, &ps);
}
```



<span data-ttu-id="a6252-170">Per il messaggio di **\_ dimensioni WM** , chiamare [**IMFPMediaPlayer:: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span><span class="sxs-lookup"><span data-stu-id="a6252-170">For the **WM\_SIZE** message, call [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span></span> <span data-ttu-id="a6252-171">Questo metodo fa in modo che l'oggetto Player riregoli il video in modo che corrisponda alla dimensione corrente della finestra.</span><span class="sxs-lookup"><span data-stu-id="a6252-171">This method causes the player object to readjust the video to match the current size of the window.</span></span> <span data-ttu-id="a6252-172">Si noti che **UpdateVideo** viene usato sia per il **\_ disegno WM** che per la **\_ dimensione WM**.</span><span class="sxs-lookup"><span data-stu-id="a6252-172">Note that **UpdateVideo** is used for both **WM\_PAINT** and **WM\_SIZE**.</span></span>


```C++
void OnSize(HWND /*hwnd*/, UINT state, int /*cx*/, int /*cy*/)
{
    if (state == SIZE_RESTORED)
    {
        if (g_pPlayer)
        {
            // Resize the video.
            g_pPlayer->UpdateVideo();
        }
    }
}
```



<span data-ttu-id="a6252-173">Per il messaggio **WM \_ Close** rilasciare i puntatori [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) e [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="a6252-173">For the **WM\_CLOSE** message, release the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) and [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) pointers.</span></span>


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



## <a name="implement-the-callback-method"></a><span data-ttu-id="a6252-174">Implementare il metodo di callback</span><span class="sxs-lookup"><span data-stu-id="a6252-174">Implement the Callback Method</span></span>

<span data-ttu-id="a6252-175">L'interfaccia [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) definisce un solo metodo, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span><span class="sxs-lookup"><span data-stu-id="a6252-175">The [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface defines a single method, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span></span> <span data-ttu-id="a6252-176">Questo metodo invia una notifica all'applicazione quando si verifica un evento durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="a6252-176">This method notifies the application whenever an event occurs during playback.</span></span> <span data-ttu-id="a6252-177">Il metodo accetta un parametro, un puntatore a una struttura dell' [**\_ \_ intestazione dell'evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) .</span><span class="sxs-lookup"><span data-stu-id="a6252-177">The method takes one parameter, a pointer to an [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="a6252-178">Il membro **eEventType** della struttura specifica l'evento che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="a6252-178">The **eEventType** member of the structure specifies the event that occurred.</span></span>

<span data-ttu-id="a6252-179">La struttura dell' [**\_ \_ intestazione dell'evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) può essere seguita da dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="a6252-179">The [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure may be followed by additional data.</span></span> <span data-ttu-id="a6252-180">Per ogni tipo di evento, viene definita una macro che esegue il cast del puntatore dell' **\_ \_ intestazione dell'evento MFP** a una struttura specifica dell'evento.</span><span class="sxs-lookup"><span data-stu-id="a6252-180">For each event type, a macro is defined that casts the **MFP\_EVENT\_HEADER** pointer to an event-specific structure.</span></span> <span data-ttu-id="a6252-181">(Vedere [**\_ \_ tipo di evento MFP**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type)).</span><span class="sxs-lookup"><span data-stu-id="a6252-181">(See [**MFP\_EVENT\_TYPE**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).)</span></span>

<span data-ttu-id="a6252-182">Per questa esercitazione, due eventi sono significativi:</span><span class="sxs-lookup"><span data-stu-id="a6252-182">For this tutorial, two events are significant:</span></span>



| <span data-ttu-id="a6252-183">Event</span><span class="sxs-lookup"><span data-stu-id="a6252-183">Event</span></span>                                    | <span data-ttu-id="a6252-184">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6252-184">Description</span></span>                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6252-185">**\_tipo di evento MFP \_ \_ MEDIAITEM \_ creato**</span><span class="sxs-lookup"><span data-stu-id="a6252-185">**MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED**</span></span> | <span data-ttu-id="a6252-186">Inviato al completamento del [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) .</span><span class="sxs-lookup"><span data-stu-id="a6252-186">Sent when the [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) completes.</span></span> |
| <span data-ttu-id="a6252-187">**\_tipo di evento MFP \_ \_ MEDIAITEM \_ set**</span><span class="sxs-lookup"><span data-stu-id="a6252-187">**MFP\_EVENT\_TYPE\_MEDIAITEM\_SET**</span></span>     | <span data-ttu-id="a6252-188">Inviato quando [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) viene completato.</span><span class="sxs-lookup"><span data-stu-id="a6252-188">Sent when [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) completes.</span></span>                         |



 

<span data-ttu-id="a6252-189">Nel codice seguente viene illustrato come eseguire il cast del puntatore dell' [**\_ \_ intestazione dell'evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) alla struttura specifica dell'evento.</span><span class="sxs-lookup"><span data-stu-id="a6252-189">The following code shows how to cast the [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) pointer to the event-specific structure.</span></span>


```C++
void MediaPlayerCallback::OnMediaPlayerEvent(MFP_EVENT_HEADER * pEventHeader)
{
    if (FAILED(pEventHeader->hrEvent))
    {
        ShowErrorMessage(L"Playback error", pEventHeader->hrEvent);
        return;
    }

    switch (pEventHeader->eEventType)
    {
    case MFP_EVENT_TYPE_MEDIAITEM_CREATED:
        OnMediaItemCreated(MFP_GET_MEDIAITEM_CREATED_EVENT(pEventHeader));
        break;

    case MFP_EVENT_TYPE_MEDIAITEM_SET:
        OnMediaItemSet(MFP_GET_MEDIAITEM_SET_EVENT(pEventHeader));
        break;
    }
}
```



<span data-ttu-id="a6252-190">Il **\_ tipo di evento MFP MEDIAITEM evento \_ \_ \_ creato** notifica all'applicazione che il metodo [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) è stato completato.</span><span class="sxs-lookup"><span data-stu-id="a6252-190">The **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event notifies the application that the [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method has completed.</span></span> <span data-ttu-id="a6252-191">La struttura dell'evento contiene un puntatore all'interfaccia [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) , che rappresenta l'elemento multimediale creato dall'URL.</span><span class="sxs-lookup"><span data-stu-id="a6252-191">The event structure contains a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface, which represents the media item created from the URL.</span></span> <span data-ttu-id="a6252-192">Per accodare l'elemento per la riproduzione, passare questo puntatore al metodo [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) :</span><span class="sxs-lookup"><span data-stu-id="a6252-192">To queue the item for playback, pass this pointer to the [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) method:</span></span>


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    // The media item was created successfully.

    if (g_pPlayer)
    {
        BOOL    bHasVideo = FALSE;
        BOOL    bIsSelected = FALSE;

        // Check if the media item contains video.
        HRESULT hr = pEvent->pMediaItem->HasVideo(&bHasVideo, &bIsSelected);
        if (SUCCEEDED(hr))
        {
            g_bHasVideo = bHasVideo && bIsSelected;

            // Set the media item on the player. This method completes
            // asynchronously.
            hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
        }

        if (FAILED(hr))
        {
            ShowErrorMessage(L"Error playing this file.", hr);
        }
   }
}
```



<span data-ttu-id="a6252-193">Il **\_ tipo di evento MFP \_ \_ MEDIAITEM \_ set** Event informa l'applicazione che [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a6252-193">The **MFP\_EVENT\_TYPE\_MEDIAITEM\_SET** event notifies the application that [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) has completed.</span></span> <span data-ttu-id="a6252-194">Chiamare [**IMFPMediaPlayer::P Lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) per avviare la riproduzione:</span><span class="sxs-lookup"><span data-stu-id="a6252-194">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to start playback:</span></span>


```C++
void OnMediaItemSet(MFP_MEDIAITEM_SET_EVENT * /*pEvent*/)
{
    HRESULT hr = g_pPlayer->Play();
    if (FAILED(hr))
    {
        ShowErrorMessage(L"IMFPMediaPlayer::Play failed.", hr);
    }
}
```



## <a name="implement-winmain"></a><span data-ttu-id="a6252-195">Implementare WinMain</span><span class="sxs-lookup"><span data-stu-id="a6252-195">Implement WinMain</span></span>

<span data-ttu-id="a6252-196">Nella parte restante di questa esercitazione non sono presenti chiamate alle API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a6252-196">In the remainder of this tutorial, there are no calls to Media Foundation APIs.</span></span> <span data-ttu-id="a6252-197">Il codice seguente illustra la procedura della finestra:</span><span class="sxs-lookup"><span data-stu-id="a6252-197">The following code shows the window procedure:</span></span>


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        HANDLE_MSG(hwnd, WM_CLOSE,   OnClose);
        HANDLE_MSG(hwnd, WM_PAINT,   OnPaint);
        HANDLE_MSG(hwnd, WM_COMMAND, OnCommand);
        HANDLE_MSG(hwnd, WM_SIZE,    OnSize);

    case WM_ERASEBKGND:
        return 1;

    default:
        return DefWindowProc(hwnd, uMsg, wParam, lParam);
    }
}
```



<span data-ttu-id="a6252-198">La `InitializeWindow` funzione registra la classe della finestra dell'applicazione e crea la finestra.</span><span class="sxs-lookup"><span data-stu-id="a6252-198">The `InitializeWindow` function registers the application's window class and creates the window.</span></span>


```C++
BOOL InitializeWindow(HWND *pHwnd)
{
    const wchar_t CLASS_NAME[]  = L"MFPlay Window Class";
    const wchar_t WINDOW_NAME[] = L"MFPlay Sample Application";

    WNDCLASS wc = {};

    wc.lpfnWndProc   = WindowProc;
    wc.hInstance     = GetModuleHandle(NULL);
    wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
    wc.lpszClassName = CLASS_NAME;
    wc.lpszMenuName  = MAKEINTRESOURCE(IDR_MENU1);

    RegisterClass(&wc);

    HWND hwnd = CreateWindow(
        CLASS_NAME, WINDOW_NAME, WS_OVERLAPPEDWINDOW,
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,
        NULL, NULL, GetModuleHandle(NULL), NULL);

    if (!hwnd)
    {
        return FALSE;
    }

    ShowWindow(hwnd, SW_SHOWDEFAULT);
    UpdateWindow(hwnd);

    *pHwnd = hwnd;

    return TRUE;
}
```



<span data-ttu-id="a6252-199">Infine, implementare il punto di ingresso dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="a6252-199">Finally, implement the application entry point:</span></span>


```C++
int WINAPI wWinMain(HINSTANCE, HINSTANCE, PWSTR, int)
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    HRESULT hr = CoInitializeEx(NULL,
        COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    if (FAILED(hr))
    {
        return 0;
    }

    HWND hwnd = NULL;
    if (InitializeWindow(&hwnd))
    {
        // Message loop
        MSG msg = {};
        while (GetMessage(&msg, NULL, 0, 0))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }

        DestroyWindow(hwnd);
    }
    CoUninitialize();

    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="a6252-200">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a6252-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6252-201">Uso di MFPlay per la riproduzione audio/video</span><span class="sxs-lookup"><span data-stu-id="a6252-201">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



