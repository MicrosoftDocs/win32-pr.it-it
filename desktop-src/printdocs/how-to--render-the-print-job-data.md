---
description: Questo argomento descrive come eseguire il rendering dei dati del programma da stampare.
ms.assetid: D1343C53-6F13-49FF-8C7C-25D5A3C31B22
title: 'Procedura: Eseguire il rendering dei dati del processo di stampa'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70724cc9dee6b7d3bb0434f08e3db959acfecfc54bc4ebafac5f5a3c6bd4b014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825131"
---
# <a name="how-to-render-print-job-data"></a>Procedura: Eseguire il rendering dei dati del processo di stampa

Questo argomento descrive come eseguire il rendering dei dati del programma da stampare. Questo argomento non illustra in dettaglio come eseguire il rendering di immagini grafiche o di testo specifiche. Descrive invece come gestire i dati del programma ed eseguirne il rendering come documento XPS, inviato a una stampante tramite [l'API di stampa XPS](xps-printing.md).

## <a name="overview"></a>Panoramica

Il rendering dei dati del processo di stampa per la stampa comporta l'uso dei dati specifici del programma, ad esempio testo, immagini e formattazione, e la conversione dei dati in un formato compatibile con la stampante di destinazione. Il programma che invia i dati alla stampante deve inviarli nel formato richiesto dal driver della stampante.

Usare [l'API di](xps-printing.md) stampa XPS per inviare i dati alla stampante e richiede che i dati siano formattati come documento XPS. Per produrre il contenuto del documento XPS necessario all'API di stampa XPS, il programma di esempio usa [l'API documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).

Se il contenuto del programma è in un formato non compatibile con una stampante, sarà necessario eseguire il rendering prima di essere inviato alla stampante. Se il programma usa [l'API XpS Document](/previous-versions/windows/desktop/dd316976(v=vs.85)) per gestire il contenuto del programma, il contenuto del programma sarà in un formato che può essere inviato direttamente all'API di stampa [XPS](xps-printing.md) e non richiederà alcun rendering aggiuntivo prima di inviarlo alla stampante.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[API di stampa XPS](xps-printing.md)
</dt> </dl>

 

 
