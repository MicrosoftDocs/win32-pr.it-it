---
title: Per trovare i numeri di flusso e i numeri di output
description: Per trovare i numeri di flusso e i numeri di output
ms.assetid: 531edd4a-a257-47cd-a367-b59cda3ea76c
keywords:
- Advanced Systems Format (ASF), numeri di flusso
- ASF (Advanced Systems Format), creazione di numeri
- Advanced Systems Format (ASF), ricerca dei numeri di output
- ASF (Advanced Systems Format), ricerca dei numeri di output
- lettori sincroni, numeri di flusso
- lettori sincroni,ricerca di numeri di output
- flussi,ricerca di numeri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4349bc98214d61a1529fe4a64dd142a9695d909f9e2a650162a8e4f8ac618177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699589"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a>Per trovare i numeri di flusso e i numeri di output

Il lettore sincrono supporta il passaggio più semplificato tra i numeri di flusso e di output per la riproduzione rispetto al lettore asincrono. È quindi più importante trovare i numeri di flusso che equidono ai numeri di output o al contrario.

Per trovare il numero di output corrispondente a un numero di flusso, chiamare [**IWMSyncReader::GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).

Per trovare il numero di flusso corrispondente a un numero di output, chiamare [ **IWMSyncReader::GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Input, Flussi e output**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Lettura di file con il lettore sincrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




