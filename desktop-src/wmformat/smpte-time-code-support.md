---
title: Supporto del codice ora SMPTE
description: Supporto del codice ora SMPTE
ms.assetid: 047bda0d-142d-4eed-9b59-c0c36b97ed45
keywords:
- Windows Media Format SDK, codici temporali SMPTE
- ASF (Advanced Systems Format), codici temporali SMPTE
- ASF (Advanced Systems Format), codici temporali SMPTE
- Windows Media Format SDK, interfaccia IWMReaderTimecode
- Advanced Systems Format (ASF), interfaccia IWMReaderTimecode
- ASF (formato avanzato dei sistemi), interfaccia IWMReaderTimecode
- Codici temporali SMPTE, informazioni
- IWMReaderTimecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecf8ef9da7d0fb0ee7d973cf21129f307066bc9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104516609"
---
# <a name="smpte-time-code-support"></a>Supporto del codice ora SMPTE

Windows Media Format SDK fornisce supporto limitato per il codice ora SMPTE, che è un formato di codice ora solare per i film e la televisione. È possibile includere i dati del codice ora SMPTE con esempi come estensioni di unità dati. La parte relativa ai dati dell'estensione è una struttura di [**\_ dati dell' \_ estensione \_ del codice temporale WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) contenente le informazioni del timestamp originale del SMPTE.

Il mantenimento del codice ora SMPTE nei file ASF comporta limiti di prestazioni. Ogni campione con un timestamp SMPTE associato richiede il trasporto dei 14 byte nella struttura del timestamp. In uno scenario di streaming, questo requisito di larghezza di banda maggiore potrebbe essere catastrofico. Di conseguenza, è consigliabile che i codici temporali SMPTE siano salvati in modo permanente solo nei file ASF durante il processo di modifica video, che in genere viene eseguito con i file locali. Quando viene creato il file finale, è necessario rimuovere le estensioni dell'unità dati.

È possibile leggere i timestamp SMPTE esattamente come si legge qualsiasi altra estensione di unità dati, ma gli oggetti di lettura forniscono il supporto integrato per la ricerca in base al codice ora SMPTE. Per poter cercare i timestamp SMPTE, è necessario innanzitutto indicizzare il file in base al codice ora SMPTE. È possibile configurare l'indicizzatore per indicizzare i codici temporali usando il metodo [**IWMIndexer2:: Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) .

Utilizzando il Reader asincrono, è possibile spostarsi in un file in base ai timestamp SMPTE utilizzando i metodi dell'interfaccia [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) e il metodo [**IWMReaderAdvanced3:: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) . Con il lettore sincrono, utilizzare [**IWMSyncReader2:: SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità file ASF**](asf-file-features.md)
</dt> <dt>

[**Configurazione di estensioni delle unità dati**](configuring-data-unit-extensions.md)
</dt> </dl>

 

 




