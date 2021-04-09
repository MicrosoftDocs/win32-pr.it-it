---
title: Per recuperare esempi di flusso con il lettore sincrono
description: Per recuperare esempi di flusso con il lettore sincrono
ms.assetid: d5cc4bb7-5fcf-4e1e-80dc-f03feed4dc8a
keywords:
- Formato avanzato dei sistemi (ASF), recupero degli esempi di flusso
- ASF (formato avanzato dei sistemi), recupero di esempi di flusso
- ASF (Advanced Systems Format), lettori sincroni
- ASF (formato avanzato dei sistemi), lettori sincroni
- lettori sincroni, recupero di esempi di flusso
- flussi, recupero di esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fd641dc08387606d1fdf04602e46cb9e9cbc2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117363"
---
# <a name="to-retrieve-stream-samples-with-the-synchronous-reader"></a>Per recuperare esempi di flusso con il lettore sincrono

Come il Reader asincrono, il lettore sincrono può recuperare esempi per numero di flusso. Diversamente dal reader asincrono, il lettore sincrono può recapitare esempi di flusso compressi o decompressi.

Per ricevere gli esempi di flusso, seguire questa procedura.

1.  In qualsiasi momento prima o durante la riproduzione, chiamare [**IWMSyncReader:: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) passando il numero di flusso desiderato.
2.  Recuperare gli esempi con chiamate continue a [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).

È possibile verificare se un flusso è selezionato per il recapito di esempio chiamando [**IWMSyncReader:: GetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lettura di file con il lettore sincrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




