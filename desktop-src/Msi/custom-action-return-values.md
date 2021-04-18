---
description: Se l'opzione di elaborazione msidbCustomActionTypeContinue return non è impostata, l'azione personalizzata deve restituire un codice di stato Integer, come illustrato nella tabella seguente.
ms.assetid: 56c2d639-eef8-47cd-9d47-9a4781b9be36
title: Valori restituiti dell'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c01ba6273aea6cf950edb56ef3c2a94ab9a272d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319019"
---
# <a name="custom-action-return-values"></a>Valori restituiti dell'azione personalizzata

Se l'opzione di elaborazione **msidbCustomActionTypeContinue** return non è impostata, l'azione personalizzata deve restituire un codice di stato Integer, come illustrato nella tabella seguente.



| Valore restituito                 | Descrizione                           |
|------------------------------|---------------------------------------|
| funzione di errore \_ \_ non \_ chiamata | L'azione non è stata eseguita.                  |
| ERRORE \_ riuscito               | Azioni completate correttamente.       |
| ERRORE di \_ installazione di \_ USEREXIT     | L'utente è stato terminato in modo anomalo.          |
| ERRORE di \_ installazione \_      | Si è verificato un errore irreversibile.         |
| ERRORE \_ nessun \_ altro \_ elemento       | Ignorare le azioni rimanenti, non un errore. |



 

Si noti che le azioni personalizzate che sono [file eseguibili](executable-files.md) devono restituire un valore pari a 0 per l'esito positivo. Il programma di installazione interpreta qualsiasi altro valore restituito come errore. Per ignorare i valori restituiti, impostare il flag di bit **msidbCustomActionTypeContinue** nel campo Type della [tabella CustomAction](customaction-table.md).

Per altre informazioni sull'opzione **msidbCustomActionTypeContinue** e su altre opzioni di elaborazione, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).

Si noti che Windows Installer converte i valori restituiti da tutte le azioni quando scrive il valore restituito nel file di log. Se, ad esempio, il valore restituito dell'azione viene visualizzato come 1 nel file di log, significa che l'azione ha restituito l'errore \_ Success. Per ulteriori informazioni su questa traduzione, vedere [registrazione dei valori restituiti dell'azione](logging-of-action-return-values.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codici errore](error-codes.md)
</dt> <dt>

[Registrazione dei valori restituiti dell'azione](logging-of-action-return-values.md)
</dt> </dl>

 

 



