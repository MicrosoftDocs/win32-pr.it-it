---
title: Per cercare in base al tempo usando il lettore sincrono
description: Per cercare in base al tempo usando il lettore sincrono
ms.assetid: 143f72b0-9d71-4efa-b8d4-5cde53a2aa2a
keywords:
- Advanced Systems Format (ASF), ricerca in base al tempo
- ASF (Advanced Systems Format), ricerca in base al tempo
- Advanced Systems Format (ASF), lettori sincroni
- ASF (Advanced Systems Format), lettori sincroni
- lettori sincroni, ricerca in base al tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74fb0cb4f73e70821347b82a9e5a2544eb9759e733fb164077b2fc007163db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118432634"
---
# <a name="to-seek-by-time-using-the-synchronous-reader"></a>Per cercare in base al tempo usando il lettore sincrono

Per cercare dati usando il lettore sincrono, è necessario specificare un intervallo per la riproduzione. Un intervallo è definito da un'ora di presentazione iniziale e una durata, entrambe in unità da 100 nanosecondi.

Per cercare i dati in un file ASF in base all'ora di presentazione usando il lettore sincrono, seguire questa procedura.

1.  Specificare un'ora di inizio e una durata per il recapito di esempio chiamando [**IWMSyncReader::SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange). Questo metodo non richiede di specificare un numero di flusso perché gli orari di presentazione di ogni flusso devono essere già sincronizzati.
2.  Iniziare a recuperare gli esempi con chiamate a [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Procedere come si farebbe normalmente con il lettore sincrono.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lettura di file con il lettore sincrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




