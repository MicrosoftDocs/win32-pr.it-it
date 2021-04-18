---
title: Per gestire la latenza del writer
description: Per gestire la latenza del writer
ms.assetid: 62ec3f25-5cd9-499e-9579-00e00086df7f
keywords:
- Formato di sistemi avanzati (ASF), gestione della latenza del writer
- ASF (formato di sistemi avanzati), gestione della latenza del writer
- ASF (Advanced Systems Format), latenza writer
- ASF (formato avanzato dei sistemi), latenza writer
- latenza writer
- latenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3260be03344f1bf13252007b10614746ceda3e96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299398"
---
# <a name="to-manage-writer-latency"></a>Per gestire la latenza del writer

Per elaborare gli esempi, il writer richiede tempo. La quantità di tempo che intercorre tra il passaggio di un campione di input e la scrittura di un campione di output è detta latenza del writer. Una serie di fattori contribuisce alla latenza del writer ed è possibile ridurla in diversi modi.

Il fattore più ovvio implicato nella latenza del writer è il tempo necessario per comprimere un campione. Nella maggior parte dei casi, l'utente non avrà alcun controllo sufficiente. Se la larghezza di banda non costituisce un problema, è possibile ridurre la latenza utilizzando una minore compressione. Naturalmente, è possibile ottenere la latenza minima passando esempi già compressi.

Il fattore successivo, e uno su cui si ha in genere il controllo, è l'ordine in cui gli esempi vengono passati al lettore. È possibile ottenere una latenza migliore passando esempi in ordine di tempo di presentazione e assicurandosi che gli esempi di input siano sincronizzati correttamente tra tutti i flussi di input. Maggiore è la discrepanza nei tempi di presentazione tra gli esempi per flussi diversi, maggiore sarà il risultato della latenza. È possibile impostare un massimo per la discrepanza tra gli esempi di input chiamando [**IWMWriterAdvanced:: SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




