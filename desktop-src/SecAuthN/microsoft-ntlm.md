---
description: Windows Challenge/Response (NTLM) è il protocollo di autenticazione usato nelle reti che includono sistemi che eseguono Windows sistema operativo e nei sistemi autonomi.
ms.assetid: 35a38858-d36f-45c9-95f4-2541a182f5ac
title: Microsoft NTLM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcb3d7f272c831c6bf9ac5efd30b8fa67bc7ad27d78d43794e5110fb63d1fe49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921692"
---
# <a name="microsoft-ntlm"></a>Microsoft NTLM

Windows Challenge/Response (NTLM) è il protocollo di autenticazione usato nelle reti che includono sistemi che eseguono Windows sistema operativo e nei sistemi autonomi.

Il pacchetto [*di sicurezza Microsoft Kerberos*](../secgloss/k-gly.md) [](../secgloss/s-gly.md) aggiunge maggiore sicurezza rispetto a NTLM ai sistemi in una rete. Anche se *Microsoft Kerberos* è il protocollo preferito, NTLM è ancora supportato. È necessario usare NTLM anche per l'autenticazione di accesso nei sistemi autonomi. Per altre informazioni su Kerberos, vedere [Microsoft Kerberos](microsoft-kerberos.md).

Le credenziali NTLM si basano sui dati ottenuti durante il processo di accesso interattivo e sono costituite da un nome di dominio, un nome utente e un [*hash*](../secgloss/h-gly.md) unidiredireale della password dell'utente. NTLM usa un protocollo challenge/response crittografato per autenticare un utente senza inviare la password dell'utente in transito. Il sistema che richiede l'autenticazione deve invece eseguire un calcolo che dimostra di avere accesso alle credenziali NTLM protette.

L'autenticazione NTLM interattiva su una rete include in genere due sistemi: un sistema client, in cui l'utente richiede l'autenticazione, e un controller di dominio, in cui vengono conservate le informazioni relative alla password dell'utente. L'autenticazione non interattiva, che può essere necessaria per consentire a un utente già connesso di accedere a una risorsa, ad esempio un'applicazione server, prevede in genere tre sistemi: un client, un server e un controller di dominio che esegue i calcoli di autenticazione per conto del server.

La procedura seguente illustra una struttura dell'autenticazione NTLM non interattiva. Il primo passaggio fornisce le credenziali NTLM dell'utente e si verifica solo come parte del processo di autenticazione interattiva (accesso).

1.  (solo autenticazione interattiva) Un utente accede a un computer client e fornisce un nome di dominio, un nome utente e una password. Il client calcola un [*hash*](../secgloss/h-gly.md) crittografico della password e rimuove la password effettiva.
2.  Il client invia il nome utente al server (in [*testo non crittografato).*](../secgloss/p-gly.md)
3.  Il server genera un numero casuale a 16 byte, denominato *challenge* o [*nonce,*](../secgloss/n-gly.md)e lo invia al client.
4.  Il client crittografa questa richiesta con l'hash della password dell'utente e restituisce il risultato al server. Questa operazione è denominata *risposta*.
5.  Il server invia i tre elementi seguenti al controller di dominio:

    -   Nome utente
    -   Richiesta di richiesta inviata al client
    -   Risposta ricevuta dal client

6.  Il controller di dominio usa il nome utente per recuperare l'hash della password dell'utente dal database di Security Account Manager. Usa questo hash della password per crittografare la richiesta.
7.  Il controller di dominio confronta la richiesta crittografata calcolata (nel passaggio 6) con la risposta calcolata dal client (nel passaggio 4). Se sono identici, l'autenticazione ha esito positivo.

L'applicazione non deve accedere direttamente al pacchetto di [*sicurezza*](../secgloss/s-gly.md) NTLM. deve invece usare il pacchetto di sicurezza [*Negotiate.*](../secgloss/n-gly.md) Negotiate consente all'applicazione di sfruttare i protocolli [*di*](../secgloss/s-gly.md) sicurezza più avanzati se sono supportati dai sistemi coinvolti nell'autenticazione. Attualmente, il pacchetto di sicurezza Negotiate seleziona tra [*Kerberos*](../secgloss/k-gly.md) e NTLM. Negotiate seleziona Kerberos a meno che non possa essere usato da uno dei sistemi coinvolti nell'autenticazione.

 

 
