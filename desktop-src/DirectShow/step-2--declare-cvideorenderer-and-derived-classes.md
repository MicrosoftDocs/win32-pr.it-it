---
description: Questo argomento è il passaggio 2 dell'esercitazione Riproduzione audio/video in DirectShow.
ms.assetid: 61106781-d10c-41a8-993e-121e0a1e4c4d
title: 'Passaggio 2: Dichiarare CVideoRenderer e classi derivate'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fae4c9c391a13acd0ede06b9a74c3b09bd264a6b74c42d7f6c7ca5e9dbb17051
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050361"
---
# <a name="step-2-declare-cvideorenderer-and-derived-classes"></a>Passaggio 2: Dichiarare CVideoRenderer e classi derivate

Questo argomento è il passaggio 2 dell'esercitazione [Riproduzione audio/video in DirectShow](audio-video-playback-in-directshow.md). Il codice completo è illustrato nell'argomento DirectShow [esempio di riproduzione](directshow-playback-example.md).

DirectShow fornisce diversi filtri che eseguono il rendering del video:

-   [**Filtro renderer video**](enhanced-video-renderer-filter.md) avanzato (EVR)
-   [Filtro renderer di combinazione video 9](video-mixing-renderer-filter-9.md) (VMR-9)
-   [Filtro renderer di combinazione video 7](video-mixing-renderer-filter-7.md) (VMR-7)

Per altre informazioni sulle differenze tra questi filtri, vedere [Scelta del renderer video giusto.](choosing-the-right-renderer.md)

In questa esercitazione viene usata la classe astratta seguente per eseguire il wrapping del filtro del renderer video.


```C++
// Abstract class to manage the video renderer filter.
// Specific implementations handle the VMR-7, VMR-9, or EVR filter.

class CVideoRenderer
{
public:
    virtual ~CVideoRenderer() {};
    virtual BOOL    HasVideo() const = 0;
    virtual HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd) = 0;
    virtual HRESULT FinalizeGraph(IGraphBuilder *pGraph) = 0;
    virtual HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc) = 0;
    virtual HRESULT Repaint(HWND hwnd, HDC hdc) = 0;
    virtual HRESULT DisplayModeChanged() = 0;
};
```



Note:

-   Il `HasVideo` metodo restituisce TRUE **se** il renderer video è stato creato.
-   Il `AddToGraph` metodo aggiunge il renderer video al grafico dei filtri.
-   Il `FinalizeGraph` metodo completa il passaggio di creazione del grafo.
-   Il `UpdateVideoWindow` metodo aggiorna il rettangolo di destinazione video.
-   Il `Repaint` metodo ridisegna il fotogramma video corrente.
-   Il `DisplayModeChanged` metodo gestisce le modifiche della modalità di visualizzazione.

Ognuno di questi metodi è descritto in dettaglio più avanti in questa esercitazione.

Dichiarare quindi una classe derivata per eseguire il wrapping di ognuno dei tre renderer video: EVR, VMR-9 e VMR-7.

### <a name="cevr-class"></a>Classe CEVR

La `CEVR` classe gestisce l'EVR. Contiene un puntatore alle [**interfacce IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) e [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) dell'EVR.


```C++
// Manages the EVR video renderer filter.

class CEVR : public CVideoRenderer
{
    IBaseFilter            *m_pEVR;
    IMFVideoDisplayControl *m_pVideoDisplay;

public:
    CEVR();
    ~CEVR();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr9-class"></a>Classe CVMR9

La `CVMR9` classe gestisce vmr-9. Contiene un puntatore [**all'interfaccia IVMRWindowlessControl9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9)


```C++
// Manages the VMR-9 video renderer filter.

class CVMR9 : public CVideoRenderer
{
    IVMRWindowlessControl9 *m_pWindowless;

public:
    CVMR9();
    ~CVMR9();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr7-class"></a>Classe CVMR7

La `CVMR7` classe gestisce vmr-7. Contiene un puntatore [**all'interfaccia IVMRWindowlessControl.**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol)


```C++
// Manages the VMR-7 video renderer filter.

class CVMR7 : public CVideoRenderer
{
    IVMRWindowlessControl   *m_pWindowless;

public:
    CVMR7();
    ~CVMR7();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



Passaggio [3: Compilare il filtro Graph](step-3--build-the-filter-graph.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione audio/video in DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Uso del renderer di combinazione video](using-the-video-mixing-renderer.md)
</dt> <dt>

[Video Rendering](video-rendering.md)
</dt> </dl>

 

 
