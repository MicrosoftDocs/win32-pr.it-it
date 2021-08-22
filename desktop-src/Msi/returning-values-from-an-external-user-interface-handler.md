---
description: Un gestore dell'interfaccia utente esterno può restituire qualsiasi numero di valori Windows Installer Windows base al tipo di pulsante specificato nel parametro del tipo di messaggio che il programma di installazione passa al gestore.
ms.assetid: a918082d-709d-4b4f-ae3b-5f16ed0ca910
title: Restituzione di valori da un gestore Interfaccia utente esterno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b4ba5edcd87b0d4f324762f840c117425b322ea03d1dd15e103c05bcf12352
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626081"
---
# <a name="returning-values-from-an-external-user-interface-handler"></a>Restituzione di valori da un gestore Interfaccia utente esterno

Un gestore dell'interfaccia utente esterno può restituire qualsiasi numero di valori Windows Installer Windows base al tipo di pulsante specificato nel parametro del tipo di messaggio che il programma di installazione passa al gestore.

Il gestore dell'interfaccia utente esterno può restituire i valori –1 e 0 in qualsiasi momento perché non sono correlati ai tipi di pulsante. Il valore restituito –1 indica che si è verificato un errore interno nel gestore dell'interfaccia utente esterno. Il valore restituito 0 indica che il gestore dell'interfaccia utente esterno non ha gestito il messaggio del programma di installazione e che il programma di installazione deve invece gestire il messaggio.

Per i messaggi che non includono un tipo di pulsante, ad esempio INSTALLMESSAGE ACTIONDATA e INSTALLMESSAGE PROGRESS, la restituzione di IDCANCEL annulla \_ \_ l'installazione. La restituzione di IDOK notifica al programma di installazione che il messaggio è stato gestito dal gestore dell'interfaccia utente esterno.

I valori restituiti rimanenti, come descritto di seguito, sono direttamente correlati ai tipi di pulsante inclusi nel tipo di messaggio.



| Valore restituito dell'interfaccia utente esterna | Significato                                                                                                |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| IDOK                     | Il **pulsante OK** è stato premuto dall'utente. Le informazioni del messaggio sono comprese.                     |
| IDCANCEL                 | È **stato premuto** il pulsante CANCEL. Annullare l'installazione.                                            |
| IDABORT                  | È stato premuto il pulsante **ABORT.** Interrompere l'installazione.                                              |
| IDRETRY                  | È stato premuto il pulsante **RETRY.** Provare di nuovo a eseguire l'azione.                                                |
| IDIGNORE                 | È stato premuto il pulsante **IGNORE.** Ignorare l'errore e continuare.                                      |
| IDYES                    | È **stato premuto** il pulsante SÌ. La risposta affermativa, continuare con la sequenza corrente di eventi.   |
| IDNO                     | È stato premuto il pulsante **NO.** La risposta negativa, non continuare con la sequenza corrente di eventi. |



 

Ad esempio, se al gestore dell'interfaccia utente esterno viene inviato un messaggio con il flag di stili della finestra di messaggio MB ABORTRETRYIGNORE, il gestore dell'interfaccia utente esterno può restituire uno \_ dei valori seguenti:

-   -1 (errore nel gestore dell'interfaccia utente esterno)
-   0 (nessuna azione eseguita nel gestore dell'interfaccia utente esterno, che Windows programma di installazione gestirlo)
-   IDABORT **(pulsante ABORT** premuto)
-   IDRETRY **(pulsante RETRY** premuto)
-   IDIGNORE **(pulsante IGNORE** premuto)

 

 



