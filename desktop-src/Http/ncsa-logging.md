---
title: Registrazione NCSA
description: La registrazione estesa NCSA è un tipo di registrazione lato server che può essere abilitata in un gruppo di URL.
ms.assetid: 14a2492a-3bcf-46f3-a3a5-1ea578516865
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a5b9ef608da18264f4534c7e50e9672794a21bc61c91741feeb9e814c7afc8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078311"
---
# <a name="ncsa-logging"></a>Registrazione NCSA

La registrazione estesa NCSA è un tipo di registrazione lato server che può essere abilitata in un gruppo di URL. Il formato del file di log NCSA Common è un formato fisso basato su testo ASCII che non può essere personalizzato. Il file di log NCSA contiene gli riscontri nella cache in modalità kernel dell'API del server HTTP. Questo tipo di registrazione può essere abilitato solo in un gruppo di URL. non può essere usato nella sessione del server.

Il formato del file di log NCSA Common registra i dati seguenti. I dati nella tabella sono nell'ordine di occorrenza nel file di log.



| Campo                                            | Descrizione                                                                                                                                                                       |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Indirizzo host remoto                              | Indirizzo IP del client che ha eseguito la richiesta.                                                                                                                               |
| Nome del log remoto                                  | Non usato. Questo valore è sempre un trattino.                                                                                                                                          |
| Nome utente                                        | Nome dell'utente autenticato che ha eseguito l'accesso al server. Gli utenti anonimi sono indicati da un trattino. La procedura consigliata è che l'applicazione fornirà sempre il nome utente. |
| Offset di data, ora e ora media di Greenwich (GMT) | Data e ora locali in cui si è verificata l'attività. Viene indicato anche l'offset dall'ora media di Greenwich.                                                                    |
| Versione richiesta e protocollo                     | Versione del protocollo HTTP usata dal client.                                                                                                                                   |
| Codice di stato del servizio                              | Codice di stato HTTP. Il valore 200 indica che la richiesta è stata completata correttamente.                                                                                         |
| Byte inviati                                       | Numero di byte inviati dal server.                                                                                                                                           |



 

Non tutti i campi conterranno informazioni. Per i campi per cui non sono presenti informazioni, viene visualizzato un trattino (-) come segnaposto. Se un campo contiene un carattere non stampabile, l'API server HTTP lo sostituisce con un segno più (+) per mantenere il formato del file di log. Ciò si verifica in genere con attacchi di virus, quando, ad esempio, un utente malintenzionato invia ritorni a capo e avanzamento riga che, se non sostituiti con il segno più (+), interrompe il formato del file di log. I campi sono separati da spazi e l'ora viene registrata come ora locale con l'offset GMT.

Nell'esempio seguente viene illustrata una voce del file di log NCSA Common, visualizzata in un editor di testo.

``` syntax
172.21.13.45 - Microsoft\JohnDoe [07/Apr/2004:17:39:04 -0800] 
"GET /scripts/iisadmin/ism.dll?http/serv HTTP/1.0" 200 3401
```

L'indirizzo IP del client è 172.21.13.45 e il nome utente è Microsoft \\ JohnDoe. Il log è stato registrato il 7 aprile 2005 alle 17:39:04 ora locale con un offset di Greenwich di 8 ore. La versione del verbo di richiesta e del protocollo era "GET /scripts/iisadmin/ism.dll?http/serv HTTP/1.0". I codici di stato erano 200 OK e il numero di byte inviati dal client era 3401.

 

 




