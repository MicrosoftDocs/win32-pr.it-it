---
title: Tipi di supporti per Windows Media Format SDK
description: Informazioni sui tipi di supporti che possono essere usati da Windows Media Format SDK. I tipi di supporto sono valori GUID assegnati alle costanti nell'SDK.
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- Windows MEDIA Format SDK, tipi di supporti
- Advanced Systems Format (ASF), tipi di supporti
- ASF (Advanced Systems Format), tipi di supporti
- tipi di supporti, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84974391a7e044367fd298598181d43447cfac4bec1829b9e5ddb0b90ae27ea4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027489"
---
# <a name="media-types-for-windows-media-format-sdk"></a>Tipi di supporti per Windows Media Format SDK

I tipi di supporti identificano i diversi tipi di supporti che possono essere usati da Windows Media Format SDK. Tutti i tipi di supporti sono valori GUID assegnati alle costanti nell'SDK. I valori GUID rappresentati dalle costanti elencate in questa sezione sono elencati nella sezione [Identificatori](media-type-identifiers.md) dei tipi di supporto di questo riferimento.

Nella tabella seguente sono elencati i tipi di supporti principali. Queste costanti definiscono la classificazione generale dei supporti digitali supportati da Windows Media Format SDK.



| Tipo principale                | Descrizione                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| WMMEDIATYPE \_ Video        | Flusso video.                                                                                         |
| WMMEDIATYPE \_ Audio        | Flusso audio.                                                                                        |
| WMMEDIATYPE \_ Script       | Flusso di script.                                                                                        |
| File \_ WMMEDIATYPETransfer | Flusso che contiene file di dati. Anche i flussi Web, costituiti da file HTML, hanno questo tipo principale. |
| Immagine \_ WMMEDIATYPE        | Flusso di immagini JPEG per un file audio illustrato (come in una presentazione).                                 |
| Testo \_ WMMEDIATYPE         | Flusso di testo.                                                                                          |



 

Oltre ai tipi di supporti principali supportati in modo esplicito, è possibile creare tipi di dati arbitrari personalizzati. Per i tipi di dati arbitrari personalizzati, è necessario assicurarsi che il GUID in uso non corrisponda a un tipo principale esistente.

Un flusso multimediale spesso avrà un sottotipo oltre al tipo principale. Le sezioni seguenti elencano i sottotipi supportati.



| Sezione                                                        | Descrizione                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Sottotipi di supporti non compressi](uncompressed-media-subtypes.md) | Descrive i sottotipi disponibili per i supporti non compressi. Si tratta dei tipi in genere associati ai supporti di input o di output.              |
| [Sottotipi di supporti compressi](compressed-media-subtypes.md)     | Descrive i sottotipi disponibili per i supporti compressi. Si tratta dei tipi in genere associati ai supporti in un flusso all'interno di un file ASF. |
| [Formati di input video](video-input-formats.md)                 | Elenca i formati video accettati come input per il codec Windows Media Video 9.                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Identificatori dei tipi di supporti**](media-type-identifiers.md)
</dt> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 




