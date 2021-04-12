---
title: Per eseguire la ricerca in base al codice ora SMPTE usando il Reader asincrono
description: Per eseguire la ricerca in base al codice ora SMPTE usando il Reader asincrono
ms.assetid: 5c618f04-3761-418c-b75a-70c7bf7fa5be
keywords:
- Formato di sistemi avanzati (ASF), ricerca di codici temporali SMPTE
- ASF (Advanced Systems Format), ricerca di codici temporali SMPTE
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- ASF (Advanced Systems Format), codici temporali SMPTE
- ASF (Advanced Systems Format), codici temporali SMPTE
- lettori asincroni, ricerca di codici temporali SMPTE
- Reader asincroni, codici temporali SMPTE
- Codici di ora SMPTE, ricerca
- Codici temporali SMPTE, lettori asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bb90e899db9820ccbd14e42b9699a5f99c7434
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398544"
---
# <a name="to-seek-by-smpte-time-code-using-the-asynchronous-reader"></a>Per eseguire la ricerca in base al codice ora SMPTE usando il Reader asincrono

L'oggetto Reader può eseguire ricerche in un punto in un file in base al codice ora SMPTE associato a un flusso video. I dati del codice temporale sono incapsulati nelle strutture di [**\_ dati dell' \_ estensione \_ del timecode WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) , associate a esempi video come estensioni di unità dati.

I codici temporali SMPTE sono definiti da un intervallo e da un codice temporale all'interno di tale intervallo. Un intervallo è una serie continua di codici temporali. Ogni volta che il codice viene definito da ore, minuti, secondi e frame.

Per cercare i dati in un file ASF dal codice ora SMPTE usando il Reader asincrono, seguire questa procedura.

1.  Ottenere un puntatore all'interfaccia [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) dell'oggetto Reader chiamando **IWMReader:: QueryInterface**.
2.  Impostare il codice dell'ora di inizio e la durata chiamando [**IWMReaderAdvanced3:: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition). È necessario specificare il numero di flusso di un flusso video indicizzato dal codice temporale. Il lettore sincronizza il resto degli output con l'ora di presentazione del frame specificato del flusso specificato e inizia a consegnare gli esempi di output.
3.  Gestire gli esempi normalmente nell'implementazione del metodo **IWMReaderCallback:: OnSample** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> <dt>

[**Supporto del codice ora SMPTE**](smpte-time-code-support.md)
</dt> </dl>

 

 




