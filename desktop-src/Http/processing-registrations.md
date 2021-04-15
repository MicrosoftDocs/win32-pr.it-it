---
title: Elaborazione delle registrazioni
description: Le API del server HTTP utilizzano il database di routing per applicare i controlli di accesso durante le registrazioni.
ms.assetid: d72aa213-b8e8-4fe9-b98c-41114d2cea56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1e02d2511d9967454d5cbddd93b2c0380d1172
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104474609"
---
# <a name="processing-registrations"></a>Elaborazione delle registrazioni

Le API del server HTTP utilizzano il database di routing per applicare i controlli di accesso durante le registrazioni. Una registrazione per un [URLPrefix](urlprefix-strings.md) deve superare una serie di controlli di accesso per assicurarsi che l'utente che esegue la registrazione per lo spazio dei nomi disponga dei diritti di accesso. Usare la funzione [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) per aggiungere una nuova registrazione.

**Per aggiungere una nuova registrazione con HttpAddUrl**

1.  Se il numero di porta in UrlPrefix include prenotazioni o registrazioni per uno schema diverso dallo schema nella UrlPrefix, la registrazione non riesce. HTTP e HTTPS non possono essere supportati sulla stessa porta.
2.  La registrazione viene inserita nel bucket appropriato per la registrazione. I bucket sono basati sul tipo di host dell'URL, come descritto nella sezione [routing delle richieste in ingresso](routing-incoming-requests.md) . I passaggi seguenti sono relativi a questo particolare bucket.
3.  Se esiste una voce di registrazione duplicata, restituire un codice di errore.
4.  Selezionare le voci di prenotazione con i componenti schema, host e porta uguali a quelli di UrlPrefix. Da questi individuare la voce con la corrispondenza **relativeUri** più estesa. Se la voce esiste, controllare le autorizzazioni in base all'ACL associato a tale voce e restituire success. Se la voce non esiste, restituire un codice di errore \_ già \_ esistente.

Negli esempi seguenti viene illustrato il processo di installazione di una registrazione nel database di routing. Le prenotazioni 1 e 2 sono presenti nel database di routing.

-   Prenotazione 1: `https://+:80/vroot/subdir/` per l'utente a e l'utente C. Questa prenotazione viene inserita nel bucket "+".
-   Prenotazione 2: `https://adatum.com:80/vroot/` per l'utente B. Questa prenotazione viene inserita nel bucket "host esplicito".
-   Registrazione: l' `https://+:80/vroot/subdir/` utente B ha esito negativo a causa della prenotazione 1.
-   Registrazione: l' `https://adatum.com:80/vroot/subdir/` utente B ha esito positivo a causa della prenotazione 2.
-   Registrazione: `https://adatum.com:80/vroot/subdir/` l'utente C non riesce a causa della prenotazione più esplicita 2. La prenotazione con carattere jolly sicuro non ha significato nel contesto della prenotazione o della registrazione esplicita.
-   Registrazione: `https://+:80/vroot/subdir/` l'utente a ha esito positivo a causa della prenotazione 1.
-   Registrazione: l' `https://adatum.com:80/vroot/anotherdir/` utente B ha esito positivo a causa della prenotazione 2.

Il controllo dell'accesso per la registrazione non include i controlli per i privilegi di delega. Non sono presenti controlli di accesso basati sulle prenotazioni (vedere [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl)). L'unico requisito per eliminare una registrazione è che il processo chiamante deve avere creato la registrazione.

 

 




