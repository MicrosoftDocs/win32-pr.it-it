---
title: Per gestire la latenza del writer
description: Per gestire la latenza del writer
ms.assetid: 62ec3f25-5cd9-499e-9579-00e00086df7f
keywords:
- Advanced Systems Format (ASF), gestione della latenza del writer
- ASF (Advanced Systems Format), gestione della latenza del writer
- Advanced Systems Format (ASF), latenza del writer
- ASF (Advanced Systems Format), latenza del writer
- latenza del writer
- latenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0adb18814cc8153ae81ed9517834d62345f18b61f51de6aacd38e9028699331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845481"
---
# <a name="to-manage-writer-latency"></a>Per gestire la latenza del writer

Il writer deve elaborare gli esempi. La quantità di tempo tra il passaggio di un esempio di input e la scrittura di un esempio di output è detta latenza del writer. Una serie di fattori contribuisce alla latenza del writer ed è possibile ridurla in diversi modi.

Il fattore più ovvio della latenza del writer è il tempo necessario per comprimere un campione. Nella maggior parte dei casi, si avrà poco o nessun controllo su questo. Se la larghezza di banda non è un problema grave, è possibile ridurre la latenza usando una compressione inferiore. Naturalmente, è possibile ottenere la latenza minima passando campioni già compressi.

Il fattore successivo, e quello su cui in genere si ha il controllo, è l'ordine in cui i campioni vengono passati al lettore. È possibile ottenere una migliore latenza passando gli esempi in ordine di tempo di presentazione e assicurando che gli esempi di input siano ben sincronizzati tra tutti i flussi di input. Maggiore è la discrepanza nei tempi di presentazione tra gli esempi per flussi diversi, maggiore sarà la latenza. È possibile impostare un valore massimo per la discrepanza tra gli esempi di input chiamando [**IWMWriterAdvanced::SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




