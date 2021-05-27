---
description: Principali tipi di supporti
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Principali tipi di supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56553ac635f0e767e43e057b2a468027dcefb730
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549576"
---
# <a name="major-media-types"></a>Principali tipi di supporti

In un tipo di supporto, *il tipo principale* descrive la categoria complessiva dei dati, ad esempio audio o video. Il *sottotipo*, se presente, perfeziona ulteriormente il tipo principale. Ad esempio, se il tipo principale è video, il sottotipo potrebbe essere un video RGB a 32 bit. I sottotipi distinguono anche i formati codificati, ad esempio i video H.264, dai formati non compressi.

Il tipo principale e il sottotipo sono identificati dai GUID e archiviati negli attributi seguenti:



| Attributo                                             | Descrizione |
|-------------------------------------------------------|-------------|
| [MF \_ MT \_ MAJOR \_ TYPE](mf-mt-major-type-attribute.md) | Tipo principale. |
| [MF \_ MT \_ SUBTYPE](mf-mt-subtype-attribute.md)        | Sottotipo.    |



 

Vengono definiti i tipi principali seguenti.



| Tipo principale                    | Descrizione                                                                                                                                                | Sottotipi                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **MFMediaType \_ Audio**        | Audio.                                                                                                                                                     | [GUID del sottotipo audio](audio-subtype-guids.md).      |
| **Binario MFMediaType \_**       | Flusso binario.                                                                                                                                             | Nessuno.                                                |
| **MFMediaType \_ FileTransfer** | Flusso che contiene i file di dati.                                                                                                                         | Nessuno.                                                |
| **MFMediaType \_ HTML**         | Flusso HTML.                                                                                                                                               | Nessuno.                                                |
| **Immagine \_ MFMediaType**        | Flusso di immagini ancora.                                                                                                                                        | [GUID WIC e CLSID](../wic/-wic-guids-clsids.md).       |
| **Metadati di \_ MFMediaType**        | Flusso di metadati.                                                                                                                                        | Nessuno.       |
| **MFMediaType \_ Protected**    | Supporti protetti.                                                                                                                                           | Il sottotipo specifica lo schema di protezione del contenuto. |
| **Percezione di MFMediaType \_**   | Flussi da un sensore di fotocamera o da un'unità di elaborazione che causa e comprende i dati video non elaborati e fornisce informazioni sull'ambiente o sugli esseri umani in esso contenuti. | Nessuno.                                                |
| **MFMediaType \_ SAMI**         | Didascalie SAMI (Accessible Media Interchange) sincronizzate.                                                                                                 | Nessuno.                                                |
| **MFMediaType \_ Script**       | Flusso di script.                                                                                                                                             | Nessuno.                                                |
| **Flusso \_ MFMediaType**       | Flusso multiplexed o flusso elementare.                                                                                                                   | [GUID del sottotipo di flusso](stream-subtype-guids.md)     |
| **Video su MFMediaType \_**        | Video.                                                                                                                                                     | [GUID del sottotipo video.](video-subtype-guids.md)      |



 

I componenti di terze parti possono definire nuovi tipi principali e nuovi sottotipi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Tipi di supporti](media-types.md)
</dt> </dl>

 

 
