---
description: Un gestore dell'interfaccia utente esterno può restituire un numero qualsiasi di valori da Windows Installer a seconda del tipo di pulsante fornito nel parametro di tipo del messaggio passato dal programma di installazione al gestore.
ms.assetid: a918082d-709d-4b4f-ae3b-5f16ed0ca910
title: Restituzione di valori da un gestore di interfaccia utente esterno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b466f6bc3cc034551a01bd2b87caa7292824e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754202"
---
# <a name="returning-values-from-an-external-user-interface-handler"></a>Restituzione di valori da un gestore di interfaccia utente esterno

Un gestore dell'interfaccia utente esterno può restituire un numero qualsiasi di valori da Windows Installer a seconda del tipo di pulsante fornito nel parametro di tipo del messaggio passato dal programma di installazione al gestore.

Il gestore dell'interfaccia utente esterno può restituire i valori – 1 e 0 in qualsiasi momento, perché non sono correlati ai tipi di pulsanti. Un valore restituito di – 1 indica che si è verificato un errore interno nel gestore dell'interfaccia utente esterno. Un valore restituito pari a 0 indica che il gestore dell'interfaccia utente esterno non ha gestito il messaggio del programma di installazione e che il programma di installazione deve gestire il messaggio.

Per i messaggi che non includono un tipo di pulsante, ad esempio INSTALLMESSAGE \_ ACTIONDATA e INSTALLMESSAGE \_ Progress, la restituzione di IDCANCEL Annulla l'installazione. La restituzione di IDOK notifica al programma di installazione che il messaggio è stato gestito dal gestore dell'interfaccia utente esterno.

I valori restituiti rimanenti, come descritto di seguito, sono direttamente correlati ai tipi di pulsanti inclusi nel tipo di messaggio.



| Valore restituito dall'interfaccia utente esterna | Significato                                                                                                |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| IDOK                     | Il pulsante **OK** è stato premuto dall'utente. Informazioni sul messaggio riconosciute.                     |
| IDCANCEL                 | È stato premuto il pulsante **Annulla** . Annulla l'installazione.                                            |
| IDABORT                  | È stato premuto il pulsante **Interrompi** . Interrompere l'installazione.                                              |
| IDRETRY                  | È stato premuto il pulsante **Riprova** . Ripetere l'azione.                                                |
| IDIGNORE                 | È stato premuto il pulsante **Ignora** . Ignorare l'errore e continuare.                                      |
| IDYES                    | È stato premuto il pulsante **Sì** . La risposta affermativa continua con la sequenza di eventi corrente.   |
| IDNO                     | È stato premuto il pulsante **No** . La risposta negativa non continua con la sequenza di eventi corrente. |



 

Se, ad esempio, al gestore dell'interfaccia utente esterno viene inviato un messaggio con il \_ flag di stili della finestra di messaggio MB AbortRetryIgnore (, il gestore dell'interfaccia utente esterno può restituire uno dei valori seguenti:

-   -1 (errore nel gestore dell'interfaccia utente esterno)
-   0 (nessuna azione eseguita nel gestore dell'interfaccia utente esterno, consente di Windows Installer gestirla)
-   IDABORT (pulsante **Interrompi** premuto)
-   IDRETRY (pulsante **Riprova** premuto)
-   IDIGNORE (pulsante **Ignora** premuto)

 

 



