---
description: Supporto di ASF in Media Foundation
ms.assetid: 4b0c4a83-623a-4378-9436-35ed120316af
title: Supporto di ASF in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db06c5a294e351b09d7f5327e8ee22891798671765bc5cc10eafd75785debde9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880959"
---
# <a name="asf-support-in-media-foundation"></a>Supporto di ASF in Media Foundation

Media Foundation supporta i file multimediali in Advanced Systems Format (ASF):

-   Windows Video multimediali (file WMV)
-   Windows Audio multimediale (file WMA)

Media Foundation fornisce diversi oggetti per la lettura e la scrittura di file ASF. Questi oggetti vengono forniti in due diversi livelli dell'architettura.

In primo luogo, *il* livello pipeline contiene oggetti che funzionano all'interno [Media Foundation pipeline](media-foundation-pipeline.md) e sono conformi alle API definite dalla pipeline. Il livello pipeline di ASF contiene:

-   [Origine multimediale ASF:](asf-media-source.md)analizza i file ASF e recapita i pacchetti di dati audio/video.
-   [Windows codec multimediali:](windows-media-codecs.md)decodificare o codificare Windows flussi audio o video multimediali.
-   [Sink multimediale ASF:](asf-media-sinks.md)riceve pacchetti di dati e scrive un file ASF.

In secondo momento, il livello contenitore WM offre un controllo di basso livello sull'analisi e la scrittura di un file ASF. Il livello pipeline usa WMContainer internamente. Le applicazioni possono anche usare WMContainer per l'analisi e la scrittura di ASF di basso livello.

![Diagramma che mostra gli elementi del livello pipeline e del contenitore wm](images/asf-components.png)

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                         | Descrizione                                                                                                        |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Struttura del file ASF](asf-file-structure.md)<br/>                       | Panoramica della struttura dei file ASF e degli oggetti forniti da Media Foundation usare i file ASF.<br/> |
| [Componenti ASF del livello pipeline](pipeline-layer-asf-components.md)<br/> | Viene descritto come analizzare e creare file ASF usando il livello pipeline.<br/>                                   |
| [Componenti ASF WMContainer](wmcontainer-asf-components.md)<br/>       | Descrive come analizzare e creare file ASF usando il livello WMContainer.<br/>                                |



 

Per informazioni dettagliate sulla struttura di un file ASF, vedere la specifica ASF, che può essere scaricata da questo [sito Web Microsoft.](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation di programmazione](media-foundation-programming-guide.md)
</dt> </dl>

 

 




