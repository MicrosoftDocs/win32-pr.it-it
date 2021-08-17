---
title: Per cercare in base al numero di frame usando il lettore sincrono
description: Per cercare in base al numero di frame usando il lettore sincrono
ms.assetid: 755e0124-de57-4699-af8e-c594567b5523
keywords:
- Advanced Systems Format (ASF), ricerca in base ai numeri di frame
- ASF (Advanced Systems Format), ricerca in base ai numeri di frame
- Advanced Systems Format (ASF), lettori sincroni
- ASF (Advanced Systems Format), lettori sincroni
- lettori sincroni, ricerca in base ai numeri di frame
- flussi video, ricerca in base ai numeri di fotogramma
- flussi video, lettori sincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1b2da615f23e5c1d17046f08310d0aeda49200d5c4ba9fba890d7ba4951e0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699112"
---
# <a name="to-seek-by-frame-number-using-the-synchronous-reader"></a>Per cercare in base al numero di frame usando il lettore sincrono

Per cercare i dati in base al numero di fotogramma usando il lettore sincrono, è necessario specificare un intervallo per la riproduzione. Un intervallo è definito da un numero di fotogramma iniziale in un flusso video specifico e da un numero di fotogrammi da riprodurre.

Per cercare i dati in un file ASF in base al numero di frame usando il lettore sincrono, seguire questa procedura.

1.  Impostare il numero di frame iniziale e il numero di frame da leggere per il recapito di esempio chiamando [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe). È necessario specificare il numero di flusso di un flusso video indicizzato con frame. Il lettore sincronirà il resto degli output con l'ora di presentazione del frame specificato del flusso specificato e inizierà a fornire gli esempi di output.
2.  Iniziare a recuperare gli esempi con chiamate a [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Procedere come si farebbe normalmente con il lettore sincrono.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lettura di file con il lettore sincrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




