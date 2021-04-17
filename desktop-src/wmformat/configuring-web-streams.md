---
title: Configurazione di flussi Web
description: Configurazione di flussi Web
ms.assetid: 1eeb6243-5095-4dba-994c-2083beda7b78
keywords:
- flussi, configurazione di flussi Web
- codec, configurazione di flussi Web
- Flussi Web, configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c91c36788b858b2378ebf46b553f076c5ec490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331943"
---
# <a name="configuring-web-streams"></a>Configurazione di flussi Web

I flussi Web sono un tipo specializzato di flusso di trasferimento di file usato per recapitare i file associati a un sito Web in un singolo flusso. La configurazione del flusso Web è riepilogata nella tabella seguente.



| Impostazione                                            | Descrizione                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| **\_Tipo di supporto WM \_ . majortype**                      | Impostare su WMMEDIATYPE \_ filetransfer.                                                 |
| **\_Tipo di supporto WM \_ . sottotipo**                        | Impostare su WMMEDIASUBTYPE \_ webstream.                                                 |
| **\_Tipo di supporto WM \_ . bFixedSizeSamples**              | Impostare su false.                                                                     |
| **\_Tipo di supporto WM \_ . bTemporalCompression**           | Impostare su true.                                                                      |
| **\_Tipo di supporto WM \_ . lSampleSize**                    | Impostare su 0.                                                                         |
| **\_Tipo di supporto WM \_ . formatType**                     | Impostare su WMFORMAT \_ webstream.                                                       |
| **\_Tipo di supporto WM \_ . punk**                           | Impostare su **null**.                                                                  |
| **\_Tipo di supporto WM \_ . cbFormat**                       | Impostare su `sizeof(WMT_WEBSTREAM_FORMAT)`.                                            |
| **\_Tipo di supporto WM \_ . pbFormat**                       | Impostare sull'indirizzo di una struttura del **\_ \_ formato webstream WMT** correttamente configurata. |
| **\_Formato WEBSTREAM WMT \_ . cbSampleHeaderFixedData** | Impostare su `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`.                                     |
| **\_Formato WEBSTREAM WMT \_ . wVersion**                | impostare su 1.                                                                         |
| **\_Formato WEBSTREAM WMT \_ . wReserved**               | Impostare su 0.                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione comune a tutti i flussi**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurazione di tipi di flusso arbitrari**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Flussi Web**](web-streams.md)
</dt> </dl>

 

 




