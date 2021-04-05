---
title: Registrazione NCSA
description: Registrazione estesa NCSA è un tipo di registrazione lato server che può essere abilitato in un gruppo di URL.
ms.assetid: 14a2492a-3bcf-46f3-a3a5-1ea578516865
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f04db62d5d561fb227f7a46a33c2aefcacd943b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713954"
---
# <a name="ncsa-logging"></a>Registrazione NCSA

Registrazione estesa NCSA è un tipo di registrazione lato server che può essere abilitato in un gruppo di URL. Il formato di file di log comune NCSA è un formato basato su testo ASCII fisso che non può essere personalizzato. Il file di registro NCSA contiene i riscontri nella cache in modalità kernel dell'API del server HTTP. Questo tipo di registrazione può essere abilitato solo in un gruppo di URL; non può essere utilizzato nella sessione del server.

Il formato di file di log comune NCSA registra i dati seguenti. I dati nella tabella sono nell'ordine di occorrenza nel file di log.



| Campo                                            | Descrizione                                                                                                                                                                       |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Indirizzo host remoto                              | Indirizzo IP del client che ha eseguito la richiesta.                                                                                                                               |
| Nome registro remoto                                  | Non usato. Questo valore è sempre un trattino.                                                                                                                                          |
| Nome utente                                        | Nome dell'utente autenticato che ha eseguito l'accesso al server. Gli utenti anonimi sono indicati da un trattino. È consigliabile che l'applicazione fornisca sempre il nome utente. |
| Offset di data, ora e ora di Greenwich (GMT) | Data e ora locali in cui si è verificata l'attività. Viene indicato anche l'offset rispetto all'ora di Greenwich.                                                                    |
| Versione della richiesta e del protocollo                     | Versione del protocollo HTTP utilizzata dal client.                                                                                                                                   |
| Codice di stato del servizio                              | Codice di stato HTTP. Il valore 200 indica che la richiesta è stata completata correttamente.                                                                                         |
| Byte inviati                                       | Numero di byte inviati dal server.                                                                                                                                           |



 

Non tutti i campi conterranno informazioni. Per i campi per i quali non sono disponibili informazioni, un trattino (-) viene visualizzato come segnaposto. Se un campo contiene un carattere non stampabile, l'API server HTTP la sostituisce con un segno più (+) per mantenere il formato del file di log. Questa situazione si verifica in genere con attacchi di virus, quando, ad esempio, un utente malintenzionato invia ritorni a capo e feed di riga che, se non sostituiti con il segno più (+), interrompono il formato del file di log. I campi sono separati da spazi e l'ora viene registrata come ora locale con l'offset GMT.

Nell'esempio seguente viene illustrata una voce del file di log comune NCSA, come visualizzato in un editor di testo.

``` syntax
172.21.13.45 - Microsoft\JohnDoe [07/Apr/2004:17:39:04 -0800] 
"GET /scripts/iisadmin/ism.dll?http/serv HTTP/1.0" 200 3401
```

L'indirizzo IP del client è 172.21.13.45 e il nome utente è Microsoft \\ johndoe. Il log è stato registrato il 7 aprile 2005 alle 17:39:04 ora locale con un offset di Greenwich di 8 ore. Il verbo della richiesta e la versione del protocollo erano "GET/scripts/IISADMIN/ism.dll? http/serv HTTP/1.0". I codici di stato sono 200 OK e il numero di byte inviati dal client è 3401.

 

 




