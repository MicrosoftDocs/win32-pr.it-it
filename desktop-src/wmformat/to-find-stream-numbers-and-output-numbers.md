---
title: Per trovare i numeri di flusso e i numeri di output
description: Per trovare i numeri di flusso e i numeri di output
ms.assetid: 531edd4a-a257-47cd-a367-b59cda3ea76c
keywords:
- ASF (Advanced Systems Format), numeri di flusso
- ASF (formato avanzato dei sistemi), creazione di numeri
- ASF (Advanced Systems Format), ricerca dei numeri di output
- ASF (Advanced Systems Format), ricerca dei numeri di output
- lettori sincroni, numeri di flusso
- lettori sincroni, ricerca di numeri di output
- flussi, ricerca di numeri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4bdf10eaeb95f981ab2972ba56ad09b867cd99
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723463"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a>Per trovare i numeri di flusso e i numeri di output

Il lettore sincrono supporta il cambio più semplificato tra i numeri di flusso e di output per la riproduzione rispetto al Reader asincrono. È quindi più importante riuscire a individuare i numeri di flusso che corrispondono ai numeri di output o viceversa.

Per trovare il numero di output corrispondente a un numero di flusso, chiamare [**IWMSyncReader:: GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).

Per trovare il numero di flusso che corrisponde a un numero di output, chiamare [ **IWMSyncReader:: GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Input, flussi e output**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Lettura di file con il lettore sincrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




