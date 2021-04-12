---
description: Filtro renderer video
ms.assetid: 7719ed9d-e3b9-4c84-b587-4e120b5cabf8
title: Filtro renderer video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c71e72375a43a57ce94b38d01f48abba9309e603
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226494"
---
# <a name="video-renderer-filter"></a>Filtro renderer video

Il filtro renderer video è un potente renderer video per tutti gli scopi.

> [!Note]  
> In Windows XP e versioni successive, il renderer video predefinito è il [filtro del renderer video mixing 7](video-mixing-renderer-filter-7.md) (VMR-7). VMR-7 e il renderer video hanno entrambi il nome descrittivo "renderer video". Sulle piattaforme precedenti, il renderer video è il renderer predefinito. Vedere [scelta del renderer appropriato](choosing-the-right-renderer.md).

 

Se la scheda video li supporta, il renderer video usa le superfici DirectDraw e overlay. Filter Graph Manager espone l'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) , che consente alle applicazioni di impostare e recuperare le proprietà nel renderer video. Con le schede video più recenti, il renderer video supporta il rendering a schermo intero. In caso contrario, il gestore del grafico dei filtri passa automaticamente al filtro [renderer](full-screen-renderer-filter.md) a schermo intero per la modalità schermo intero. Per ulteriori informazioni, vedere [**IVideoWindow::p UT \_ FullScreenMode**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode) .

-   \[! Importante\]  
    > In genere, la finestra video di questo filtro elabora i messaggi in un thread di lavoro creato da Filter Graph Manager. Tuttavia, se un'applicazione crea direttamente il filtro utilizzando **CoCreateInstance**, la finestra del video elabora i messaggi nel thread dell'applicazione. In tal caso, è necessario che il thread dell'applicazione disponga di un ciclo di messaggi per inviare messaggi alla finestra del video. Inoltre, il thread non deve uscire fino alla chiamata di **rilascio** finale al renderer video, che si verifica quando il gestore del grafico del filtro viene arrestato. In caso contrario, l'applicazione potrebbe verificarsi un deadlock.

     



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2), [**IDirectDrawVideo**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo), [**IKsPropertySet**](ikspropertyset.md), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop), [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) |
| Tipi di supporti pin di input                    | Formati video non compressi.                                                                                                                                                                                                                                                                                                                                                                              |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**iOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                           |
| Tipi di supporti pin di output                   | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                          |
| Interfacce del PIN di output                    | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                          |
| CLSID filtro                             | \_VIDEORENDERER CLSID                                                                                                                                                                                                                                                                                                                                                                                     |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                                                                                                                                                                                                                                                                                                        |
| File eseguibile                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                                               |
| [Merito](merit.md)                       | Windows XP e versioni successive: **Merit \_ improbabile**                                                                                                                                                                                                                                                                                                                                                                |
| [Categoria filtro](filter-categories.md) | **\_LEGACYAMFILTERCATEGORY CLSID**                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Commenti

Nella versione di debug di Quartz.dll, se il livello di debug della traccia di LOG \_ è impostato su 5 o superiore, il renderer video Visualizza i timestamp di ogni frame nella finestra del video. Questi numeri non vengono visualizzati nella versione finale della DLL. Per altre informazioni, vedere [debug di funzioni di output](debug-output-functions.md).

Le osservazioni seguenti sono destinate agli sviluppatori di filtri:

Il renderer video accetta formati YUV se la scheda grafica video supporta le superfici della sovrimpressione YUV. Quando si connette per la prima volta al filtro upstream, tuttavia, il renderer video richiede un formato RGB che corrisponda alla profondità di colore delle impostazioni di monitoraggio correnti. Se, ad esempio, l'impostazione di visualizzazione corrente è il colore a 24 bit, il filtro upstream deve essere in grado di fornire video RGB a 24 bit. Quando il grafico di filtro passa a uno stato runing, il renderer video negozia una modifica di formato dinamico nello spazio colore YUV appropriato.

Connettendosi a un tipo RGB, il renderer video garantisce che sia possibile utilizzare GDI nel caso in cui DirectDraw non sia disponibile. Passa a GDI se un'altra applicazione sta usando la memoria video, se il rettangolo video si trova in un sistema a più monitor o se il rettangolo video è completamente nascosto da un'altra finestra.

> [!Note]  
> Il renderer di mixaggio video non esegue questo tipo di modifica del formato dinamico e non richiede un tipo di supporto RGB, perché non usa mai GDI per il rendering.

 

Per negoziare una modifica di formato, il renderer video chiama [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) con il nuovo tipo di supporto. Se il filtro upstream restituisce S \_ OK, il renderer video collegherà il nuovo supporto all'esempio successivo. Il filtro upstream deve chiamare [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) per ogni esempio. Se **GetMediaType** restituisce un valore non **null** , indica una modifica del formato e il filtro upstream deve rispondere cambiando i tipi di output. Non cambiare i tipi nel metodo **QueryAccept** . Il filtro upstream deve accettare almeno i tipi RGB principali e idealmente deve supportare i tipi YUV comuni. Durante lo streaming, il renderer video potrebbe spostarsi tra i tipi YUV e RGB per un numero qualsiasi di volte. Il renderer video non accetta modifiche al formato dinamico avviate dal filtro upstream.

Quando il renderer video disegna in una superficie sovrapposta DirectDraw, alloca un singolo buffer per il pin di input. Se il filtro upstream tenta di forzare una connessione utilizzando più buffer, il renderer video non sarà in grado di utilizzare la superficie della sovrimpressione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



