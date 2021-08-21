---
description: Implementazione di una barra di ricerca
ms.assetid: 384f0732-e0c5-4b1f-b590-195e0acf90e1
title: Implementazione di una barra di ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e86dc52f92a4800639a5dbb1659f70fbe1cfaca7cbc2f0d022df889f970ea5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015549"
---
# <a name="implementing-a-seek-bar"></a>Implementazione di una barra di ricerca

Questa sezione descrive come implementare una barra di ricerca per un'applicazione lettore multimediale. La barra di ricerca viene implementata come controllo trackbar. Per una panoramica della ricerca in DirectShow, vedere Ricerca del [filtro Graph](seeking-the-filter-graph.md).

All'avvio dell'applicazione, inizializzare il trackbar:


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



Il trackbar è disabilitato finché l'utente non apre un file multimediale. L'intervallo del trackbar è impostato da 0 a 100. Durante la riproduzione dei file, l'applicazione calcolerà la posizione di riproduzione come percentuale della durata del file e aggiornerà di conseguenza il trackbar. Ad esempio, la posizione del trackbar "50" corrisponde sempre alla parte centrale del file.

Quando l'utente apre un file, compilare un grafico di riproduzione file usando **RenderFile.** Il codice per questa operazione è illustrato in [How To Play a File](how-to-play-a-file.md). Eseguire quindi una query su Filter Graph Manager per **l'interfaccia IMediaSeeking** e archiviare il puntatore di interfaccia:


```C++
IMediaSeeking *g_pSeek = 0;
hr = pGraph->QueryInterface(IID_IMediaSeeking, (void**)&g_pSeek);
```



Per determinare se il file è ricercabile, chiamare il metodo [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) o [**il metodo IMediaSeeking::GetCapabilities.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) Questi metodi e fanno quasi la stessa cosa, ma la semantica è leggermente diversa. L'esempio seguente **usa CheckCapabilites:**


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



Il \_ flag AM SEEKING CanSeekAbsolute controlla se il file di origine è ricercabile e il \_ flag AM \_ SEEKING CanGetDuration controlla se la durata del file può essere determinata \_ in anticipo. Se sono supportate entrambe le funzionalità, l'applicazione abilita il trackbar e recupera la durata del file.

Se il grafico è ricercabile, l'applicazione userà un timer per aggiornare la posizione del trackbar durante la riproduzione. Quando si esegue il grafico dei filtri per riprodurre il file, avviare l'evento timer chiamando una delle funzioni del timer Windows, ad esempio **SetTimer**. Per altre informazioni sui timer, vedere l'argomento "Timer" in Platform SDK.


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



Usare l'evento timer per aggiornare la posizione del trackbar. Chiamare [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) per recuperare la posizione di riproduzione corrente e quindi calcolare la posizione come percentuale della durata del file:


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



L'utente può anche spostare il trackbar per cercare il file. Quando l'utente trascina o fa clic sul controllo trackbar, l'applicazione riceve un evento \_ WM HSCROLL. La parola più bassa del *parametro wParam* è il messaggio di notifica del trackbar. Ad esempio, TB ENDTRACK viene inviato alla fine dell'azione del trackbar e TB THUMBTRACK viene inviato in modo continuo mentre l'utente \_ \_ trascina il trackbar. Il codice seguente illustra un modo per gestire il messaggio \_ HSCROLL WM:


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



Se l'utente trascina il trackbar, l'applicazione invia una serie di comandi di ricerca, uno per ogni messaggio THUMBTRACK da TB \_ ricevuto. Per rendere le operazioni di ricerca il più uniformi possibile, l'applicazione sospende il grafo. La sospensione del grafo interrompe la riproduzione, ma garantisce che la finestra video sia aggiornata. Quando l'applicazione riceve il messaggio \_ TB ENDTRACK, ripristina lo stato originale del grafo.

 

 



