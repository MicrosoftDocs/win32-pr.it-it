---
description: MPEG-2 Splitter
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: MPEG-2 Splitter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417fcca0bfc7a5c24416cfc2cb915f968c12105d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465257"
---
# <a name="mpeg-2-splitter"></a>MPEG-2 Splitter

A partire da Microsoft® Windows® XP, il filtro mpeg-2 splitter è deprecato. Usare invece [il demultiplexer MPEG-2.](mpeg-2-demultiplexer.md)

Nelle piattaforme precedenti usare lo splitter MPEG-2 per i flussi di programma MPEG-2 recapitati in modalità pull che contengono almeno uno dei tipi di flusso seguenti: video MPEG-2; Audio MPEG-2; Audio AC3 codificato come definito per il video DVD; o audio PCM codificato come definito per il video DVD. Questo filtro analizza i flussi, crea un pin di output per ogni flusso e restituisce i pacchetti audio o video MPEG compressi in un filtro decodificatore MPEG-2.

Per i flussi di programma e trasporto recapitati in modalità push, usare il [demultiplexer MPEG-2](mpeg-2-demultiplexer.md)in tutte le piattaforme.

> [!Note]  
> La barra di divisione MPEG-2 non supporta la ricerca accurata dei frame.

 




| | | Interfacce di filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <strong>ISpecifyPropertyPages,</strong> <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a> | | Tipi di supporti pin di input | <ul><li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</li><li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</li><li>MEDIATYPE_Stream, MEDIASUBTYPE_NULL</li></ul> | | Interfacce pin di input | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipi di supporti pin di output | Dipende dal tipo di flusso. Vedere <a href="mpeg-2-splitter-media-types.md">MpEG-2 Splitter Media Types (Tipi di supporti con separatore MPEG-2)</a> | | Interfacce pin di output | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a> | | Filtrare l'| CLSID CLSID_MMSPLITTER | | Proprietà pagina CLSID | Non applicabile | | File eseguibili | mpg2splt.ax | | <a href="merit.md">|</a> MERIT_NORMAL + 1 | | <a href="filter-categories.md">Filtro categoria |</a> CLSID_AudioInputDeviceCategory | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[Uso della barra di divisione MPEG-2](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



