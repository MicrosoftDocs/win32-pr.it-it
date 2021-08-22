---
description: Protocollo di accesso digest
ms.assetid: 7b2fd75e-dd0d-4a63-a84b-a64f08f883f2
title: Protocollo di accesso digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45fea65fc25df87ef434e7bfea5cb81690cdc06f82b72882438fe4475a1895b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916435"
---
# <a name="the-digest-access-protocol"></a>Protocollo di accesso digest

Il protocollo di accesso digest specificato [da RFC 2617](https://www.ietf.org/rfc/rfc2617.txt) viene implementato dal Microsoft Digest [*security support provider*](../secgloss/s-gly.md) (SSP). L'implementazione è costituita da un set di funzioni del contesto di sicurezza SSPI [(Microsoft Security Support Provider Interface)](sspi.md) chiamate dalle applicazioni client/server a:

-   Stabilire un contesto [*di sicurezza per*](../secgloss/s-gly.md) lo scambio di messaggi.
-   Ottenere gli oggetti dati richiesti dal provider di servizi di configurazione digest, ad esempio [*credenziali*](../secgloss/c-gly.md) e handle di contesto.
-   Accedere ai meccanismi [*di*](../secgloss/i-gly.md) integrità e riservatezza dei messaggi.

L'autenticazione dell'accesso digest avviene all'interno di transazioni di richiesta/risposta abbinate, con richieste provenienti dal client e risposte originate nel server. Per una corretta autenticazione dell'accesso al digest sono necessarie due coppie di richiesta/risposta.

Quando il provider di servizi di elaborazione digest viene usato per l'autenticazione HTTP, non viene mantenuta alcuna connessione tra la prima e la seconda coppia richiesta/risposta. In altre parole, il server non attende la seconda richiesta dopo l'invio della prima risposta.

La figura seguente illustra la procedura eseguita nel percorso HTTP da un client e un server per completare un'autenticazione usando il provider di servizi di configurazione digest. Il meccanismo SASL usa l'autenticazione reciproca, quindi i dati di autenticazione vengono inviati alla chiamata finale del server del Certificato del servizio di sicurezza al client che verifica che il client comunichi con il server corretto.

![protocollo di accesso digest](images/digest1.png)

Il processo inizia con il client che richiede una risorsa protetta da accesso al server inviando la richiesta HTTP 1.

Il server riceve la richiesta HTTP 1 e determina che la risorsa richiede informazioni di autenticazione non incluse nella richiesta. Il server genera una richiesta per il client come indicato di seguito:

1.  Il server ottiene le [*credenziali*](../secgloss/c-gly.md) chiamando la [**funzione AcquireCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)
2.  Il server genera la richiesta digest chiamando la [**funzione AcceptSecurityContext (General).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
3.  Il server invia unWWW-Authenticate di intestazione come risposta alla richiesta del client (visualizzata come risposta HTTP 1). L'intestazione contiene la richiesta digest e una direttiva opaca che contiene un riferimento a un contesto di [*sicurezza*](../secgloss/s-gly.md) parziale stabilito per il client. L'intestazione viene inviata con un codice di stato 401 che indica che la richiesta client ha generato un errore di accesso non autorizzato. Per altre informazioni sulla richiesta di digest, vedere [Contenuto di una](contents-of-a-digest-challenge.md) richiesta di digest e Generazione della richiesta di [digest.](generating-the-digest-challenge.md)
4.  Il client riceve la risposta HTTP 1, estrae la richiesta di digest inviata dal server e genera una risposta di richiesta digest come segue:
    1.  Le credenziali dell'utente vengono ottenute chiamando la funzione [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) o richiedendo in modo interattivo le credenziali all'utente.
    2.  Le informazioni relative alla richiesta di verifica e alle credenziali vengono passate alla [**funzione InitializeSecurityContext (Generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) che genera la risposta alla richiesta di verifica digest.
5.  Il client invia un'intestazione Authorization che contiene la risposta alla richiesta di verifica al server (visualizzata come richiesta HTTP 2). Per altre informazioni sulla risposta alla richiesta di digest, vedere [Contenuto di una](contents-of-a-digest-challenge-response.md) risposta alla richiesta di digest e Generazione della risposta alla richiesta di [digest.](generating-the-digest-challenge-response.md)
6.  Il server riceve la richiesta HTTP 2, estrae la risposta di richiesta inviata dal client e autentica le informazioni chiamando la funzione [**AcceptSecurityContext (Generale).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) Per informazioni dettagliate sul processo di autenticazione, vedere [Autenticazione iniziale con Microsoft Digest](initial-authentication-using-microsoft-digest.md).
7.  Il server invia la risposta HTTP 2 al client come seconda e ultima risposta richiesta dal protocollo di accesso digest. Se l'autenticazione ha esito positivo, questa risposta contiene la risorsa richiesta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contenuto di una risposta alla richiesta di digest](contents-of-a-digest-challenge-response.md)
</dt> </dl>

 

 
