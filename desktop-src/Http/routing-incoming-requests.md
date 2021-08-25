---
title: Routing delle richieste in ingresso
description: L'API server HTTP gestisce un database di routing per determinare quale applicazione riceve una richiesta in ingresso.
ms.assetid: 7c613137-66bd-4375-93cb-b5562823bc12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e40feab96a913da895633bddd8e53697b6aeef959162da054da22aeeedef652a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829961"
---
# <a name="routing-incoming-requests"></a>Routing delle richieste in ingresso

L'API server HTTP gestisce un database di routing per determinare quale applicazione riceve una richiesta in ingresso. La tabella di routing viene compilata dal database di prenotazione e contiene le voci di prenotazione e le registrazioni correnti. Quando viene effettuata una registrazione o una prenotazione, questa viene inserita nel bucket del database di routing che corrisponde al tipo di host, come indicato di seguito:

-   \+ : le registrazioni delle porte vengono inserite nel bucket "Carattere jolly sicuro"

-   host: le registrazioni delle porte vengono inserite nel bucket "Explicit"

-   IP: le registrazioni delle porte vengono inserite nel bucket "Carattere jolly debole associato all'IP"

-   \* : le registrazioni delle porte vengono inserite nel bucket "Carattere jolly debole"

Questi passaggi fanno riferimento anche all'ordine in cui vengono elaborate le richieste HTTP in ingresso. Prima vengono controllate le prenotazioni con caratteri jolly forti, quindi la prenotazione esplicita, seguita dal carattere jolly debole associato all'indirizzo IP e dal carattere jolly debole. La ricerca si interrompe quando viene trovata una corrispondenza in modo che le registrazioni in uno dei bucket rimanenti non siano state trovate.

L'algoritmo di routing dell'API del server HTTP individua la corrispondenza migliore per [UrlPrefix](urlprefix-strings.md) cercando sia le voci di registrazione che le voci di prenotazione del database di routing, a partire dal bucket con caratteri jolly avanzati e terminando con il bucket con caratteri jolly deboli. La corrispondenza migliore, all'interno di un bucket, è la corrispondenza più lunga nella parte RELATIVA DELL'URI di UrlPrefix (presupponendo una corrispondenza esatta per le parti host, porta e schema dell'URL). Quando viene trovata una corrispondenza in un bucket, l'algoritmo di routing arresta la ricerca e ignora tutti i bucket con priorità inferiore.

Si considerino ad esempio le registrazioni seguenti ,elencate in ordine decrescente di priorità in base ai tipi di bucket:

-   Registrazione: `https://+:80/vroot/` è registrata dall'applicazione 1

-   Registrazione: `https://adatum.com:80/` è registrata dall'applicazione 2

-   Registrazione: `https://\*:80/` è registrata dall'applicazione 3

Una richiesta in ingresso `https://adatum.com:80/vroot/subdir/file.htm/` per viene recapitata all'applicazione 1. Una richiesta in ingresso `https://adatum.com:80/default.htm/` per viene recapitata all'applicazione 2. Una richiesta in ingresso `https://otheradatum.com:80/file.htm/` per viene recapitata all'applicazione 3.

Se la corrispondenza migliore è una voce di prenotazione, significa che l'applicazione che deve ricevere la richiesta non è in esecuzione. Si considerino ad esempio la registrazione e la prenotazione seguenti:

-   Registrazione: `https://\*:80/vroot/` è registrata dall'applicazione 1, utente A

-   Prenotazione: `https://adatum.com:80/` è stata riservata per l'utente B

Una richiesta in ingresso per non viene recapitata all'applicazione 1 perché la corrispondenza migliore porta alla voce di prenotazione per `https://adatum.com:80/vroot/file.htm/` l'utente B. Le regole di precedenza vengono applicate in questo caso alla prenotazione con una priorità più alta. Se non è attivo alcun processo autorizzato e registrato per le richieste di servizio per l'URL ricevuto, la richiesta viene rifiutata con un codice di stato 400 (Richiesta non valida).

 

 




