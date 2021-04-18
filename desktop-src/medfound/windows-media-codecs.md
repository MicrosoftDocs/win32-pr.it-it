---
description: I codec Windows Media Audio e video sono una raccolta di oggetti che è possibile usare per comprimere e decomprimere i dati multimediali digitali.
ms.assetid: 74de2e75-b1ee-436d-8d78-efe366ab7aa6
title: Codec Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec98f98fbd0561b291dfc4cc18e4270bf363baf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320801"
---
# <a name="windows-media-codecs"></a>Codec Windows Media

I codec Windows Media Audio e video sono una raccolta di oggetti che è possibile usare per comprimere e decomprimere i dati multimediali digitali. Ogni codec è costituito da due oggetti, un codificatore e un decodificatore. In questa parte della documentazione viene descritto come utilizzare le funzionalità dei codec Windows Media Audio e video per produrre e utilizzare flussi di dati compressi.

> [!Note]  
> Questa documentazione è destinata principalmente agli sviluppatori che desiderano utilizzare codec Windows Media nelle applicazioni multimediali basate su C++. Per una panoramica tecnica delle funzionalità dei codec Windows Media, vedere [informazioni sui codec Windows Media](about-the-windows-media-codecs.md).

 

Il termine *codec* è un amalgama dei termini compressore e decompressore. Un codec viene in genere implementato come una coppia di oggetti COM: uno per la codifica del contenuto e un altro per la decodifica del contenuto. In alcuni casi gli oggetti COM occupano la stessa libreria a collegamento dinamico (DLL).

Ogni oggetto codec implementa due interfacce separate ma simili:



| Interfaccia                              | Descrizione                                 |
|----------------------------------------|---------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Compatibile con Microsoft Media Foundation. |
| [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Compatibile con DirectShow.                 |



 

Sono disponibili diversi codec per audio e video, ma anche codec diversi per diversi tipi di contenuto che possono essere inseriti in un file audio o video. Gli algoritmi usati per comprimere e decomprimere i dati per le parole pronunciate differiscono dagli algoritmi usati per comprimere e decomprimere i dati di musica.

## <a name="codec-descriptions"></a>Descrizioni codec

Nella tabella seguente vengono descritti gli utilizzi previsti dei codec Windows Media.



| Codec                                                                     | Descrizione                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Media Audio](windowsmediaaudioencoder.md)                       | Un codec audio che supporta tre categorie di contenuto codificato: standard, Professional e lossless.                                                                                                                                                                                      |
| [Windows Media Audio Voice](windowsmediaaudiovoiceencoder.md)            | Codec audio ottimizzato per la codifica della voce umana a rapporti di compressione elevati. Questo è il codec preferito per i flussi costituiti principalmente da parole vocali. Per contenuti con musica mista e sintesi vocale, questo codec può modificare dinamicamente l'algoritmo di codifica usato per ottenere la qualità ottimale. |
| [Windows Media Video 9](windowsmediavideo9encoder.md)                    | Un codec video che supporta quattro categorie di contenuto codificato: profilo semplice, profilo principale, profilo avanzato e immagine.                                                                                                                                                                  |
| [Schermata Windows Media Video 9](usingthewindowsmediavideo9screencodec.md) | Codec video ottimizzato per la codifica di schermate sequenziali dai monitoraggi computer. Questo codec viene spesso utilizzato per il training o il supporto software registrando le immagini di monitoraggio durante l'utilizzo delle applicazioni del computer.                                                                         |



 

Le versioni più recenti degli oggetti codec consentono anche l'accesso ad alcuni codec legacy, tra cui Windows Media Video 7 e 8, Windows Media Screen 7, i precedenti codec Microsoft MPEG-4 e i codec MPEG-4 Microsoft ISO.

> [!Note]  
> Questa documentazione non copre questi codec legacy; vengono illustrate solo le versioni correnti dei codec.

 

Per i codec precedenti, usare le stesse procedure di quando si usano i codec correnti; Tuttavia, tenere presente che non tutte le funzionalità sono supportate in tutti i codec.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Informazioni sui codec Windows Media](about-the-windows-media-codecs.md)
-   [Uso degli oggetti codec e DSP](decidinghowtousethewindowsmediaaudioandvideocodecs.md)
-   [Metodi di codifica](encodingmethods.md)
-   [Implementazione del codec](codecimplementation.md)
-   [Modello di buffer di bucket a perdita](the-leaky-bucket-buffer-model.md)
-   [Uso di codec DMOs](workingwithcodecdmos.md)
-   [Uso di codec MFTs](workingwithcodecmfts.md)
-   [Utilizzo di audio](workingwithaudio.md)
-   [Uso dei video](workingwithvideo.md)
-   [Archiviazione di supporti compressi in file AVI](storingcompressedmediainavifiles.md)
-   [Uso della codifica VBR](usingvbrencoding.md)
-   [Uso della codifica Two-Pass](usingtwoencodingpasses.md)
-   [Recupero delle statistiche di codifica](gettingencodingstatistics.md)
-   [Uso delle estensioni dell'unità dati](usingdataunitextensions.md)
-   [Costanti IPropertyBag codec e DSP](codecanddspproperties.md)
-   [Parser Sommario](toc-parser.md)
-   [Domande frequenti sui codec di Windows Media](frequentlyaskedquestions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione di Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[Tecnologie multimediali per Windows](/previous-versions/bg125389(v=msdn.10))
</dt> </dl>

 

 
