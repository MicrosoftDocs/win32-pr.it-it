---
description: Tipi di supporto
ms.assetid: 690fda6e-dcbd-44dc-968d-cc949126da81
title: Tipi di supporto (Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acbfb1b637eef6acb664d3d95a0488f155c6916
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351621"
---
# <a name="media-types-media-foundation"></a>Tipi di supporto (Media Foundation)

Un *tipo di supporto* è un modo per descrivere il formato di un flusso multimediale. In Media Foundation i tipi di supporto sono rappresentati dall'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Le applicazioni utilizzano i tipi di supporto per individuare il formato di un file multimediale o di un flusso multimediale. Gli oggetti nella pipeline Media Foundation utilizzano i tipi di supporto per negoziare i formati che verranno recapitati o ricevuti.

In questa sezione vengono trattati gli argomenti seguenti.



| Argomento                                                                    | Descrizione                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Informazioni sui tipi di supporto](about-media-types.md)                               | Panoramica generale dei tipi di supporto in Media Foundation.                             |
| [GUID di tipo multimediale](media-type-guids.md)                                 | Elenca i GUID definiti per i tipi e i sottotipi principali.                            |
| [Tipi di supporti audio](audio-media-types.md)                               | Come creare i tipi di supporto per i formati audio.                                     |
| [Tipi di supporti video](video-media-types.md)                               | Come creare i tipi di supporto per i formati video.                                     |
| [Tipi di supporti completi e parziali](complete-and-partial-media-types.md) | Descrive la differenza tra i tipi di supporto completi e i tipi di supporti parziali.   |
| [Conversioni di tipi di supporto](media-type-conversions.md)                     | Come eseguire la conversione tra Media Foundation tipi di supporto e le strutture di formato precedenti. |
| [Funzioni helper del tipo di supporto](media-type-helper-functions.md)           | Elenco di funzioni che modificano o ottengono informazioni da un tipo di supporto.        |
| [Codice di debug del tipo di supporto](media-type-debugging-code.md)               | Codice di esempio che illustra come visualizzare un tipo di supporto durante il debug.                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Primitive Media Foundation](media-foundation-primitives.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 



