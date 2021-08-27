---
title: Per eseguire la ricerca tramite codice temporale SMPTE usando il lettore asincrono
description: Per eseguire la ricerca tramite codice temporale SMPTE usando il lettore asincrono
ms.assetid: 5c618f04-3761-418c-b75a-70c7bf7fa5be
keywords:
- Advanced Systems Format (ASF), ricerca da parte dei codici di tempo SMPTE
- ASF (Advanced Systems Format), ricerca da parte dei codici ora SMPTE
- Advanced Systems Format (ASF), lettori asincroni
- ASF (Advanced Systems Format), lettori asincroni
- Advanced Systems Format (ASF), codici di ora SMPTE
- ASF (Advanced Systems Format), codici di ora SMPTE
- lettori asincroni, ricerca da codici temporità SMPTE
- lettori asincroni, codici di ora SMPTE
- codici di tempo SMPTE, ricerca
- Codici di ora SMPTE, lettori asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01ad42170c2458a4dc23a23cfa8102b406f45b6a624cacac28ce31a905ad299
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110121"
---
# <a name="to-seek-by-smpte-time-code-using-the-asynchronous-reader"></a>Per eseguire la ricerca tramite codice temporale SMPTE usando il lettore asincrono

L'oggetto lettore può cercare un punto in un file in base alla time code SMPTE associata a un flusso video. I dati del codice temporale sono incapsulati in strutture DI ESTENSIONE [**\_ \_ TIMECODE \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) collegate agli esempi video come estensioni di unità dati.

I codici di ora SMPTE sono definiti da un intervallo e da un time code all'interno di tale intervallo. Un intervallo è una serie continua di codici tempo. Ogni time code è definita da ore, minuti, secondi e fotogrammi.

Per cercare dati in un file ASF da parte di SMPTE time code il lettore asincrono, seguire questa procedura.

1.  Ottenere un puntatore [**all'interfaccia IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) dell'oggetto reader chiamando **IWMReader::QueryInterface**.
2.  Impostare il valore time code e la durata chiamando [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition). È necessario specificare il numero di flusso di un flusso video indicizzato da time code. Il lettore sincronirà il resto degli output con l'ora di presentazione del frame specificato del flusso specificato e inizierà a fornire gli esempi di output.
3.  Gestire gli esempi come si farebbe normalmente nell'implementazione del **metodo IWMReaderCallback::OnSample.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> <dt>

[**Supporto del codice temporale SMPTE**](smpte-time-code-support.md)
</dt> </dl>

 

 




