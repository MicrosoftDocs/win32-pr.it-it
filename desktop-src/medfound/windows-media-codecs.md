---
description: I Windows codec Audio e Video multimediali sono una raccolta di oggetti che è possibile usare per comprimere e decomprimere i dati multimediali digitali.
ms.assetid: 74de2e75-b1ee-436d-8d78-efe366ab7aa6
title: Codec Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 863bb21e17200016317ce273ecb8e2493b9d6bea7d19f92f3f397fb61b88eba4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972530"
---
# <a name="windows-media-codecs"></a>Codec Windows Media

I Windows codec Audio e Video multimediali sono una raccolta di oggetti che è possibile usare per comprimere e decomprimere i dati multimediali digitali. Ogni codec è costituito da due oggetti, un codificatore e un decodificatore. Questa parte della documentazione descrive come usare le funzionalità dei codec audio e video di Windows per produrre e utilizzare flussi di dati compressi.

> [!Note]  
> Questa documentazione è destinata principalmente agli sviluppatori che vogliono usare Windows codec multimediali nelle applicazioni multimediali basate su C++. Per una panoramica tecnica delle funzionalità dei codec multimediali Windows, vedere [About the Windows Media Codecs](about-the-windows-media-codecs.md)(Informazioni sui codec multimediali di Windows).

 

Il termine *codec* è un'affollamento dei termini termini termini e decompressore. Un codec viene in genere implementato come coppia di oggetti COM: uno per la codifica del contenuto e un altro per la decodifica del contenuto. In alcuni casi gli oggetti COM occupano la stessa libreria collegata dinamicamente (DLL).

Ogni oggetto codec implementa due interfacce separate ma simili:



| Interfaccia                              | Descrizione                                 |
|----------------------------------------|---------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Compatibile con Microsoft Media Foundation. |
| [**Oggetto IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Compatibile con DirectShow.                 |



 

Non solo sono disponibili codec diversi per audio e video, ma anche codec diversi per diversi tipi di contenuto che è possibile inserire in un file audio o video. Gli algoritmi usati per comprimere e decomprimere i dati per le parole pronunciate sono diversi dagli algoritmi usati per comprimere e decomprimere i dati musicali.

## <a name="codec-descriptions"></a>Descrizioni dei codec

Nella tabella seguente vengono descritti gli utilizzi di Windows codec multimediali.



| Codec                                                                     | Descrizione                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Media Audio](windowsmediaaudioencoder.md)                       | Codec audio che supporta tre categorie di contenuto codificato: Standard, Professional e Lossless.                                                                                                                                                                                      |
| [Windows Voce audio multimediale](windowsmediaaudiovoiceencoder.md)            | Codec audio ottimizzato per la codifica della voce umana con rapporti di compressione elevati. Si tratta del codec preferito per i flussi costituiti principalmente da parole pronunciate. Per contenuti con musica mista e voce, questo codec può modificare dinamicamente l'algoritmo di codifica usato per ottenere una qualità ottimale. |
| [Windows Video multimediale 9](windowsmediavideo9encoder.md)                    | Codec video che supporta quattro categorie di contenuto codificato: Profilo semplice, Profilo principale, Profilo avanzato e Immagine.                                                                                                                                                                  |
| [Windows Schermata Media Video 9](usingthewindowsmediavideo9screencodec.md) | Codec video ottimizzato per la codifica di schermate sequenziali dai monitor del computer. Questo codec viene spesso usato per il training del software o per il supporto tramite la registrazione di immagini di monitoraggio durante l'uso di applicazioni per computer.                                                                         |



 

Le versioni più recenti degli oggetti codec consentono anche l'accesso ad alcuni codec legacy, tra cui Windows Media Video 7 e 8, Windows Media Screen 7, i codec Microsoft MPEG-4 meno recenti e i codec MICROSOFT ISO MPEG-4.

> [!Note]  
> Questa documentazione non tratta questi codec legacy. vengono illustrate solo le versioni correnti dei codec.

 

Per i codec meno recenti, usare le stesse procedure usate quando si usano i codec correnti. Tuttavia, tenere presente che non tutte le funzionalità sono supportate in tutti i codec.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Informazioni sui Windows media codec](about-the-windows-media-codecs.md)
-   [Uso degli oggetti Codec e DSP](decidinghowtousethewindowsmediaaudioandvideocodecs.md)
-   [Metodi di codifica](encodingmethods.md)
-   [Implementazione di codec](codecimplementation.md)
-   [Modello di buffer del bucket di perdita](the-leaky-bucket-buffer-model.md)
-   [Uso degli oggetti DMO codec](workingwithcodecdmos.md)
-   [Uso dei codec MFT](workingwithcodecmfts.md)
-   [Uso dell'audio](workingwithaudio.md)
-   [Uso dei video](workingwithvideo.md)
-   [Archiviazione di supporti compressi in file AVI](storingcompressedmediainavifiles.md)
-   [Uso della codifica VBR](usingvbrencoding.md)
-   [Uso Two-Pass codifica](usingtwoencodingpasses.md)
-   [Recupero delle statistiche di codifica](gettingencodingstatistics.md)
-   [Uso delle estensioni per unità dati](usingdataunitextensions.md)
-   [Costanti IPropertyBag codec e DSP](codecanddspproperties.md)
-   [Parser sommario](toc-parser.md)
-   [Windows Domande frequenti sui codec multimediali](frequentlyaskedquestions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation di programmazione](media-foundation-programming-guide.md)
</dt> <dt>

[Tecnologie multimediali per Windows](/previous-versions/bg125389(v=msdn.10))
</dt> </dl>

 

 
