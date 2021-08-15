---
title: Elaborazione delle registrazioni
description: Le API del server HTTP usano il database di routing per applicare i controlli di accesso durante le registrazioni.
ms.assetid: d72aa213-b8e8-4fe9-b98c-41114d2cea56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74454d888cccf083e27fc9067c8a5485e286b4f55df4c5c18f2b2e490dc9db39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393844"
---
# <a name="processing-registrations"></a>Elaborazione delle registrazioni

Le API del server HTTP usano il database di routing per applicare i controlli di accesso durante le registrazioni. Una registrazione per [urlPrefix](urlprefix-strings.md) deve superare una serie di controlli di accesso per garantire che l'utente che esegue la registrazione per lo spazio dei nomi abbia diritti di accesso. Usare la [**funzione HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) per aggiungere una nuova registrazione.

**Per aggiungere una nuova registrazione con HttpAddUrl**

1.  Se il numero di porta in UrlPrefix ha prenotazioni o registrazioni per uno schema diverso dallo schema in UrlPrefix, la registrazione ha esito negativo. HTTP e HTTPS non possono essere supportati sulla stessa porta.
2.  La registrazione viene inserito nel bucket appropriato per la registrazione. I bucket sono basati sul tipo di host dell'URL, come descritto nella sezione [Routing delle richieste in](routing-incoming-requests.md) ingresso. I passaggi seguenti sono relativi a questo bucket specifico.
3.  Se esiste una voce di registrazione duplicata, restituire un codice di errore.
4.  Selezionare le voci di prenotazione con componenti di schema, host e porta uguali a quelli di UrlPrefix. Da questi, individuare la voce con la corrispondenza **relativeUri più** lunga. Se la voce esiste, controllare le autorizzazioni in base all'elenco di controllo di accesso associato a tale voce e restituire l'esito positivo. Se la voce non esiste, restituire un codice ERROR \_ ALREADY \_ EXISTS.

Negli esempi seguenti viene illustrato il processo di installazione di una registrazione nel database di routing. Le prenotazioni 1 e 2 sono presenti nel database di routing.

-   Prenotazione 1: `https://+:80/vroot/subdir/` per l'utente A e l'utente C. Questa prenotazione viene inserita nel bucket "+".
-   Prenotazione 2: `https://adatum.com:80/vroot/` per l'utente B. Questa prenotazione viene inserita nel bucket "Host esplicito".
-   Registrazione: `https://+:80/vroot/subdir/` l'utente B ha esito negativo a causa della prenotazione 1.
-   Registrazione: `https://adatum.com:80/vroot/subdir/` l'utente B ha esito positivo a causa della prenotazione 2.
-   Registrazione: `https://adatum.com:80/vroot/subdir/` l'utente C ha esito negativo a causa della prenotazione più esplicita 2. La prenotazione con caratteri jolly forti non ha significato nel contesto della prenotazione o della registrazione esplicita.
-   Registrazione: `https://+:80/vroot/subdir/` l'utente A ha esito positivo a causa della prenotazione 1.
-   Registrazione: `https://adatum.com:80/vroot/anotherdir/` l'utente B ha esito positivo a causa della prenotazione 2.

Il controllo di accesso per la registrazione non include i controlli per i privilegi di delega. Non sono disponibili controlli di accesso in base alle prenotazioni (vedere [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl)). L'unico requisito per l'eliminazione di una registrazione è che il processo chiamante abbia creato la registrazione.

 

 




