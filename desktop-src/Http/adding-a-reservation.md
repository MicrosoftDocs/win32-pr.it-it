---
title: Aggiunta di una prenotazione
description: Il database di routing contiene l'elenco delle prenotazioni.
ms.assetid: c36e731c-6a0b-42a8-bc92-106a8e017b0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac683c48748fa0e644f2f7569590b3783c521f1d10a1a5852a638a29731daf38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014949"
---
# <a name="adding-a-reservation"></a>Aggiunta di una prenotazione

Il database di routing contiene l'elenco delle prenotazioni. L'elenco delle prenotazioni è costituito dagli utenti a cui è consentito l'accesso allo spazio dei nomi, nonché dal livello di accesso per ogni utente elencato nella prenotazione. Quando le prenotazioni vengono aggiunte o eliminate, viene effettuata una ricerca nel database di routing per determinare i privilegi di accesso.

Oltre a controllare l'ID utente, l'API del server HTTP verifica anche la presenza di conflitti nelle prenotazioni esistenti prima di installare una nuova prenotazione.

**Per aggiungere una nuova prenotazione**

1.  Se il numero di porta in UrlPrefix ha prenotazioni o registrazioni per uno schema diverso dallo schema in UrlPrefix, la registrazione non riesce. HTTP e HTTPS non possono essere supportati sulla stessa porta.
2.  Individuare il bucket appropriato per la registrazione (vedere la sezione Routing delle richieste [in ingresso),](routing-incoming-requests.md) in base al tipo di host. I passaggi rimanenti sono relativi a questo bucket.
3.  Selezionare le voci di prenotazione con i componenti schema, host e porta che corrispondono al valore UrlPrefix riservato. Da questi, individuare la voce con il *valore relativeUri* corrispondente più lungo diverso da relativeUri nella prenotazione , ovvero il *nodo padre*. Se la voce esiste, valutare i diritti di accesso in base all'ACL assegnato a tale voce.
4.  Se non è stato trovato un nodo padre, si tratta di una prenotazione con un relativeUri vuoto o una *prenotazione radice.* Concedere i diritti di accesso solo se il chiamante è registrato con gli account LocalSystem o Administrator.
5.  Se vengono concessi diritti di accesso, verificare la presenza di prenotazioni duplicate. Se esiste una voce di prenotazione con lo stesso schema, porta, host e relativeUri, viene restituito un codice ERROR \_ ALREADY \_ EXISTS.
    > [!Note]  
    > L'aggiornamento di una voce esistente deve essere eseguito in due passaggi: eliminare la voce e aggiungerne una nuova.

     

Se i passaggi precedenti hanno esito positivo, viene immessa una nuova voce di prenotazione nel database di prenotazione.

> [!Note]  
> La nuova voce viene creata con l'ACL specificato e non eredita gli ACL dalla *voce* padre.

 

Gli esempi seguenti illustrano il processo di prenotazione.

-   Prenotazione 1: `https://+:80/vroot/subdir/` l'amministratore per l'utente A e l'utente C ha esito positivo e viene immesso nel bucket "+".
-   Prenotazione 2: `https://adatum.com:80/vroot/` l'amministratore per l'utente B ha esito positivo e viene immesso nel bucket "Host esplicito".
-   Prenotazione 3: `https://adatum.com:80/vroot/subdir/otherdir/` l'utente B per l'utente C ha esito positivo a causa della prenotazione 2.
-   Prenotazione 4: `https://+:80/vroot/subdir/otherdir/` l'utente A per l'utente E ha esito positivo a causa della prenotazione 1.
-   Prenotazione 5: `https://adatum.com:80/vroot/subdir/otherdir/` l'utente A per l'utente E ha esito negativo. Accesso negato a causa della prenotazione 2.
-   Prenotazione 6: `https://+:80/vroot/subdir/` l'amministratore per l'utente A ha esito negativo. La prenotazione è in conflitto con la prenotazione 1.
-   Prenotazione 7: `https://adatum.com:80/newroot/` l'utente A per l'utente A ha esito negativo. Accesso negato a causa di una prenotazione radice implicita `https://adatum.com:80/` di per LocalSystem o Administrator.

Le prenotazioni possono influire sul set di URL nelle richieste recapitate a un processo che in precedenza ha registrato un UrlPrefix. Ad esempio, si consideri lo scenario seguente.

-   Registrazione: `https://adatum.com:80/vroot/` dall'applicazione 1 per l'utente A.
-   Una richiesta per `https://adatum.com:80/vroot/subdir/file.htm` viene recapitata all'applicazione 1.
-   Prenotazione: `https://+:80/vroot/subdir/` per l'utente B.
-   Una richiesta per `https://adatum.com:80/vroot/subdir/file.htm` viene ora rifiutata.
-   Registrazione: `https://adatum.com:80/vroot/subdir/` dall'applicazione 2 per l'utente B.
-   Una richiesta per `https://adatum.com:80/vroot/subdir/file.htm` viene recapitata all'applicazione 2.

 

 




