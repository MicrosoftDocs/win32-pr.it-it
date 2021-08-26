---
title: Supporto del codice temporale SMPTE
description: Supporto del codice temporale SMPTE
ms.assetid: 047bda0d-142d-4eed-9b59-c0c36b97ed45
keywords:
- Windows MEDIA Format SDK, codici ora SMPTE
- Advanced Systems Format (ASF), codici ora SMPTE
- ASF (Advanced Systems Format), codici ora SMPTE
- Windows Media Format SDK, interfaccia IWMReaderTimecode
- Advanced Systems Format (ASF), interfaccia IWMReaderTimecode
- ASF (Advanced Systems Format),interfaccia IWMReaderTimecode
- codici di ora SMPTE, informazioni
- IWMReaderTimecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19e3d7a85c797a3b0247bedb2359b4b40b60e8d4f243f14e2c94175bb1e2740
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929611"
---
# <a name="smpte-time-code-support"></a>Supporto del codice temporale SMPTE

L Windows Media Format SDK offre un supporto limitato per SMPTE time code, un formato time code standard per film e tv. È possibile includere dati di time code SMPTE con esempi come estensioni di unità dati. La parte relativa ai dati dell'estensione è una struttura [**WMT \_ TIMECODE \_ EXTENSION \_ DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) contenente le informazioni del timestamp SMPTE originale.

La gestione delle time code SMPTE nei file ASF presenta limiti di prestazioni. Ogni esempio con un timestamp SMPTE associato richiede il trasporto dei 14 byte nella struttura del timestamp. In uno scenario di streaming, questo requisito di aumento della larghezza di banda potrebbe essere irreversico. Di conseguenza, è consigliabile che i codici temporizzazione SMPTE siano persistenti solo nei file ASF durante il processo di modifica video, che in genere viene eseguito con i file locali. Quando viene creato il file finale, è necessario rimuovere le estensioni delle unità dati.

È possibile leggere i timestamp SMPTE esattamente come si legge qualsiasi altra estensione di unità dati, ma gli oggetti di lettura forniscono supporto integrato per la ricerca tramite SMPTE time code. Per poter cercare timestamp SMPTE, è prima necessario indicizzare il file in base a SMPTE time code. È possibile configurare l'indicizzatore per indicizzare i codici temporizzazione usando il [**metodo IWMIndexer2::Configure.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)

Usando il lettore asincrono, è possibile esplorare un file tramite timestamp SMPTE usando i metodi [**dell'interfaccia IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) e del metodo [**IWMReaderAdvanced3::StartAtPosition.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) Con il lettore sincrono, usare [**IWMSyncReader2::SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità dei file ASF**](asf-file-features.md)
</dt> <dt>

[**Configurazione di estensioni delle unità dati**](configuring-data-unit-extensions.md)
</dt> </dl>

 

 




