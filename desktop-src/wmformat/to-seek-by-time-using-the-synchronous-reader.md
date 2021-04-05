---
title: Per eseguire ricerche in base al tempo tramite il lettore sincrono
description: Per eseguire ricerche in base al tempo tramite il lettore sincrono
ms.assetid: 143f72b0-9d71-4efa-b8d4-5cde53a2aa2a
keywords:
- Formato Advanced Systems (ASF), ricerca per ora
- ASF (Advanced Systems Format), ricerca per ora
- ASF (Advanced Systems Format), lettori sincroni
- ASF (formato avanzato dei sistemi), lettori sincroni
- lettori sincroni, ricerca per ora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a43e914a6fc0d320860db61f4747cbee3033e9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723559"
---
# <a name="to-seek-by-time-using-the-synchronous-reader"></a>Per eseguire ricerche in base al tempo tramite il lettore sincrono

Per cercare i dati utilizzando il lettore sincrono, è necessario specificare un intervallo per la riproduzione. Un intervallo è definito da un'ora di presentazione iniziale e da una durata, entrambe in unità di 100 nanosecondi.

Per cercare i dati in un file ASF in base all'ora di presentazione usando il lettore sincrono, seguire questa procedura.

1.  Specificare l'ora di inizio e la durata per il recapito di esempio chiamando [**IWMSyncReader:: SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange). Questo metodo non richiede di specificare un numero di flusso perché le ore di presentazione di ogni flusso devono essere già sincronizzate.
2.  Iniziare il recupero degli esempi con le chiamate a [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Procedere normalmente con il lettore sincrono.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lettura di file con il lettore sincrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




