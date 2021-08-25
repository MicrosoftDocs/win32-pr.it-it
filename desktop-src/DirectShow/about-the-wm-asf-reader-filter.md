---
description: Informazioni sul filtro WM ASF Reader
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: Informazioni sul filtro WM ASF Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b71d0b25070c446ebff88f18785df7b55ba7bbcc7b1bcaa1dcf21995185252ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873701"
---
# <a name="about-the-wm-asf-reader-filter"></a>Informazioni sul filtro WM ASF Reader

La riproduzione dei file ASF viene gestita dal filtro [lettore ASF WM.](wm-asf-reader-filter.md) Quando il lettore ASF WM legge un file, crea automaticamente un pin di output per ogni flusso, inclusi flussi Web, flussi di comandi script e qualsiasi altro tipo di flusso arbitrario. Nel caso di più file con velocità in bit, i pin vengono creati solo per i flussi attualmente selezionati. Per riprodurre un file ASF con il filtro Lettore ASF WM, chiamare [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) o [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).

Wm ASF Reader supporta l'interfaccia [**DirectShow IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) che consente alle applicazioni di eseguire la ricerca temporale all'interno del file. Tuttavia, la riproduzione a velocità diverse da 1.0 (come specificato in [**IMediaSeeking::SetRate)**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)non è supportata.

Il filtro lettore ASF WM espone anche Windows interfacce di Media Format SDK, come descritto nella tabella seguente. Queste interfacce sono documentate nella documentazione Windows Media Format SDK.



| Interfaccia                                             | Modalità di esposizione                                 | Commenti                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | Tramite **IServiceProvider** nel filtro. | Fornito per le applicazioni che devono riprodurre contenuto protetto da Digital Rights Management (DRM).                             |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** sul filtro.           | Fornito in modo che le applicazioni possano leggere gli attributi di file e contenuto, nonché informazioni e metadati su marcatori e script.     |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** sul filtro.           | Implementazione parziale sul filtro in modo che le applicazioni possano accedere ai metodi in formato informativo nell'oggetto Reader WM.         |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** sul filtro.           | Implementazione parziale sul filtro in modo che le applicazioni possano accedere ai metodi in formato informativo nell'oggetto lettore di Format SDK. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



