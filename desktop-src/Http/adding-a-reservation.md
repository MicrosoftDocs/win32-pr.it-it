---
title: Aggiunta di una prenotazione
description: Il database di routing contiene l'elenco delle prenotazioni.
ms.assetid: c36e731c-6a0b-42a8-bc92-106a8e017b0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358181cbe57a046f5af54f7adf17bdadb24c3ddc
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104517200"
---
# <a name="adding-a-reservation"></a>Aggiunta di una prenotazione

Il database di routing contiene l'elenco delle prenotazioni. L'elenco delle prenotazioni è costituito dagli utenti a cui è consentito l'accesso allo spazio dei nomi, nonché dal livello di accesso per ogni utente elencato sotto la prenotazione. Quando si aggiungono o eliminano prenotazioni, viene eseguita la ricerca del database di routing per determinare i privilegi di accesso.

Oltre a controllare l'ID utente, l'API server HTTP verifica anche la presenza di conflitti nelle prenotazioni esistenti prima di installare una nuova prenotazione.

**Per aggiungere una nuova prenotazione**

1.  Se il numero di porta in UrlPrefix include prenotazioni o registrazioni per uno schema diverso dallo schema nella UrlPrefix, la registrazione non riesce. HTTP e HTTPS non possono essere supportati sulla stessa porta.
2.  Individuare il bucket appropriato per la registrazione (vedere la sezione [routing delle richieste in ingresso](routing-incoming-requests.md) ), in base al tipo di host. I passaggi rimanenti sono relativi a questo bucket.
3.  Selezionare le voci di prenotazione con i componenti schema, host e porta che corrispondono ai UrlPrefix riservati. Da questi individuare la voce con il *relativeUri* corrispondente più lungo che non è uguale a relativeUri nella prenotazione, ovvero il *nodo padre*. Se la voce esiste, valutare i diritti di accesso in base all'ACL assegnato a tale voce.
4.  Se non è stato trovato alcun nodo padre, si tratta di una prenotazione con una relativeUri vuota o una *prenotazione radice*. Concedere i diritti di accesso solo se il chiamante viene registrato con gli account LocalSystem o Administrator.
5.  Se vengono concessi i diritti di accesso, verificare la presenza di prenotazioni duplicate. Se esiste una voce di prenotazione con lo stesso schema, porta, host e relativeUri, viene restituito un errore di \_ \_ codice esistente.
    > [!Note]  
    > L'aggiornamento di una voce esistente deve essere eseguito in due passaggi: eliminare la voce e aggiungerne una nuova.

     

Se il passaggio precedente ha esito positivo, viene immessa una nuova voce di prenotazione nel database di prenotazione.

> [!Note]  
> La nuova voce viene creata con l'ACL specificato e non eredita gli ACL dalla voce *padre* .

 

Gli esempi seguenti illustrano il processo di prenotazione.

-   Prenotazione 1: `https://+:80/vroot/subdir/` per amministratore per l'utente A e l'utente C ha esito positivo e viene immesso nel bucket "+".
-   Prenotazione 2: `https://adatum.com:80/vroot/` l'amministratore dell'utente B ha esito positivo e viene immesso nel bucket "host esplicito".
-   Prenotazione 3: l' `https://adatum.com:80/vroot/subdir/otherdir/` utente B per l'utente C ha esito positivo a causa della prenotazione 2.
-   Prenotazione 4: `https://+:80/vroot/subdir/otherdir/` l'utente a per l'utente E ha esito positivo a causa della prenotazione 1.
-   Prenotazione 5: `https://adatum.com:80/vroot/subdir/otherdir/` l'utente a per l'utente E non riesce. Accesso negato a causa della prenotazione 2.
-   Prenotazione 6: `https://+:80/vroot/subdir/` l'amministratore per l'utente a ha esito negativo. La prenotazione è in conflitto con la prenotazione 1.
-   Prenotazione 7: l' `https://adatum.com:80/newroot/` utente a per l'utente a ha esito negativo. Accesso negato a causa della prenotazione radice implicita di `https://adatum.com:80/` per LocalSystem o Administrator.

Le prenotazioni possono influenzare il set di URL nelle richieste recapitate a un processo che ha precedentemente registrato un UrlPrefix. Ad esempio, si consideri lo scenario seguente.

-   Registrazione: `https://adatum.com:80/vroot/` per l'applicazione 1 per l'utente a.
-   Una richiesta per `https://adatum.com:80/vroot/subdir/file.htm` viene recapitata all'applicazione 1.
-   Prenotazione: `https://+:80/vroot/subdir/` per l'utente B.
-   Una richiesta per `https://adatum.com:80/vroot/subdir/file.htm` è stata rifiutata.
-   Registrazione: `https://adatum.com:80/vroot/subdir/` per l'applicazione 2 per l'utente B.
-   Una richiesta per `https://adatum.com:80/vroot/subdir/file.htm` viene recapitata all'applicazione 2.

 

 




