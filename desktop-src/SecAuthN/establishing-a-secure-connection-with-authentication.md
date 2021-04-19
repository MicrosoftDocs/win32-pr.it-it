---
description: In un protocollo dell'applicazione client/server, un server viene associato a una porta di comunicazione, ad esempio un socket o un'interfaccia RPC.
ms.assetid: 176d4ca5-83dd-42ef-b116-227d4badc0dd
title: Stabilire una connessione protetta con l'autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a43483893c8dcf56e6db6b3c7d7aa1451bf9540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317084"
---
# <a name="establishing-a-secure-connection-with-authentication"></a>Stabilire una connessione protetta con l'autenticazione

In un [*protocollo dell'applicazione*](/windows/desktop/SecGloss/a-gly)client/server, un server viene associato a una porta di comunicazione, ad esempio un socket o un'interfaccia RPC. Il server attende quindi che un client si connetta e chieda il servizio. Il ruolo di sicurezza alla configurazione della connessione è due volte nel caso dell'autenticazione reciproca:

-   Autenticazione client da parte del server.
-   Autenticazione del server da parte del client.

I componenti client e server di un'applicazione di trasporto utilizzano un [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly) per stabilire una connessione sicura per la trasmissione dei messaggi. Il primo passaggio per stabilire una connessione sicura consiste nel creare un [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly). ovvero una struttura di dati opaca che contiene i dati di sicurezza relativi a una connessione, ad esempio una [*chiave di sessione*](/windows/desktop/SecGloss/s-gly) e la durata della sessione.

Un contesto di sicurezza è essenzialmente un messaggio del pacchetto di sicurezza associato al client al pacchetto di sicurezza associato al server. Di conseguenza, la creazione di un contesto di sicurezza richiede in genere sia il client che il server per effettuare chiamate ai rispettivi pacchetti di sicurezza. Per ulteriori informazioni sulle funzioni di contesto, vedere [gestione del contesto](authentication-functions.md).

Il protocollo utilizzato per stabilire una connessione autenticata protetta comporta lo scambio di uno o più "token di sicurezza" tra il client e il server. Questi token vengono inviati come messaggi opachi dai due lati insieme a qualsiasi altra informazione specifica del [*protocollo dell'applicazione*](/windows/desktop/SecGloss/a-gly). Come messaggio opaco, il token viene ricevuto da una funzione del pacchetto di sicurezza da parte del client, che non è in grado di interpretarla o modificarla e di inviarla come messaggio al server. Il token è anche opaco per il server, che non può interpretare né modificare il token. Il server invia il token opaco al relativo pacchetto di sicurezza per l'interpretazione. Il pacchetto informa quindi il server dell'autenticazione client o l'esito negativo dell'autenticazione.

Il client riceve il token del server in un messaggio, recupera il token dal messaggio ricevuto e utilizza tale token in una chiamata al relativo pacchetto di sicurezza. Il client chiama quindi di nuovo il pacchetto di sicurezza che indica se è stata stabilita una connessione protetta o se sono necessari altri scambi prima che una connessione protetta sia pronta. In teoria, non esiste alcun limite al numero di scambi di token di sicurezza necessari. In pratica, è necessario solo un numero limitato di scambi. L'autenticazione NTLM è basata sullo schema di richiesta/risposta e utilizza tre gambe per autenticare un client nel server. Il protocollo [*Kerberos*](/windows/desktop/SecGloss/k-gly) versione 5,0 può richiedere scambi di messaggi aggiuntivi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Inizializzazione del contesto client](client-context-initialization.md)
</dt> <dt>

[Inizializzazione del contesto server](server-context-initialization.md)
</dt> </dl>

 

 
