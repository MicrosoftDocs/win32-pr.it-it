---
title: Configurazione dei Flussi
description: Configurazione dei Flussi
ms.assetid: 1eeb6243-5095-4dba-994c-2083beda7b78
keywords:
- flussi, configurazione di flussi Web
- codec, configurazione di flussi Web
- flussi Web, configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8df1ced96a772a26b674fb47a30a8664d6431ff946328f45467554857b1ee4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199122"
---
# <a name="configuring-web-streams"></a>Configurazione dei Flussi

I flussi Web sono un tipo specializzato di flusso di trasferimento file usato per recapitare i file associati a un sito Web in un unico flusso. La configurazione del flusso Web è riepilogata nella tabella seguente.



| Impostazione                                            | Descrizione                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| **WM \_ MEDIA \_ TYPE.majortype**                      | Impostare su WMMEDIATYPE \_ FileTransfer.                                                 |
| **WM \_ MEDIA \_ TYPE.subtype**                        | Impostare su WMMEDIASUBTYPE \_ WebStream.                                                 |
| **WM \_ MEDIA \_ TYPE.bFixedSizeSamples**              | Impostare su False.                                                                     |
| **WM \_ MEDIA \_ TYPE.bTemporalCompression**           | Impostare su True.                                                                      |
| **WM \_ MEDIA \_ TYPE.lSampleSize**                    | Impostare su 0.                                                                         |
| **WM \_ MEDIA \_ TYPE.formattype**                     | Impostare su WMFORMAT \_ WebStream.                                                       |
| **WM \_ MEDIA \_ TYPE.pUnk**                           | Impostare su **NULL.**                                                                  |
| **WM \_ MEDIA \_ TYPE.cbFormat**                       | Impostare su `sizeof(WMT_WEBSTREAM_FORMAT)`.                                            |
| **WM \_ MEDIA \_ TYPE.pbFormat**                       | Impostare sull'indirizzo di una struttura **WMT \_ WEBSTREAM \_ FORMAT** configurata correttamente. |
| **WMT \_ WEBSTREAM \_ FORMAT.cbSampleHeaderFixedData** | Impostare su `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`.                                     |
| **WMT \_ WEBSTREAM \_ FORMAT.wVersion**                | impostare su 1.                                                                         |
| **WMT \_ WEBSTREAM \_ FORMAT.wreserved**               | Impostare su 0.                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione comune a tutti Flussi**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurazione di tipi di flusso arbitrari**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Web Flussi**](web-streams.md)
</dt> </dl>

 

 




