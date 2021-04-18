---
description: Uso della barra di divisione MPEG-2
ms.assetid: a08e079c-41be-475a-9e88-ee46d17fe938
title: Uso della barra di divisione MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60505ef242c2ed9c1eab3031a005a2582b99608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314385"
---
# <a name="using-the-mpeg-2-splitter"></a>Uso della barra di divisione MPEG-2

> [!Note]  
> A partire da Microsoft® Windows® XP, il filtro della barra di divisione MPEG-2 è deprecato. Usare invece [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) .

 

Il filtro Splitter MPEG-2 supporta la riproduzione in modalità pull dei flussi di programma MPEG-2 che contengono almeno uno dei tipi di flusso seguenti.

-   Video MPEG-2
-   Audio MPEG-2
-   Audio Dolby AC-3 codificato come definito per DVD-Video
-   LPCM (Linear Pulse Code modulata) audio codificato come definito per DVD-Video

Per un elenco dei tipi di supporto supportati dal separatore MPEG-2, vedere tipi di supporto per la [barra di divisione MPEG-2](mpeg-2-splitter-media-types.md).

Il separatore MPEG-2 non analizza i flussi di trasporto. Usare il filtro di demultiplexing MPEG-2 per i flussi di trasporto (solo modalità push).

**Timestamp**

Quando si esegue la riproduzione dei flussi di programma MPEG-2, il filtro con separatore MPEG-2 considera il primo riferimento all'orologio di sistema rilevato come origine dell'ora di qualsiasi flusso. Questo comportamento è diverso dal [separatore di flusso MPEG-1](mpeg-1-stream-splitter-filter.md), che usa i timestamp di presentazione. Il metodo [**IAMParse:: GetParseTime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) restituisce il tempo di clock del sistema di flusso (probabilmente stimato) per i dati elaborati.

Se il filtro della barra di divisione MPEG-2 rileva un campione di input con il set di proprietà di discontinuità (la proprietà discontinuità può essere impostata tramite [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) o [**IMediaSample2:: seproperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)) ignora i dati fino a quando non trova il primo pacchetto nei dati e ne modifica i timestamp in modo che il riferimento all'orologio di sistema (SCR) per il pacchetto venga considerato identico all'ora di SCR prima della discontinuità. Se il clock SCR viene visualizzato per tornare indietro o per andare avanti di più di un secondo, quindi, in linea con la specifica MPEG-2 Program Stream, viene trattato anche come una discontinuità di clock e la discrepanza di clock apparente viene sottratta dai timestamp passati ai filtri downstream.

**Selezione flusso**

Quando si esegue la riproduzione del flusso di programma MPEG-2, vengono scelti il primo flusso video e il primo flusso audio trovato attraversando il flusso del programma. Sono supportati fino a un pin audio e un pin di output video. Tramite l'interfaccia [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) , è possibile selezionare flussi diversi dello stesso tipo fino al numero specificato dal limite audio nell'intestazione di sistema. Per l'audio MPEG-2, attualmente si presuppone che i flussi formino un intervallo contiguo a partire dal flusso 0xC0.

**Interfacce supportate**

Il filtro separatore MPEG-2 supporta le interfacce seguenti.

-   [**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse). Solo flusso di programma MPEG-2.
-   [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect). Solo flusso di programma MPEG-2, solo flussi audio.
-   [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking). Include la ricerca in modalità byte.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto MPEG-2 in DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



