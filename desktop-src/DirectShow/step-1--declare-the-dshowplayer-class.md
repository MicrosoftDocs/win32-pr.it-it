---
description: Questo argomento è il passaggio 1 della riproduzione audio/video dell'esercitazione in DirectShow.
ms.assetid: 3ccd201d-e60d-40bf-a602-6d42df03b36b
title: 'Passaggio 1: dichiarare la classe DShowPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22ff36a76be8017f7b468815cf572514900f8d11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314409"
---
# <a name="step-1-declare-the-dshowplayer-class"></a>Passaggio 1: dichiarare la classe DShowPlayer

Questo argomento è il passaggio 1 della [riproduzione audio/video dell'esercitazione in DirectShow](audio-video-playback-in-directshow.md). Il codice completo è illustrato nell'esempio relativo alla [riproduzione DirectShow](directshow-playback-example.md).

In questa esercitazione la `DShowPlayer` classe gestisce tutte le funzionalità DirectShow. Questa classe è dichiarata come folows.


```C++
#include <new>
#include <windows.h>
#include <dshow.h>


enum PlaybackState
{
    STATE_NO_GRAPH,
    STATE_RUNNING,
    STATE_PAUSED,
    STATE_STOPPED,
};

const UINT WM_GRAPH_EVENT = WM_APP + 1;

typedef void (CALLBACK *GraphEventFN)(HWND hwnd, long eventCode, LONG_PTR param1, LONG_PTR param2);

class DShowPlayer
{
public:
    DShowPlayer(HWND hwnd);
    ~DShowPlayer();

    PlaybackState State() const { return m_state; }

    HRESULT OpenFile(PCWSTR pszFileName);
    
    HRESULT Play();
    HRESULT Pause();
    HRESULT Stop();

    BOOL    HasVideo() const;
    HRESULT UpdateVideoWindow(const LPRECT prc);
    HRESULT Repaint(HDC hdc);
    HRESULT DisplayModeChanged();

    HRESULT HandleGraphEvent(GraphEventFN pfnOnGraphEvent);

private:
    HRESULT InitializeGraph();
    void    TearDownGraph();
    HRESULT CreateVideoRenderer();
    HRESULT RenderStreams(IBaseFilter *pSource);

    PlaybackState   m_state;

    HWND m_hwnd; // Video window. This window also receives graph events.

    IGraphBuilder   *m_pGraph;
    IMediaControl   *m_pControl;
    IMediaEventEx   *m_pEvent;
    CVideoRenderer  *m_pVideo;
};
```





Note:

-   L' `PlaybackState` enumerazione descrive lo stato corrente dell' `DShowPlayer` oggetto.
-   L'evento costante WM \_ Graph \_ definisce un messaggio di finestra privata. Questo messaggio viene utilizzato per notificare all'applicazione gli eventi del grafico del filtro. Vedere [passaggio 6: gestire gli eventi del grafo](step-6--handle-graph-events.md).
-   `GraphEventFN` puntatore a una funzione di callback per la gestione degli eventi del grafo del filtro. Questa funzione di callback viene implementata dall'applicazione.
-   La variabile membro *\_ pVideo m* fornisce un wrapper per i diversi renderer video DirectShow. Vedere [passaggio 2: dichiarare CVideoRenderer e classi derivate](step-2--declare-cvideorenderer-and-derived-classes.md).
-   In questa esercitazione, la funzione [SafeRelease](../medfound/saferelease.md) viene usata per rilasciare i puntatori di interfaccia com.

[Passaggio 2: dichiarare CVideoRenderer e le classi derivate](step-2--declare-cvideorenderer-and-derived-classes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione audio/video in DirectShow](audio-video-playback-in-directshow.md)
</dt> </dl>

 

 
