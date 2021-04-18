---
description: Supporto ASF in Media Foundation
ms.assetid: 4b0c4a83-623a-4378-9436-35ed120316af
title: Supporto ASF in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb7774d0ddaee592cb583ffb771c900642ed216
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320564"
---
# <a name="asf-support-in-media-foundation"></a>Supporto ASF in Media Foundation

Media Foundation supporta i file multimediali nel formato ASF (Advanced Systems Format):

-   Windows Media Video (file WMV)
-   Windows Media Audio (file WMA)

Media Foundation fornisce diversi oggetti per la lettura e la scrittura di file ASF. Questi oggetti sono disponibili in due livelli architetturali diversi.

In primo luogo, il livello della *pipeline* contiene gli oggetti che funzionano all'interno della [pipeline Media Foundation](media-foundation-pipeline.md) e sono conformi alle API definite dalla pipeline. Il livello della pipeline ASF contiene:

-   [Origine multimediale ASF](asf-media-source.md): analizza i file ASF e recapita i pacchetti di dati audio/video.
-   [Codec Windows Media](windows-media-codecs.md): decodifica o codifica i flussi audio o video di Windows Media.
-   [Sink multimediale ASF](asf-media-sinks.md): riceve i pacchetti di dati e scrive un file ASF.

In secondo luogo, il livello contenitore WM fornisce il controllo di basso livello sull'analisi e la scrittura di un file ASF. Il livello della pipeline utilizza WMContainer internamente. Le applicazioni possono anche usare WMContainer per l'analisi e la scrittura di basso livello ASF.

![diagramma che Mostra gli elementi del livello pipeline e il contenitore WM](images/asf-components.png)

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                         | Descrizione                                                                                                        |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Struttura di file ASF](asf-file-structure.md)<br/>                       | Cenni preliminari sulla struttura dei file ASF e sugli oggetti forniti da Media Foundation per lavorare con i file ASF.<br/> |
| [Componenti ASF a livello pipeline](pipeline-layer-asf-components.md)<br/> | Viene descritto come analizzare e creare file ASF utilizzando il livello pipeline.<br/>                                   |
| [Componenti ASF WMContainer](wmcontainer-asf-components.md)<br/>       | Viene descritto come analizzare e creare file ASF usando il livello WMContainer.<br/>                                |



 

Per informazioni dettagliate sulla struttura di un file ASF, vedere la specifica ASF, che può essere scaricata da questo [sito Web Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione di Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 




