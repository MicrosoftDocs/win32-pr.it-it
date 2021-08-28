---
title: Registrazione IIS
description: La registrazione IIS è un tipo di registrazione lato server che può essere abilitata in un gruppo di URL.
ms.assetid: 2adfee73-090a-4bc1-827e-4b0e8075e2b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd92582e048a3b1a27d88f50f33c368345c72a836b72de9f2abb777bf5e9c59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102101"
---
# <a name="iis-logging"></a>Registrazione IIS

La registrazione IIS è un tipo di registrazione lato server che può essere abilitata in un gruppo di URL. Il formato del file di log di IIS è un formato fisso basato su testo ASCII che non può essere personalizzato. Il file di log IIS contiene gli riscontri nella cache in modalità kernel dell'API del server HTTP. Questo tipo di registrazione può essere abilitato solo in un gruppo di URL. non può essere usato nella sessione del server.

Il formato del file di log di IIS registra i dati seguenti. I dati nella tabella sono nell'ordine di occorrenza nel file di log.



| Campo                | Descrizione                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Indirizzo IP client    | Indirizzo IP del client che ha eseguito la richiesta.                                                                                                                               |
| Nome utente            | Nome dell'utente autenticato che ha eseguito l'accesso al server. Gli utenti anonimi sono indicati da un trattino. La procedura consigliata è che l'applicazione fornirà sempre il nome utente. |
| Data                 | Data in cui si è verificata l'attività.                                                                                                                                          |
| Ora                 | Ora locale in cui si è verificata l'attività.                                                                                                                                    |
| Servizio e istanza | Nome del servizio Internet e numero di istanza in esecuzione nel client.                                                                                                     |
| Nome server          | Nome del server in cui è stata generata la voce del file di log.                                                                                                                 |
| Indirizzo IP del server    | Indirizzo IP del server in cui è stata generata la voce del file di log.                                                                                                           |
| Tempo impiegato           | Durata dell'azione, in millisecondi.                                                                                                                         |
| Byte client inviati    | Numero di byte inviati dal client.                                                                                                                                           |
| Byte del server inviati    | Numero di byte inviati dal server.                                                                                                                                           |
| Codice di stato del servizio  | Il valore 200 indica che la richiesta è stata soddisfatta correttamente.                                                                                                             |
| Windows di stato  | Il valore 0 (zero) indica che la richiesta è stata soddisfatta correttamente.                                                                                                        |
| Tipo di richiesta         | Verbo di richiesta.                                                                                                                                                                 |
| Destinazione dell'operazione  | Destinazione del verbo, ad esempio, Default.htm.                                                                                                                                 |
| Parametri           | Parametri passati a un oggetto scrip.                                                                                                                                        |



 

Non tutti i campi conterranno informazioni. Per i campi per cui non sono presenti informazioni, viene visualizzato un trattino (-) come segnaposto. Se un campo contiene un carattere non stampabile, l'API server HTTP lo sostituisce con un segno più (+) per mantenere il formato del file di log. Ciò si verifica in genere con attacchi di virus, quando, ad esempio, un utente malintenzionato invia ritorni a capo e avanzamento riga che, se non sostituiti con il segno più (+), interrompe il formato del file di log. I campi sono separati da virgole, semplificando la lettura del formato rispetto agli altri formati ASCII, che usano spazi per i separatori. L'ora viene registrata come ora locale. Il tempo impiegato viene registrato in millisecondi. Per altre informazioni sul campo relativo al tempo impiegato, vedere [l'argomento Registrazione W3C.](w3c-logging.md)

Nell'esempio seguente viene illustrata una voce del file di log comune NCSA.

``` syntax
192.168.114.201, -, 03/20/05, 7:55:20, W3SVC2, SERVER, 
172.21.13.45, 4502, 163, 3223, 200, 0, GET, /DeptLogo.gif, -,
```

 

 




