---
description: Protocollo di accesso digest
ms.assetid: 7b2fd75e-dd0d-4a63-a84b-a64f08f883f2
title: Protocollo di accesso digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86aa8f05580c27c866c0568dbc67c4d5ba5c2016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555662"
---
# <a name="the-digest-access-protocol"></a>Protocollo di accesso digest

Il protocollo di accesso digest specificato da [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt) viene implementato dal Microsoft Digest [*Security Support Provider*](../secgloss/s-gly.md) (SSP). L'implementazione di è costituita da un set di funzioni del contesto di sicurezza di [Microsoft Security Support Provider Interface](sspi.md) (SSPI) a cui le applicazioni client/server chiamano:

-   Stabilire un [*contesto di sicurezza*](../secgloss/s-gly.md) per lo scambio di messaggi.
-   Ottenere gli oggetti dati richiesti dall'SSP digest, ad esempio le [*credenziali*](../secgloss/c-gly.md) e gli handle di contesto.
-   Accedere ai meccanismi di [*integrità*](../secgloss/i-gly.md) e riservatezza dei messaggi.

L'autenticazione dell'accesso al digest avviene all'interno di transazioni di richiesta/risposta abbinate, con richieste provenienti dal client e risposte provenienti dal server. Una corretta autenticazione dell'accesso digest richiede due coppie di richiesta/risposta.

Quando il provider di servizi condivisi del digest viene usato per l'autenticazione HTTP, non viene mantenuta alcuna connessione tra la prima e la seconda coppia richiesta-risposta. In altre parole, il server non attende la seconda richiesta dopo l'invio della prima risposta.

Nella figura seguente vengono illustrati i passaggi eseguiti sul percorso HTTP da un client e un server per completare un'autenticazione utilizzando il provider di servizi condivisi del digest. Il meccanismo SASL usa l'autenticazione reciproca, quindi i dati di autenticazione vengono restituiti alla chiamata finale al server ASC al client che verifica che il client stia comunicando con il server corretto.

![protocollo di accesso digest](images/digest1.png)

Il processo inizia con il client che richiede una risorsa protetta dall'accesso dal server inviando la richiesta HTTP 1.

Il server riceve la richiesta HTTP 1 e determina che la risorsa richiede informazioni di autenticazione che non sono state incluse nella richiesta. Il server genera una richiesta di verifica per il client nel modo seguente:

1.  Il server ottiene le proprie [*credenziali*](../secgloss/c-gly.md) chiamando la funzione [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .
2.  Il server genera la richiesta di digest chiamando la funzione [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .
3.  Il server invia un'intestazione WWW-Authenticate come risposta alla richiesta del client (visualizzata come risposta HTTP 1). L'intestazione contiene la richiesta digest e una direttiva opaca che contiene un riferimento a un [*contesto di sicurezza*](../secgloss/s-gly.md) parziale stabilito per il client. L'intestazione viene inviata con un codice di stato 401 che indica che la richiesta client ha generato un errore di accesso non autorizzato. Per ulteriori informazioni sulla richiesta di digest, vedere [contenuto di una richiesta di digest](contents-of-a-digest-challenge.md) e [generazione della richiesta di digest](generating-the-digest-challenge.md).
4.  Il client riceve la risposta HTTP 1, estrae la richiesta digest inviata dal server e genera una risposta di richiesta digest nel modo seguente:
    1.  Le credenziali dell'utente vengono ottenute chiamando la funzione [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) o richiedendo in modo interattivo all'utente di specificare le credenziali.
    2.  Le informazioni sulla richiesta di verifica e sulle credenziali vengono passate alla funzione [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) , che genera la risposta alla richiesta di verifica del digest.
5.  Il client invia un'intestazione di autorizzazione che contiene la risposta di richiesta al server (visualizzata come richiesta HTTP 2). Per ulteriori informazioni sulla risposta di verifica del digest, vedere il [contenuto di una risposta di verifica del digest](contents-of-a-digest-challenge-response.md) e [generazione della risposta di verifica del digest](generating-the-digest-challenge-response.md).
6.  Il server riceve la richiesta HTTP 2, estrae la risposta alla richiesta di verifica inviata dal client e autentica le informazioni chiamando la funzione [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Per informazioni dettagliate sul processo di autenticazione, vedere [autenticazione iniziale con Microsoft Digest](initial-authentication-using-microsoft-digest.md).
7.  Il server invia la risposta HTTP 2 di nuovo al client come seconda e ultima risposta richiesta dal protocollo di accesso digest. Se l'autenticazione ha esito positivo, questa risposta contiene la risorsa richiesta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contenuto di una risposta di richiesta digest](contents-of-a-digest-challenge-response.md)
</dt> </dl>

 

 
