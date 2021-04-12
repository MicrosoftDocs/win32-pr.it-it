---
title: Per eseguire la ricerca in base al numero di frame utilizzando il lettore sincrono
description: Per eseguire la ricerca in base al numero di frame utilizzando il lettore sincrono
ms.assetid: 755e0124-de57-4699-af8e-c594567b5523
keywords:
- Formato di sistemi avanzati (ASF), ricerca per numero di frame
- ASF (Advanced Systems Format), ricerca per numero di frame
- ASF (Advanced Systems Format), lettori sincroni
- ASF (formato avanzato dei sistemi), lettori sincroni
- lettori sincroni, ricerca per numero di frame
- flussi video, ricerca per numero di frame
- flussi video, lettori sincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c26711d2d839e47279e7e52a50f5dc82c6e81da
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336321"
---
# <a name="to-seek-by-frame-number-using-the-synchronous-reader"></a>Per eseguire la ricerca in base al numero di frame utilizzando il lettore sincrono

Per cercare i dati in base al numero di frame utilizzando il lettore sincrono, è necessario specificare un intervallo per la riproduzione. Un intervallo è definito da un numero di frame iniziale in un flusso video specifico e da un numero di frame da riprodurre.

Per cercare i dati in un file ASF in base al numero di frame usando il lettore sincrono, seguire questa procedura.

1.  Impostare il numero del fotogramma iniziale e il numero di fotogrammi da leggere per il recapito di esempio chiamando [**IWMSyncReader:: SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe). È necessario specificare il numero di flusso di un flusso video indicizzato con frame. Il lettore sincronizza il resto degli output con l'ora di presentazione del frame specificato del flusso specificato e inizia a consegnare gli esempi di output.
2.  Iniziare il recupero degli esempi con le chiamate a [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Procedere normalmente con il lettore sincrono.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lettura di file con il lettore sincrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




