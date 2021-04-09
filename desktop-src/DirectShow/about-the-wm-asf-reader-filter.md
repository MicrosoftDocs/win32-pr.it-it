---
description: Informazioni sul filtro WM ASF Reader
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: Informazioni sul filtro WM ASF Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350e6597aa6aa66193af37a30ed54c37139d5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876858"
---
# <a name="about-the-wm-asf-reader-filter"></a>Informazioni sul filtro WM ASF Reader

La riproduzione dei file ASF viene gestita dal filtro [WM ASF Reader](wm-asf-reader-filter.md) . Quando il lettore WM ASF legge un file, viene creato automaticamente un pin di output per ogni flusso, inclusi i flussi Web, i flussi dei comandi di script e qualsiasi altro tipo di flusso arbitrario. Nel caso di file a più velocità in bit, i PIN vengono creati solo per i flussi attualmente selezionati. Per riprodurre un file ASF con il filtro WM ASF Reader, chiamare [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) o [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).

Il lettore WM ASF supporta l'interfaccia DirectShow [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , che consente alle applicazioni di eseguire ricerche temporali all'interno del file. Tuttavia, la riproduzione a velocità diverse da 1,0 (come specificato in [**IMediaSeeking:: serate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)) non è supportata.

Il filtro WM ASF Reader espone inoltre diverse interfacce di Windows Media Format SDK, come descritto nella tabella seguente. Queste interfacce sono documentate nella documentazione di Windows Media Format SDK.



| Interfaccia                                             | Modalità di esposizione                                 | Commenti                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | Tramite **IServiceProvider** sul filtro. | Fornito per le applicazioni che devono riprodurre contenuti protetti da Rights Management digitali (DRM).                             |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** sul filtro.           | Fornito in modo che le applicazioni possano leggere gli attributi di file e contenuto, nonché informazioni su marcatore e script e metadati.     |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** sul filtro.           | Implementato parzialmente sul filtro in modo che le applicazioni possano accedere ai metodi informativi nell'oggetto WM Reader.         |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** sul filtro.           | Implementato parzialmente sul filtro in modo che le applicazioni possano accedere ai metodi informativi nell'oggetto Reader di Format SDK. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



