---
title: Per eseguire la ricerca in base al codice ora SMPTE usando il lettore sincrono
description: Per eseguire la ricerca in base al codice ora SMPTE usando il lettore sincrono
ms.assetid: 1fd8885c-a694-43fd-b2a2-23eb0ae7ed72
keywords:
- Formato di sistemi avanzati (ASF), ricerca di codici temporali SMPTE
- ASF (Advanced Systems Format), ricerca di codici temporali SMPTE
- ASF (Advanced Systems Format), lettori sincroni
- ASF (formato avanzato dei sistemi), lettori sincroni
- ASF (Advanced Systems Format), codici temporali SMPTE
- ASF (Advanced Systems Format), codici temporali SMPTE
- lettori sincroni, ricerca di codici temporali SMPTE
- lettori sincroni, codici temporali SMPTE
- Codici di ora SMPTE, ricerca
- Codici temporali SMPTE, lettori sincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c843ba802272d02f1dfc885a3c65b3d124b7423
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336401"
---
# <a name="to-seek-by-smpte-time-code-using-the-synchronous-reader"></a>Per eseguire la ricerca in base al codice ora SMPTE usando il lettore sincrono

L'oggetto Reader sincrono può eseguire ricerche in un punto in un file in base al codice ora SMPTE associato a un flusso video. I dati del codice temporale sono incapsulati nelle strutture di [**\_ dati dell' \_ estensione \_ del timecode WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) , associate a esempi video come estensioni di unità dati.

I codici temporali SMPTE sono definiti da un intervallo e da un codice temporale all'interno di tale intervallo. Un intervallo è una serie continua di codici temporali. Ogni volta che il codice viene definito da ore, minuti, secondi e frame.

Per cercare i dati in un file ASF dal codice ora SMPTE usando il lettore sincrono, seguire questa procedura.

1.  Impostare il codice ora di inizio e il codice orario di fine per il recapito di esempio chiamando [**IWMSyncReader:: SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe). È necessario specificare il numero di flusso di un flusso video indicizzato dal codice temporale. Il lettore sincrono sincronizza il resto degli output con l'ora di presentazione del frame specificato del flusso specificato.
2.  Iniziare il recupero degli esempi con le chiamate a [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Procedere normalmente con il lettore sincrono.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file con il lettore sincrono**](reading-files-with-the-synchronous-reader.md)
</dt> <dt>

[**Supporto del codice ora SMPTE**](smpte-time-code-support.md)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> </dl>

 

 




