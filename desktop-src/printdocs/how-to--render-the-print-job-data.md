---
description: In questo argomento viene descritto come eseguire il rendering dei dati del programma da stampare.
ms.assetid: D1343C53-6F13-49FF-8C7C-25D5A3C31B22
title: 'Procedura: eseguire il rendering dei dati del processo di stampa'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2d9f8cbf68394fd56ebcf31cfb37ee8f337f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885177"
---
# <a name="how-to-render-print-job-data"></a>Procedura: eseguire il rendering dei dati del processo di stampa

In questo argomento viene descritto come eseguire il rendering dei dati del programma da stampare. In questo argomento non viene illustrato in dettaglio come eseguire il rendering di immagini grafiche o di testo specifiche. Viene invece descritto come gestire i dati di programma ed eseguirne il rendering come documento XPS, che viene inviato a una stampante tramite l' [API di stampa XPS](xps-printing.md).

## <a name="overview"></a>Panoramica

Il rendering dei dati dei processi di stampa per la stampa comporta l'esecuzione di dati specifici del programma, ad esempio testo, immagini e formattazione, e la relativa conversione in un formato compatibile con la stampante di destinazione. Il programma che invia i dati alla stampante deve inviarlo nel formato richiesto dal driver della stampante.

Utilizzare l' [API di stampa XPS](xps-printing.md) per inviare i dati alla stampante ed è necessario che i dati vengano formattati come documento XPS. Per produrre il contenuto del documento XPS necessario per l'API di stampa XPS, il programma di esempio utilizza l' [API del documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).

Se il contenuto del programma è in un formato non compatibile con una stampante, sarà necessario eseguirne il rendering prima di inviarlo alla stampante. Se il programma utilizza l' [API documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) per gestire il contenuto del programma, il contenuto del programma sarà in un formato che può essere inviato direttamente all' [API di stampa XPS](xps-printing.md) e non sarà necessario alcun rendering aggiuntivo prima di inviarlo alla stampante.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API documenti XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[API di stampa XPS](xps-printing.md)
</dt> </dl>

 

 
