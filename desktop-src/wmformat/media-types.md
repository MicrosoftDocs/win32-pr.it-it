---
title: Tipi di supporto per Windows Media Format SDK
description: Informazioni sui tipi di supporto che possono essere usati da Windows Media Format SDK. I tipi di supporto sono valori GUID assegnati alle costanti nell'SDK.
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- Windows Media Format SDK, tipi di supporto
- Formati di sistemi avanzati (ASF), tipi di supporto
- ASF (formato di sistemi avanzati), tipi di supporto
- tipi di supporto, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6d15255ab311c67562a6c9dde83650240b0803
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334336"
---
# <a name="media-types-for-windows-media-format-sdk"></a>Tipi di supporto per Windows Media Format SDK

I tipi di supporto identificano i diversi tipi di supporti che possono essere usati da Windows Media Format SDK. Tutti i tipi di supporto sono valori GUID che sono stati assegnati alle costanti nell'SDK. I valori GUID rappresentati dalle costanti elencate in questa sezione sono elencati nella sezione [identificatori del tipo di supporto](media-type-identifiers.md) di questo riferimento.

La tabella seguente elenca i principali tipi di supporti. Queste costanti definiscono la classificazione di alto livello del supporto digitale supportato da Windows Media Format SDK.



| Tipo principale                | Descrizione                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| Video di WMMEDIATYPE \_        | Flusso video.                                                                                         |
| \_Audio WMMEDIATYPE        | Flusso audio.                                                                                        |
| \_Script WMMEDIATYPE       | Flusso di script.                                                                                        |
| WMMEDIATYPE \_ filetransfer | Flusso contenente file di dati. I flussi Web, che sono costituiti da file HTML, hanno anche questo tipo principale. |
| Immagine di WMMEDIATYPE \_        | Un flusso di immagini JPEG per un file audio illustrato (come in una presentazione).                                 |
| \_Testo WMMEDIATYPE         | Flusso di testo.                                                                                          |



 

Oltre ai tipi di supporti principali supportati in modo esplicito, è possibile creare tipi di dati arbitrari. Per i tipi di dati arbitrari personalizzati, è necessario assicurarsi che il GUID utilizzato non corrisponda a un tipo principale esistente.

Un flusso multimediale avrà spesso un sottotipo oltre al tipo principale. Nelle sezioni seguenti sono elencati i sottotipi supportati.



| Sezione                                                        | Descrizione                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Sottotipi di supporti non compressi](uncompressed-media-subtypes.md) | Descrive i sottotipi disponibili per i supporti non compressi. Questi sono i tipi generalmente associati al supporto di input o di output.              |
| [Sottotipi di supporti compressi](compressed-media-subtypes.md)     | Descrive i sottotipi disponibili per i supporti compressi. Questi sono i tipi in genere associati ai supporti in un flusso all'interno di un file ASF. |
| [Formati di input video](video-input-formats.md)                 | Elenca i formati video accettati come input per il codec Windows Media Video 9.                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Identificatori del tipo di supporto**](media-type-identifiers.md)
</dt> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 




