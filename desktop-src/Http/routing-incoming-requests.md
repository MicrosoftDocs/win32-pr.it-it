---
title: Routing delle richieste in ingresso
description: L'API server HTTP gestisce un database di routing per determinare quale applicazione riceve una richiesta in ingresso.
ms.assetid: 7c613137-66bd-4375-93cb-b5562823bc12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da483030441f3a9239eef153da59212166bce9eb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104399897"
---
# <a name="routing-incoming-requests"></a>Routing delle richieste in ingresso

L'API server HTTP gestisce un database di routing per determinare quale applicazione riceve una richiesta in ingresso. La tabella di routing è compilata dal database di prenotazione e contiene le voci di prenotazione nonché le registrazioni correnti. Quando viene effettuata una registrazione o una prenotazione, questa viene inserita nel bucket del database di routing che corrisponde al tipo di host, come indicato di seguito:

-   \+ : le registrazioni delle porte vengono inserite nel bucket "con carattere jolly sicuro"

-   host: le registrazioni delle porte vengono inserite nel bucket "esplicito"

-   IP: le registrazioni delle porte vengono inserite nel bucket "con carattere jolly vulnerabile associato a IP"

-   \* : le registrazioni delle porte vengono inserite nel bucket "con carattere jolly debole"

Questa procedura si riferisce anche all'elaborazione delle richieste HTTP in ingresso. Prima le prenotazioni con caratteri jolly forti, quindi la prenotazione esplicita vengono controllate seguito dal carattere jolly debole associato a IP e dal carattere jolly vulnerabile. La ricerca viene arrestata quando viene trovata una corrispondenza in modo che non vengano trovate le registrazioni in uno dei bucket rimanenti.

L'algoritmo di routing dell'API del server HTTP individua la migliore corrispondenza per [URLPrefix](urlprefix-strings.md) eseguendo una ricerca nelle voci di registrazione e nelle voci di prenotazione del database di routing, iniziando dal bucket con carattere jolly complesso e terminando con il bucket con carattere jolly vulnerabile. La corrispondenza migliore, all'interno di un bucket, è la corrispondenza più estesa nella parte URI relativa di UrlPrefix (presupponendo una corrispondenza esatta per l'host, la porta e le parti dello schema dell'URL). Quando viene trovata una corrispondenza in un bucket, l'algoritmo di routing interrompe la ricerca e ignora tutti i bucket con priorità più bassa.

Si considerino, ad esempio, le registrazioni seguenti (elencate in ordine decrescente di priorità in base ai tipi di bucket:

-   Registrazione: `https://+:80/vroot/` è registrata dall'applicazione 1

-   Registrazione: `https://adatum.com:80/` è registrata dall'applicazione 2

-   Registrazione: `https://\*:80/` è registrata dall'applicazione 3

Una richiesta in ingresso per `https://adatum.com:80/vroot/subdir/file.htm/` viene inviata all'applicazione 1. Una richiesta in ingresso per `https://adatum.com:80/default.htm/` viene inviata all'applicazione 2. Una richiesta in ingresso per `https://otheradatum.com:80/file.htm/` viene inviata all'applicazione 3.

Se la corrispondenza migliore è una voce di prenotazione, significa che l'applicazione che deve ricevere la richiesta non è in esecuzione. Si consideri, ad esempio, la registrazione e la prenotazione seguenti:

-   Registrazione: `https://\*:80/vroot/` è registrata dall'applicazione 1, dall'utente A

-   Prenotazione: `https://adatum.com:80/` è stata riservata all'utente B

Una richiesta in ingresso per `https://adatum.com:80/vroot/file.htm/` non viene recapitata all'applicazione 1 perché la corrispondenza migliore porta alla voce di prenotazione per l'utente B. Le regole di precedenza vengono applicate in questo caso alla prenotazione con una priorità più alta. Se non è attivo alcun processo autorizzato e registrato per richieste di assistenza per l'URL ricevuto, la richiesta viene rifiutata con un codice di stato 400 (richiesta non valida).

 

 




