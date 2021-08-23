---
description: In un protocollo dell'applicazione client/server, un server esegue il binding a una porta di comunicazione, ad esempio un socket o un'interfaccia RPC.
ms.assetid: 176d4ca5-83dd-42ef-b116-227d4badc0dd
title: Definizione di una connessione protetta con l'autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad5f9458cf578481e049dcf2b41d6607b3c6151ce16a938cfe0e398ae7b3bf56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008249"
---
# <a name="establishing-a-secure-connection-with-authentication"></a>Definizione di una connessione protetta con l'autenticazione

In un protocollo [*dell'applicazione*](/windows/desktop/SecGloss/a-gly)client/server un server esegue il binding a una porta di comunicazione, ad esempio un socket o un'interfaccia RPC. Il server attende quindi che un client si connetta e richiedi il servizio. Il ruolo della sicurezza durante la configurazione della connessione è doppio nel caso dell'autenticazione reciproca:

-   Autenticazione client da parte del server.
-   Autenticazione server da parte del client.

I componenti client e server di un'applicazione di trasporto usano un pacchetto [*di sicurezza*](/windows/desktop/SecGloss/s-gly) per stabilire una connessione sicura per la trasmissione dei messaggi. Il primo passaggio per stabilire una connessione sicura consiste nel creare un [*contesto di sicurezza.*](/windows/desktop/SecGloss/s-gly) una struttura di dati opaca che contiene i dati di [](/windows/desktop/SecGloss/s-gly) sicurezza rilevanti per una connessione, ad esempio una chiave di sessione e la durata della sessione.

Un contesto di sicurezza è essenzialmente un messaggio dal pacchetto di sicurezza associato al client al pacchetto di sicurezza associato al server. Di conseguenza, la creazione di un contesto di sicurezza richiede in genere sia client che server per effettuare chiamate ai rispettivi pacchetti di sicurezza. Per altre informazioni sulle funzioni di contesto, vedere [Gestione del contesto](authentication-functions.md).

Il protocollo usato per stabilire una connessione protetta e autenticata comporta lo scambio di uno o più "token di sicurezza" tra il client e il server. Questi token vengono inviati come messaggi opachi dai due lati insieme a qualsiasi [*altra*](/windows/desktop/SecGloss/a-gly)informazione specifica del protocollo dell'applicazione. Come messaggio opaco, il token viene ricevuto da una funzione del pacchetto di sicurezza dal client, che non può interpretarlo o modificarlo, e inoltrato come messaggio al server. Il token è anche opaco per il server, che non può interpretare né modificare il token. Il server inoltra il token opaco al relativo pacchetto di sicurezza per l'interpretazione. Il pacchetto informa quindi il server dell'autenticazione client o dell'esito negativo dell'autenticazione.

Il client riceve il token del server in un messaggio, recupera il token dal messaggio ricevuto e lo usa in una chiamata al relativo pacchetto di sicurezza. Il client chiama quindi nuovamente il pacchetto di sicurezza che indica se è stata stabilita una connessione protetta o se sono necessari altri scambi prima che una connessione sicura sia pronta. In teoria, non è previsto alcun limite al numero di scambi di token di sicurezza necessari. In pratica, è necessario solo un numero limitato di scambi. L'autenticazione NTLM si basa sullo schema challenge/response e usa tre metodi per autenticare un client nel server. Il [*protocollo Kerberos*](/windows/desktop/SecGloss/k-gly) versione 5.0 può richiedere scambi di messaggi aggiuntivi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Inizializzazione del contesto client](client-context-initialization.md)
</dt> <dt>

[Inizializzazione del contesto del server](server-context-initialization.md)
</dt> </dl>

 

 
