---
description: MFPlay è un'API per la creazione di applicazioni di riproduzione multimediale in C++.
ms.assetid: 55612f49-5995-4bdf-aa12-8a853e5a2b24
title: Attività iniziali con MFPlay
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2afb0b20189501530116c252a4d11a9b3e2d8d0dff07482b1998b73400071e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118063495"
---
# <a name="getting-started-with-mfplay"></a>Attività iniziali con MFPlay

\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. \]

MFPlay è un'API per la creazione di applicazioni di riproduzione multimediale in C++.

In questo argomento sono incluse le sezioni seguenti:

-   [Requisiti](#requirements)
-   [Informazioni su MFPlay](#about-mfplay)
-   [Riproduzione di un file multimediale](#playing-a-media-file)
-   [Controllo della riproduzione](#controlling-playback)
-   [Ricezione di eventi dal lettore](#receiving-events-from-the-player)
-   [Recupero di informazioni su un file multimediale](#getting-information-about-a-media-file)
-   [Gestione della riproduzione video](#managing-video-playback)
-   [Limitazioni di MFPlay](#limitations-of-mfplay)
-   [Argomenti correlati](#related-topics)

## <a name="requirements"></a>Requisiti

MFPlay richiede Windows 7.

## <a name="about-mfplay"></a>Informazioni su MFPlay

MFPlay ha un modello di programmazione semplice, fornendo al tempo stesso il set principale di funzionalità necessarie per la maggior parte delle applicazioni di riproduzione. Un'applicazione crea un oggetto *lettore* che controlla la riproduzione. Per riprodurre un file multimediale, l'oggetto lettore crea un elemento *multimediale* che può essere usato per ottenere informazioni sul contenuto del file multimediale. L'applicazione controlla la riproduzione tramite metodi [**sull'interfaccia IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) dell'oggetto lettore. Facoltativamente, l'applicazione può ottenere notifiche degli eventi tramite un'interfaccia di callback Il diagramma seguente illustra questo processo.

![Diagramma concettuale: l'applicazione e il lettore puntano l'uno all'altro, entrambi puntano all'elemento multimediale, che punta al file multimediale](images/mfplay.png)

## <a name="playing-a-media-file"></a>Riproduzione di un file multimediale

Per riprodurre un file multimediale, chiamare la [**funzione MFPCreateMediaPlayer.**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer)


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



La [**funzione MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) crea una nuova istanza dell'oggetto lettore MFPlay. La funzione accetta i parametri seguenti:

-   Il primo parametro è l'URL del file da aprire. Può trattarsi di un file locale o di un file in un server multimediale.
-   Il secondo parametro specifica se la riproduzione viene avviata automaticamente. Impostando questo paremetro su **TRUE,** il file verrà riprodotto non appena viene caricato da MFPlay.
-   Il terzo parametro imposta varie opzioni. Per le opzioni predefinite, passare zero (0).
-   Il quarto parametro è un puntatore a un'interfaccia di callback facoltativa. Questo parametro può essere **NULL,** come illustrato. Il callback è descritto nella sezione [Ricezione di eventi dal lettore](#receiving-events-from-the-player).
-   Il quinto parametro è un handle per la finestra dell'applicazione. Se il file multimediale contiene un flusso video, il video verrà visualizzato all'interno dell'area client di questa finestra. Per la riproduzione solo audio, questo parametro può essere **NULL.**

L'ultimo parametro riceve un puntatore [**all'interfaccia IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) dell'oggetto lettore.

Prima che l'applicazione venga arrestata, assicurarsi di rilasciare il [**puntatore IMFPMediaPlayer.**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) È possibile eseguire questa operazione nel gestore **messaggi WM \_ CLOSE.**


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



> [!Note]  
> In questo esempio viene utilizzata [la funzione SafeRelease](saferelease.md) per rilasciare puntatori a interfaccia.

 

Per una riproduzione video semplice, è tutto il codice necessario. Il resto di questa esercitazione illustra come aggiungere altre funzionalità, a partire da come controllare la riproduzione.

## <a name="controlling-playback"></a>Controllo della riproduzione

Il codice illustrato nella sezione precedente riprodurrà il file multimediale fino a raggiungere la fine del file. È possibile arrestare e avviare la riproduzione chiamando i metodi seguenti [**nell'interfaccia IMFPMediaPlayer:**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)

-   [**IMFPMediaPlayer::P ause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) sospende la riproduzione. Mentre la riproduzione è sospesa, viene visualizzato il fotogramma video più recente e l'audio è invisibile all'utente.
-   [**IMFPMediaPlayer::Stop arresta**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) la riproduzione. Non viene visualizzato alcun video e la posizione di riproduzione viene reimpostata all'inizio del file.
-   [**IMFPMediaPlayer::P lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) riprende la riproduzione dopo l'arresto o la sospensione.

Il codice seguente sospende o riprende la riproduzione quando si preme LA **BARRA SPAZIATRICE.**


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



Questo esempio chiama il metodo [**IMFPMediaPlayer::GetState**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) per ottenere lo stato di riproduzione corrente (sospeso, arrestato o in riproduzione) e sospende o riprende di conseguenza.

## <a name="receiving-events-from-the-player"></a>Ricezione di eventi dal lettore

MFPlay usa un'interfaccia di callback per inviare eventi all'applicazione. Esistono due motivi per questo callback:

-   La riproduzione avviene in un thread separato. Durante la riproduzione, potrebbero verificarsi determinati eventi, ad esempio il raggiungimento della fine del file. MFPlay usa il callback per inviare una notifica all'applicazione dell'evento.
-   Molti dei metodi [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) sono asincroni, ovvero restituiscono prima del completamento dell'operazione. I metodi asincroni consentono di avviare un'operazione dal thread dell'interfaccia utente che potrebbe richiedere molto tempo, senza causare il blocco dell'interfaccia utente. Al termine dell'operazione, MFPlay segnala il callback.

Per ricevere notifiche di callback, implementare [**l'interfaccia IMFPMediaPlayerCallback.**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) Questa interfaccia eredita **IUnknown** e definisce un singolo metodo, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent). Per configurare il callback, passare un puntatore all'implementazione **di IMFPMediaPlayerCallback** nel *parametro pCallback* della [**funzione MFPCreateMediaPlayer.**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer)

Ecco il primo esempio di questa esercitazione, modificato per includere il callback.


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



Il [**metodo OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) ha un singolo parametro, ovvero un puntatore alla struttura [**EVENT \_ \_ HEADER MFP.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Il **membro eEventType** di questa struttura indica quale evento si è verificato. Ad esempio, all'avvio della riproduzione, MFPlay invia **l'evento MFP \_ EVENT TYPE \_ \_ PLAY.**

Ogni tipo di evento ha una struttura di dati corrispondente che contiene informazioni per tale evento. Ognuna di queste strutture inizia con una struttura [**EVENT \_ \_ HEADER MFP.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Nel callback eseguire il cast del puntatore **\_ EVENT \_ HEADER MFP** alla struttura di dati specifica dell'evento. Ad esempio, se il tipo di evento è **MFP \_ PLAY \_ EVENT**, la struttura dei dati è [**MFP \_ PLAY \_ EVENT**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event). Il codice seguente illustra come gestire questo evento nel callback.


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



Questo esempio usa [**l'evento \_ MFP GET PLAY \_ \_ EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) per eseguire il cast del puntatore *pEventHeader* a una struttura [**MFP \_ PLAY \_ EVENT.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) Il **valore HRESULT** dell'operazione che ha attivato l'evento viene archiviato nel **campo hrEvent** della struttura .

Per un elenco di tutti i tipi di evento e delle strutture di dati corrispondenti, vedere [**MFP \_ EVENT \_ TYPE**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).

Nota sul threading: per impostazione predefinita, MFPlay richiama il callback dallo stesso thread che ha chiamato [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer). Questo thread deve avere un ciclo di messaggi. In alternativa, è possibile passare il flag **MFP \_ OPTION \_ FREE \_ THREADED \_ CALLBACK** nel parametro *creationOptions* di **MFPCreateMediaPlayer**. Questo flag fa in modo che MFPlay richiama i callback da un thread separato. Entrambe le opzioni hanno implicazioni per l'applicazione. L'opzione predefinita indica che il callback non può eseguire alcuna operazione che attende il ciclo di messaggi, ad esempio l'attesa di un'azione dell'interfaccia utente, perché ciò bloccherà la routine della finestra. L'opzione a thread libero indica che è necessario usare sezioni critiche per proteggere tutti i dati a cui si accede nel callback. Nella maggior parte dei casi, l'opzione predefinita è la più semplice.

## <a name="getting-information-about-a-media-file"></a>Recupero di informazioni su un file multimediale

Quando si apre un file multimediale in MFPlay, il lettore crea un oggetto denominato *elemento multimediale* che rappresenta il file multimediale. Questo oggetto espone [**l'interfaccia IMFPMediaItem,**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) che è possibile usare per ottenere informazioni sul file multimediale. Molte delle strutture di eventi MFPlay contengono un puntatore all'elemento multimediale corrente. È anche possibile ottenere l'elemento multimediale corrente chiamando [**IMFPMediaPlayer::GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) nel lettore.

Due metodi particolarmente utili sono [**IMFPMediaItem::HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) e [**IMFPMediaItem::HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio). Questi metodi esere query se l'origine multimediale contiene video o audio.

Ad esempio, il codice seguente verifica se il file multimediale corrente contiene un flusso video.


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



Se il file di origine contiene un flusso video selezionato per la riproduzione, *bHasVideo* e *bIsSelected* sono entrambi impostati su **TRUE.**

## <a name="managing-video-playback"></a>Gestione della riproduzione video

Quando MFPlay riproduce un file video, disegna il video nella finestra specificata nella [**funzione MFPCreateMediaPlayer.**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) Ciò si verifica in un thread separato di proprietà della pipeline Microsoft Media Foundation di riproduzione. Nella maggior parte dei casi, l'applicazione non deve gestire questo processo. Esistono tuttavia due situazioni in cui l'applicazione deve inviare una notifica a MFPlay per aggiornare il video.

-   Se la riproduzione viene sospesa o arrestata, MFPlay deve ricevere una notifica ogni volta che la finestra video dell'applicazione riceve un messaggio WM \_ PAINT. Ciò consente a MFPlay di ridisegnare la finestra.
-   Se la finestra viene ridimensionata, MFPlay deve ricevere una notifica in modo che possa ridimensionare il video in modo che corrisponda alle nuove dimensioni della finestra.

Il [**metodo IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) gestisce entrambi i casi. Chiamare questo metodo all'interno dei gestori di messaggi WM PAINT e \_ WM SIZE per la finestra \_ video.

> [!IMPORTANT]
> Chiamare la funzione **BeginPaint** di GDI prima [**di chiamare UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).

 


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



A meno che non si specifica diversamente, MFPlay mostra il video con le proporzioni corrette, usando il letterboxing, se necessario. Se non si vogliono mantenere le proporzioni, chiamare [**IMFPMediaPlayer::SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) con il flag **MFVideoARMode \_ None.** In questo modo MFPlay estenderà il video per riempire l'intero rettangolo, senza letterboxing. In genere è consigliabile usare l'impostazione predefinita e consentire a MFPlay di certificare il video. Il colore predefinito della casella di testo è nero, ma è possibile modificarlo chiamando [**IMFPMediaPlayer::SetBorderColor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor).

## <a name="limitations-of-mfplay"></a>Limitazioni di MFPlay

La versione corrente di MFPlay presenta le limitazioni seguenti:

-   MFPlay non supporta contenuto protetto da DRM.
-   Per impostazione predefinita, MFPlay non supporta i protocolli di streaming di rete. Per altre informazioni, vedere [**IMFPMediaPlayer::CreateMediaItemFromURL.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl)
-   MFPlay non supporta playlist lato server (SSPL) o altri tipi di origine che riproducino più segmenti. In termini tecnici, MFPlay interrompe la riproduzione dopo la prima presentazione e ignora gli eventi [MENewPresentation](menewpresentation.md) dall'origine multimediale.
-   MFPlay non supporta transizioni semplici tra origini multimediali.
-   MFPlay non supporta la combinazione di più flussi video.
-   Solo i formati multimediali supportati in modo nativo Media Foundation sono supportati da MFPlay. Sono inclusi componenti Media Foundation di terze parti che potrebbero essere installati nel sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di MFPlay per la riproduzione audio/video](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



