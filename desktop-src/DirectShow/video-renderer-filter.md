---
description: Filtro renderer video
ms.assetid: 7719ed9d-e3b9-4c84-b587-4e120b5cabf8
title: Filtro renderer video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96df49305b357cf4a889d283c64839c13c38e2b8f89b8d4eda35d06260f18c58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083501"
---
# <a name="video-renderer-filter"></a>Filtro renderer video

Il filtro Renderer video è un renderer video affidabile e per tutti gli scopi.

> [!Note]  
> In Windows XP e versioni successive, il renderer video predefinito è [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7). VmR-7 e il renderer video hanno entrambi il nome descrittivo "Renderer video". Nelle piattaforme precedenti, il renderer video è il renderer predefinito. Vedere [Scelta del renderer di destra.](choosing-the-right-renderer.md)

 

Il renderer video usa DirectDraw e le superfici di sovrapposizione, se supportate dalla scheda video. Filter Graph Manager espone [**l'interfaccia IVideoWindow,**](/windows/desktop/api/Control/nn-control-ivideowindow) che consente alle applicazioni di impostare e recuperare le proprietà nel renderer video. Con le schede video più nuove, il renderer video supporta il rendering a schermo intero. In caso contrario, gestione Graph passa automaticamente al filtro [renderer](full-screen-renderer-filter.md) a schermo intero per la modalità schermo intero. Per altre informazioni, vedere [**IVideoWindow::p ut \_ FullScreenMode.**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode)

-   \[! Importante\]  
    > In genere, la finestra video di questo filtro elabora i messaggi in un thread di lavoro creato da Filter Graph Manager. Howerver, se un'applicazione crea direttamente il filtro usando **CoCreateInstance,** la finestra video elabora i messaggi nel thread dell'applicazione. In tal caso, il thread dell'applicazione deve avere un ciclo di messaggi per inviare messaggi alla finestra video. Inoltre, il thread non deve  uscire fino alla chiamata finale release al renderer video, che si verifica all'arresto di Filter Graph Manager. In caso contrario, l'applicazione potrebbe deadlock.

     



| Etichetta | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IBasicVideo,**](/windows/desktop/api/Control/nn-control-ibasicvideo) [**IBasicVideo2,**](/windows/desktop/api/Control/nn-control-ibasicvideo2) [**IDirectDrawVideo,**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo) [**IKsPropertySet,**](ikspropertyset.md) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IQualProp,**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) |
| Tipi di supporti pin di input                    | Formati video non compressi.                                                                                                                                                                                                                                                                                                                                                                              |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                           |
| Tipi di supporti pin di output                   | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                          |
| Interfacce pin di output                    | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                          |
| CLSID del filtro                             | CLSID \_ VideoRenderer                                                                                                                                                                                                                                                                                                                                                                                     |
| CLSID pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                                                                                                                                                                                                                                                                                                        |
| File eseguibile                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                                               |
| [Merito](merit.md)                       | Windows XP e versioni successive: **PROBABILITÀ \_ IMPROBABILE**                                                                                                                                                                                                                                                                                                                                                                |
| [Categoria filtro](filter-categories.md) | **CLSID \_ LegacyAmFilterCategory**                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Commenti

Nella versione di debug di Quartz.dll, se il livello di debug LOG TRACE è impostato su 5 o su un valore superiore, il renderer video visualizza i timestamp di ogni fotogramma nella finestra \_ video. Questi numeri non vengono visualizzati nella versione definitiva della DLL. Per altre informazioni, vedere [Funzioni di output di debug.](debug-output-functions.md)

Le osservazioni seguenti sono destinate agli sviluppatori di filtri:

Il renderer video accetta i formati YUV se la scheda grafica video supporta le superfici di sovrapposizione YUV. Quando si connette per la prima volta al filtro upstream, tuttavia, il renderer video richiede un formato RGB corrispondente alla profondità del colore delle impostazioni correnti del monitor. Ad esempio, se l'impostazione di visualizzazione corrente è a 24 bit, il filtro upstream deve essere in grado di fornire video RGB a 24 bit. Quando il grafico dei filtri passa a uno stato di esecuzione, il renderer video negozia una modifica del formato dinamico nello spazio colore YUV appropriato.

Connettendosi con un tipo RGB, il renderer video garantisce che possa usare GDI nel caso in cui DirectDraw non sia disponibile. Passa a GDI se un'altra applicazione usa la memoria video, se il rettangolo video si trova in due monitor in un sistema a più monitor o se il rettangolo video è completamente nascosto da un'altra finestra.

> [!Note]  
> Il renderer di combinazione video non esegue questo tipo di modifica del formato dinamico e non richiede un tipo di supporto RGB, perché non usa mai GDI per il rendering.

 

Per negoziare una modifica del formato, il renderer video chiama [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) con il nuovo tipo di supporto. Se il filtro upstream restituisce S \_ OK, il renderer video collega il nuovo supporto all'esempio successivo. Il filtro upstream deve chiamare [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) per ogni esempio. Se **GetMediaType** restituisce un valore non **NULL,** indica una modifica del formato e il filtro upstream deve rispondere scambiando i tipi di output. Non cambiare tipo nel **metodo QueryAccept.** Il filtro upstream deve accettare almeno i tipi RGB principali e idealmente deve supportare i tipi YUV comuni. Durante lo streaming, il renderer video può passare da un tipo YUV a un altro e da un tipo RGB a un numero qualsiasi di volte. Il renderer video non accetta modifiche di formato dinamico avviate dal filtro upstream.

Quando il renderer video disegna su una superficie di sovrapposizione DirectDraw, alloca un singolo buffer per il pin di input. Se il filtro upstream tenta di forzare una connessione usando più buffer, il renderer video non sarà in grado di usare la superficie di sovrapposizione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 



