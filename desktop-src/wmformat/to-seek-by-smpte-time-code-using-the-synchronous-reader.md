---
title: Per eseguire la ricerca in base al codice temporale SMPTE usando il lettore sincrono
description: Per eseguire la ricerca in base al codice temporale SMPTE usando il lettore sincrono
ms.assetid: 1fd8885c-a694-43fd-b2a2-23eb0ae7ed72
keywords:
- Advanced Systems Format (ASF), ricerca in base ai codici ora SMPTE
- ASF (Advanced Systems Format), ricerca in base ai codici ora SMPTE
- Advanced Systems Format (ASF), lettori sincroni
- ASF (Advanced Systems Format), lettori sincroni
- Advanced Systems Format (ASF), codici ora SMPTE
- ASF (Advanced Systems Format), codici ora SMPTE
- lettori sincroni, ricerca in base ai codici ora SMPTE
- lettori sincroni,codici ora SMPTE
- codici di ora SMPTE, ricerca
- Codici di ora SMPTE, lettori sincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b368492d45d3bc564ce0fbb84a6013349c26fcdaca8c1ad576863a9cee6f6f36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196470"
---
# <a name="to-seek-by-smpte-time-code-using-the-synchronous-reader"></a>Per eseguire la ricerca in base al codice temporale SMPTE usando il lettore sincrono

L'oggetto lettore sincrono può cercare un punto in un file in base alla time code SMPTE associata a un flusso video. I dati del codice temporale vengono incapsulati in strutture DI DATI [**ESTENSIONE \_ \_ \_ TIMECODE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) collegate a campioni video come estensioni di unità dati.

I codici di ora SMPTE sono definiti da un intervallo e da time code all'interno di tale intervallo. Un intervallo è una serie continua di codici tempor numerici. Ogni time code è definita da ore, minuti, secondi e fotogrammi.

Per cercare i dati in un file ASF tramite SMPTE time code il lettore sincrono, seguire questa procedura.

1.  Impostare l'time code iniziale e time code per il recapito di esempio chiamando [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe). È necessario specificare il numero di flusso di un flusso video indicizzato time code. Il lettore sincrono sincrono sincronerà il resto degli output con l'ora di presentazione del frame specificato del flusso specificato.
2.  Iniziare a recuperare gli esempi con chiamate a [**IWMSyncReader::GetNextSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) Procedere normalmente con il lettore sincrono.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file con il lettore sincrono**](reading-files-with-the-synchronous-reader.md)
</dt> <dt>

[**Supporto del codice temporale SMPTE**](smpte-time-code-support.md)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> </dl>

 

 




