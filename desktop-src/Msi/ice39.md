---
description: ICE39 convalida il flusso di informazioni di riepilogo del database.
ms.assetid: 9de72de6-fd9c-4d94-92f7-61b85dff0f6a
title: ICE39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb912afbe7220eee1aa3bbcd494f6531736279b85c5736f6867fdf8779e39bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528441"
---
# <a name="ice39"></a>ICE39

ICE39 convalida il [flusso di informazioni di](summary-information-stream.md) riepilogo del database.

ICE39 controlla il formato delle proprietà seguenti:

-   [**Riepilogo conteggio parole**](word-count-summary.md)
-   [**Riepilogo conteggio pagine**](page-count-summary.md)
-   [**Riepilogo dei modelli**](template-summary.md)
-   [**Riepilogo del numero di revisione**](revision-number-summary.md)
-   [**Creare un riepilogo di data/ora**](create-time-date-summary.md)
-   [**Riepilogo data/ora ultimo salvataggio**](last-saved-time-date-summary.md)
-   [**Riepilogo ultima stampa**](last-printed-summary.md)

Se la [**proprietà Riepilogo**](word-count-summary.md) conteggio parole specifica che l'origine è compressa, ICE39 invia un avviso se anche i file sono contrassegnati come compressi nella colonna Attributi della [tabella File](file-table.md). Vedere [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).

ICE39 invia un avviso se la [**proprietà Riepilogo**](word-count-summary.md) conteggio parole specifica che il pacchetto è conforme a Controllo dell'account utente e la tabella [MsiPackageCertificate](msipackagecertificate-table.md) non è vuota.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



