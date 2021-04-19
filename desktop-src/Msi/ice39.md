---
description: ICE39 convalida il flusso di informazioni di riepilogo del database.
ms.assetid: 9de72de6-fd9c-4d94-92f7-61b85dff0f6a
title: ICE39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e72e7b4a73f3a134ec108b07666cc1c4e9af23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314217"
---
# <a name="ice39"></a>ICE39

ICE39 convalida il [flusso di informazioni di riepilogo](summary-information-stream.md) del database.

ICE39 controlla il formato delle proprietà seguenti:

-   [**Riepilogo Conteggio parole**](word-count-summary.md)
-   [**Riepilogo conteggio pagine**](page-count-summary.md)
-   [**Riepilogo modelli**](template-summary.md)
-   [**Riepilogo numero revisione**](revision-number-summary.md)
-   [**Crea riepilogo Data/ora**](create-time-date-summary.md)
-   [**Ultimo riepilogo Data/ora di salvataggio**](last-saved-time-date-summary.md)
-   [**Ultimo riepilogo stampato**](last-printed-summary.md)

Se la proprietà di [**Riepilogo di Word Count**](word-count-summary.md) specifica che l'origine è compressa, ICE39 pubblica un avviso se eventuali file sono contrassegnati come compressi nella colonna attributi della [tabella file](file-table.md). Vedere [uso di cabinet e origini compresse](using-cabinets-and-compressed-sources.md).

ICE39 pubblica un avviso se la proprietà di [**Riepilogo di Word Count**](word-count-summary.md) specifica che il pacchetto è conforme a UAC e la [tabella MsiPackageCertificate](msipackagecertificate-table.md) non è vuota.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



