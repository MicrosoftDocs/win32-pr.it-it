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
# <a name="mfplay-tutorial-video-playback"></a>Esercitazione su MFPlay: riproduzione video

\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. \]

Questa esercitazione presenta un'applicazione completa che riproduce video con MFPlay. Si basa sull'esempio SDK [SimplePlay](simpleplay-sample.md) .

Questa esercitazione contiene le sezioni seguenti:

-   [Requisiti](#requirements)
-   [File di intestazione e di libreria](#header-and-library-files)
-   [Variabili globali](#global-variables)
-   [Dichiarare la classe callback](#declare-the-callback-class)
-   [Dichiarare la funzione SafeRelease](#declare-the-saferelease-function)
-   [Aprire un file multimediale](#open-a-media-file)
-   [Gestori di messaggi della finestra](#window-message-handlers)
-   [Implementare il metodo di callback](#implement-the-callback-method)
-   [Implementare WinMain](#implement-winmain)
-   [Argomenti correlati](#related-topics)

Per una descrizione più dettagliata dell'API MFPlay, vedere [Introduzione con MFPlay](getting-started-with-mfplay.md).

## <a name="requirements"></a>Requisiti

MFPlay richiede Windows 7.

## <a name="header-and-library-files"></a>File di intestazione e di libreria

Includere i file di intestazione seguenti nel progetto:


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



Collegamento alle librerie di codice seguenti:

-   mfplay. lib
-   shlwapi. lib

## <a name="global-variables"></a>Variabili globali

Dichiarare le variabili globali seguenti:


```C++
IMFPMediaPlayer         *g_pPlayer = NULL;      // The MFPlay player object.
MediaPlayerCallback     *g_pPlayerCB = NULL;    // Application callback object.

BOOL                    g_bHasVideo = FALSE;
```



Queste variabili verranno utilizzate come segue:

<dl> <dt>

<span id="g_hwnd"></span><span id="G_HWND"></span>*\_HWND g*
</dt> <dd>

Handle per la finestra dell'applicazione.

</dd> <dt>

<span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g \_ bVideo*
</dt> <dd>

Valore booleano che indica se il video viene riprodotto.

</dd> <dt>

<span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g \_ pPlayer*
</dt> <dd>

Puntatore all'interfaccia [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) . Questa interfaccia viene utilizzata per controllare la riproduzione.

</dd> <dt>

<span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g \_ pCallback*
</dt> <dd>

Puntatore all'interfaccia [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) . L'applicazione implementa questa interfaccia di callback per ottenere notifiche dall'oggetto Player.

</dd> </dl>

## <a name="declare-the-callback-class"></a>Dichiarare la classe callback

Per ottenere le notifiche degli eventi dall'oggetto Player, l'applicazione deve implementare l'interfaccia [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) . Nel codice seguente viene dichiarata una classe che implementa l'interfaccia. L'unica variabile membro è *m \_ cref*, che archivia il conteggio dei riferimenti.

I metodi **IUnknown** sono implementati inline. L'implementazione del metodo [**IMFPMediaPlayerCallback:: OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) viene visualizzata in un secondo momento; vedere [implementare il metodo di callback](#implement-the-callback-method).


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



## <a name="declare-the-saferelease-function"></a>Dichiarare la funzione SafeRelease

In questa esercitazione viene usata la funzione [SafeRelease](saferelease.md) per rilasciare i puntatori all'interfaccia:


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



## <a name="open-a-media-file"></a>Aprire un file multimediale

La `PlayMediaFile` funzione apre un file multimediale, come indicato di seguito:

1.  Se *g \_ PPlayer* è **null**, la funzione chiama [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) per creare una nuova istanza dell'oggetto Media Player. I parametri di input per **MFPCreateMediaPlayer** includono un puntatore all'interfaccia di callback e un handle per la finestra video.
2.  Per aprire il file multimediale, la funzione chiama [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl), passando l'URL del file. Questo metodo viene completato in modo asincrono. Al termine, viene chiamato il metodo [**IMFPMediaPlayerCallback:: OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) dell'applicazione.


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



La `OnFileOpen` funzione Visualizza la finestra di dialogo file comune, che consente all'utente di selezionare un file per la riproduzione. L'interfaccia **IFileOpenDialog** viene utilizzata per visualizzare la finestra di dialogo file comune. Questa interfaccia fa parte delle API della shell di Windows. è stata introdotta in Windows Vista come sostituzione per la funzione **GetOpenFileName** precedente. Dopo che l'utente ha selezionato un file, `OnFileOpen` chiama `PlayMediaFile` per avviare la riproduzione.


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



## <a name="window-message-handlers"></a>Gestori di messaggi della finestra

Dichiarare quindi i gestori dei messaggi per i messaggi della finestra seguenti:

-   **\_disegno WM**
-   **\_dimensioni WM**
-   **\_chiusura WM**

Per il messaggio di **\_ disegno WM** , è necessario verificare se il video è attualmente in riproduzione. In tal caso, chiamare il metodo [**IMFPMediaPlayer:: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) . Questo metodo fa in modo che l'oggetto Player ridisegni il frame video più recente.

Se non è presente alcun video, l'applicazione è responsabile per disegnare la finestra. Per questa esercitazione, l'applicazione chiama semplicemente la funzione GDI **fillRect** per riempire l'intera area client.


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



Per il messaggio di **\_ dimensioni WM** , chiamare [**IMFPMediaPlayer:: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo). Questo metodo fa in modo che l'oggetto Player riregoli il video in modo che corrisponda alla dimensione corrente della finestra. Si noti che **UpdateVideo** viene usato sia per il **\_ disegno WM** che per la **\_ dimensione WM**.


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



Per il messaggio **WM \_ Close** rilasciare i puntatori [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) e [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



## <a name="implement-the-callback-method"></a>Implementare il metodo di callback

L'interfaccia [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) definisce un solo metodo, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent). Questo metodo invia una notifica all'applicazione quando si verifica un evento durante la riproduzione. Il metodo accetta un parametro, un puntatore a una struttura dell' [**\_ \_ intestazione dell'evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) . Il membro **eEventType** della struttura specifica l'evento che si è verificato.

La struttura dell' [**\_ \_ intestazione dell'evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) può essere seguita da dati aggiuntivi. Per ogni tipo di evento, viene definita una macro che esegue il cast del puntatore dell' **\_ \_ intestazione dell'evento MFP** a una struttura specifica dell'evento. (Vedere [**\_ \_ tipo di evento MFP**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type)).

Per questa esercitazione, due eventi sono significativi:



| Event                                    | Descrizione                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------|
| **\_tipo di evento MFP \_ \_ MEDIAITEM \_ creato** | Inviato al completamento del [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) . |
| **\_tipo di evento MFP \_ \_ MEDIAITEM \_ set**     | Inviato quando [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) viene completato.                         |



 

Nel codice seguente viene illustrato come eseguire il cast del puntatore dell' [**\_ \_ intestazione dell'evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) alla struttura specifica dell'evento.


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



Il **\_ tipo di evento MFP MEDIAITEM evento \_ \_ \_ creato** notifica all'applicazione che il metodo [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) è stato completato. La struttura dell'evento contiene un puntatore all'interfaccia [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) , che rappresenta l'elemento multimediale creato dall'URL. Per accodare l'elemento per la riproduzione, passare questo puntatore al metodo [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) :


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



Il **\_ tipo di evento MFP \_ \_ MEDIAITEM \_ set** Event informa l'applicazione che [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) è stata completata. Chiamare [**IMFPMediaPlayer::P Lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) per avviare la riproduzione:


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



## <a name="implement-winmain"></a>Implementare WinMain

Nella parte restante di questa esercitazione non sono presenti chiamate alle API Media Foundation. Il codice seguente illustra la procedura della finestra:


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



La `InitializeWindow` funzione registra la classe della finestra dell'applicazione e crea la finestra.


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



Infine, implementare il punto di ingresso dell'applicazione:


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di MFPlay per la riproduzione audio/video](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



