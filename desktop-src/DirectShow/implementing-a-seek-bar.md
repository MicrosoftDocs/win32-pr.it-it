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
# <a name="implementing-a-seek-bar"></a>Implementazione di una barra di ricerca

In questa sezione viene descritto come implementare una barra di ricerca per un'applicazione Media Player. La barra di ricerca viene implementata come controllo TrackBar. Per una panoramica della ricerca in DirectShow, vedere [seeking the Filter Graph](seeking-the-filter-graph.md).

All'avvio dell'applicazione, inizializzare il TrackBar:


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



Il TrackBar viene disabilitato fino a quando l'utente non apre un file multimediale. L'intervallo TrackBar è impostato da 0 a 100. Durante la riproduzione del file, l'applicazione calcolerà la posizione di riproduzione come percentuale della durata del file e aggiornerà il TrackBar di conseguenza. Ad esempio, la posizione di TrackBar "50" corrisponde sempre al centro del file.

Quando l'utente apre un file, compila un grafico di riproduzione file usando **RenderFile**. Il codice per questa operazione viene illustrato in [come riprodurre un file](how-to-play-a-file.md). Eseguire quindi una query su Filter Graph Manager per l'interfaccia **IMediaSeeking** e archiviare il puntatore di interfaccia:


```C++
IMediaSeeking *g_pSeek = 0;
hr = pGraph->QueryInterface(IID_IMediaSeeking, (void**)&g_pSeek);
```



Per determinare se il file è ricercabile, chiamare il metodo [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) o [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) . Questi metodi eseguono quasi la stessa operazione, ma la loro semantica è leggermente diversa. L'esempio seguente usa **CheckCapabilites**:


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



Il \_ \_ flag CanSeekAbsolute seeking controlla se il file di origine è ricercabile e il \_ flag CanGetDuration seeking \_ Controlla se è possibile determinare in anticipo la durata del file. Se entrambe le funzionalità sono supportate, l'applicazione Abilita il TrackBar e recupera la durata del file.

Se il grafico è ricercabile, l'applicazione userà un timer per aggiornare la posizione di TrackBar durante la riproduzione. Quando si esegue il grafico del filtro per riprodurre il file, avviare l'evento del timer chiamando una delle funzioni timer di Windows, ad esempio **setimer**. Per ulteriori informazioni sui timer, vedere l'argomento "timer" in Platform SDK.


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



Utilizzare l'evento timer per aggiornare la posizione del TrackBar. Chiamare [**IMediaSeeking:: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) per recuperare la posizione di riproduzione ribes, quindi calcolare la posizione come percentuale della durata del file:


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



L'utente può anche spostare il TrackBar per cercare il file. Quando l'utente trascina o fa clic sul controllo TrackBar, l'applicazione riceve un \_ evento HSCROLL di WM. La parola bassa del parametro *wParam* è il messaggio di notifica TrackBar. Ad esempio, TB \_ ENDTRACK viene inviato alla fine dell'azione TrackBar e TB \_ THUMBTRACK viene inviato continuamente mentre l'utente trascina il TrackBar. Il codice seguente illustra un modo per gestire il \_ messaggio HSCROLL di WM:


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



Se l'utente trascina il TrackBar, l'applicazione emette una serie di comandi Seek, uno per ogni \_ messaggio THUMBTRACK TB che riceve. Per fare in modo che le operazioni di ricerca siano più agevoli possibile, l'applicazione sospende il grafo. La sospensione del grafico interrompe la riproduzione ma garantisce che la finestra video venga aggiornata. Quando l'applicazione riceve il \_ messaggio TB ENDTRACK, ripristina lo stato originale del grafico.

 

 



