---
title: Per usare la selezione del flusso manuale
description: Per usare la selezione del flusso manuale
ms.assetid: 49ec283f-670a-4a0e-9477-c60a80919a1e
keywords:
- ASF (Advanced Systems Format), selezione del flusso manuale
- ASF (formato avanzato dei sistemi), selezione del flusso manuale
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- ASF (Advanced Systems Format), selezione flusso
- ASF (formato avanzato dei sistemi), selezione flusso
- Formato di sistemi avanzati (ASF), esclusione reciproca
- ASF (formato avanzato dei sistemi), esclusione reciproca
- Reader asincroni, selezione flusso manuale
- Reader asincroni, selezione flusso
- flussi, selezione manuale
- esclusione reciproca, selezione flusso manuale
- flussi, lettori asincroni
- esclusione reciproca, lettori asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87c493bc8f41bc2a03ba15832ed402939adbeff
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299424"
---
# <a name="to-use-manual-stream-selection"></a>Per usare la selezione del flusso manuale

Quando si recapitano campioni non compressi con l'oggetto Reader, è possibile recapitarli solo in base al numero di output. Nel caso di flussi che si escludono a vicenda, ciò significa che è possibile ricevere esempi solo da un flusso nell'esclusione reciproca alla volta. Il processo di scelta del flusso che si escludono reciprocamente per la distribuzione è denominato selezione dei flussi.

Per l'esclusione reciproca della velocità in bit, il lettore esegue automaticamente le selezioni del flusso in base alle condizioni nel computer host durante la riproduzione. Per altri tipi di esclusione reciproca, il lettore fornirà esempi dal flusso predefinito a meno che non si selezioni manualmente un flusso diverso. Potrebbero inoltre essere presenti istanze in cui si desidera selezionare un flusso manualmente da un'esclusione reciproca con frequenza di bit.

La selezione del flusso manuale è attiva o disattiva per l'intero file. Se un file contiene l'esclusione reciproca con velocità in bit e un altro tipo di esclusione reciproca, è necessario selezionare manualmente i flussi basati sulla velocità in bit.

Per selezionare un flusso a esclusione reciproca manualmente, è necessario eseguire i passaggi seguenti.

1.  Recuperare un puntatore all'interfaccia [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) dell'oggetto Reader chiamando **IWMReader:: QueryInterface**.
2.  Abilitare la selezione del flusso manuale chiamando [**IWMReaderAdvanced:: SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).
3.  Per sapere se è selezionato un determinato flusso, chiamare [**IWMReaderAdvanced:: GetStreamSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected). È necessario passare un puntatore a una variabile del tipo di enumerazione di [**\_ \_ selezione del flusso WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) . Quando la chiamata viene restituita, il valore nella variabile descrive il tipo di selezione corrente del flusso.
4.  Per selezionare un flusso, chiamare [**IWMReaderAdvanced:: SetStreamsSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected). Questo metodo consente di specificare più flussi contemporaneamente per il cambio di flusso sincronizzato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




