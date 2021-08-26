---
description: Se l'opzione di elaborazione di restituzione msidbCustomActionTypeContinue non è impostata, l'azione personalizzata deve restituire un codice di stato intero, come illustrato nella tabella seguente.
ms.assetid: 56c2d639-eef8-47cd-9d47-9a4781b9be36
title: Valori restituiti dell'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3853cfeafba22cb2d479feb1e699c29bcf4b0ab7a08402245f30958cb593df6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045001"
---
# <a name="custom-action-return-values"></a>Valori restituiti dell'azione personalizzata

Se l'opzione di elaborazione di restituzione **msidbCustomActionTypeContinue** non è impostata, l'azione personalizzata deve restituire un codice di stato intero, come illustrato nella tabella seguente.



| Valore restituito                 | Descrizione                           |
|------------------------------|---------------------------------------|
| FUNZIONE \_ ERROR \_ NON \_ CHIAMATA | Azione non eseguita.                  |
| ERRORE \_ RIUSCITO               | Azioni completate correttamente.       |
| ERRORE \_ DURANTE \_ L'INSTALLAZIONE DI USEREXIT     | L'utente è stato terminato in modo prematuro.          |
| ERRORE DURANTE \_ \_ L'INSTALLAZIONE      | Si è verificato un errore irreversibile.         |
| ERRORE \_ NESSUN \_ ALTRO \_ ELEMENTO       | Ignorare le azioni rimanenti, non un errore. |



 

Si noti che le azioni personalizzate che sono [file eseguibili](executable-files.md) devono restituire il valore 0 per l'esito positivo. Il programma di installazione interpreta qualsiasi altro valore restituito come errore. Per ignorare i valori restituiti, impostare il flag di bit **msidbCustomActionTypeContinue** nel campo Type della [tabella CustomAction](customaction-table.md).

Per altre informazioni sull'opzione **msidbCustomActionTypeContinue** e altre opzioni di elaborazione di restituzione, vedere Opzioni di elaborazione [della restituzione dell'azione personalizzata.](custom-action-return-processing-options.md)

Si noti Windows installer converte i valori restituiti da tutte le azioni quando scrive il valore restituito nel file di log. Ad esempio, se il valore restituito dell'azione viene visualizzato come 1 nel file di log, significa che l'azione ha restituito ERROR \_ SUCCESS. Per altre informazioni su questa traduzione, vedere [Registrazione dei valori restituiti delle azioni.](logging-of-action-return-values.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codici errore](error-codes.md)
</dt> <dt>

[Registrazione dei valori restituiti dell'azione](logging-of-action-return-values.md)
</dt> </dl>

 

 



