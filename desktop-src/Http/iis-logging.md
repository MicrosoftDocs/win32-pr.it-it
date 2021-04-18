---
title: Registrazione IIS
description: La registrazione di IIS è un tipo di registrazione lato server che può essere abilitata in un gruppo di URL.
ms.assetid: 2adfee73-090a-4bc1-827e-4b0e8075e2b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d438d0926be2579fa526cc126c7f635a6eecd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298691"
---
# <a name="iis-logging"></a>Registrazione IIS

La registrazione di IIS è un tipo di registrazione lato server che può essere abilitata in un gruppo di URL. Il formato del file di log di IIS è un formato basato su testo ASCII fisso che non può essere personalizzato. Il file di log di IIS contiene i riscontri nella cache in modalità kernel dell'API del server HTTP. Questo tipo di registrazione può essere abilitato solo in un gruppo di URL; non può essere utilizzato nella sessione del server.

Il formato del file di log di IIS registra i dati seguenti. I dati nella tabella sono nell'ordine di occorrenza nel file di log.



| Campo                | Descrizione                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Indirizzo IP client    | Indirizzo IP del client che ha eseguito la richiesta.                                                                                                                               |
| Nome utente            | Nome dell'utente autenticato che ha eseguito l'accesso al server. Gli utenti anonimi sono indicati da un trattino. È consigliabile che l'applicazione fornisca sempre il nome utente. |
| Data                 | Data in cui si è verificata l'attività.                                                                                                                                          |
| Tempo                 | Ora locale in cui si è verificata l'attività.                                                                                                                                    |
| Servizio e istanza | Il nome del servizio Internet e il numero di istanza in esecuzione nel client.                                                                                                     |
| Nome server          | Nome del server in cui è stata generata la voce del file di log.                                                                                                                 |
| Indirizzo IP del server    | Indirizzo IP del server in cui è stata generata la voce del file di log.                                                                                                           |
| Tempo impiegato           | Durata dell'azione, in millisecondi.                                                                                                                         |
| Byte client inviati    | Numero di byte inviati dal client.                                                                                                                                           |
| Byte server inviati    | Numero di byte inviati dal server.                                                                                                                                           |
| Codice di stato del servizio  | Il valore 200 indica che la richiesta è stata soddisfatta correttamente.                                                                                                             |
| Codice di stato di Windows  | Il valore 0 (zero) indica che la richiesta è stata soddisfatta correttamente.                                                                                                        |
| Tipo di richiesta         | Verbo della richiesta.                                                                                                                                                                 |
| Destinazione dell'operazione  | La destinazione del verbo, ad esempio Default.htm.                                                                                                                                 |
| Parametri           | Parametri passati a una bisaccia.                                                                                                                                        |



 

Non tutti i campi conterranno informazioni. Per i campi per i quali non sono disponibili informazioni, un trattino (-) viene visualizzato come segnaposto. Se un campo contiene un carattere non stampabile, l'API server HTTP la sostituisce con un segno più (+) per mantenere il formato del file di log. Questa situazione si verifica in genere con attacchi di virus, quando, ad esempio, un utente malintenzionato invia ritorni a capo e feed di riga che, se non sostituiti con il segno più (+), interrompono il formato del file di log. I campi sono separati da virgole, semplificando la lettura del formato rispetto agli altri formati ASCII, che usano spazi per i separatori. L'ora viene registrata come ora locale. Il tempo impiegato viene registrato in millisecondi. Per ulteriori informazioni sul campo relativo al tempo impiegato, vedere l'argomento relativo alla [registrazione di W3C](w3c-logging.md) .

Nell'esempio seguente viene illustrata una voce del file di log comune NCSA.

``` syntax
192.168.114.201, -, 03/20/05, 7:55:20, W3SVC2, SERVER, 
172.21.13.45, 4502, 163, 3223, 200, 0, GET, /DeptLogo.gif, -,
```

 

 




