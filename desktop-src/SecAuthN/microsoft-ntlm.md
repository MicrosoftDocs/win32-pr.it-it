---
description: Windows Challenge/Response (NTLM) è il protocollo di autenticazione utilizzato nelle reti che includono sistemi che eseguono il sistema operativo Windows e su sistemi autonomi.
ms.assetid: 35a38858-d36f-45c9-95f4-2541a182f5ac
title: Microsoft NTLM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9723f24d5913adefe70d4e238de0591790a34bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525861"
---
# <a name="microsoft-ntlm"></a>Microsoft NTLM

Windows Challenge/Response (NTLM) è il protocollo di autenticazione utilizzato nelle reti che includono sistemi che eseguono il sistema operativo Windows e su sistemi autonomi.

Il [*pacchetto di protezione*](../secgloss/s-gly.md) [*Kerberos*](../secgloss/k-gly.md) Microsoft aggiunge maggiore sicurezza rispetto a NTLM ai sistemi in una rete. Sebbene Microsoft *Kerberos* sia il protocollo preferito, NTLM è ancora supportato. È necessario utilizzare NTLM anche per l'autenticazione di accesso nei sistemi autonomi. Per ulteriori informazioni su Kerberos, vedere [Microsoft Kerberos](microsoft-kerberos.md).

Le credenziali NTLM sono basate sui dati ottenuti durante il processo di accesso interattivo e sono costituite da un nome di dominio, un nome utente e un [*hash*](../secgloss/h-gly.md) unidirezionale della password dell'utente. NTLM usa un protocollo di richiesta/risposta crittografato per autenticare un utente senza inviare la password dell'utente attraverso la rete. Al contrario, il sistema che richiede l'autenticazione deve eseguire un calcolo che dimostri che ha accesso alle credenziali NTLM protette.

L'autenticazione NTLM interattiva in una rete prevede in genere due sistemi: un sistema client, dove l'utente richiede l'autenticazione e un controller di dominio, in cui vengono mantenute le informazioni relative alla password dell'utente. Autenticazione non interattiva, che può essere necessaria per consentire a un utente già connesso di accedere a una risorsa, ad esempio un'applicazione server, in genere comprende tre sistemi: un client, un server e un controller di dominio che esegue i calcoli di autenticazione per conto del server.

I passaggi seguenti presentano una struttura dell'autenticazione non interattiva NTLM. Il primo passaggio fornisce le credenziali NTLM dell'utente e si verifica solo come parte del processo di autenticazione interattiva (accesso).

1.  (Solo autenticazione interattiva) Un utente accede a un computer client e fornisce un nome di dominio, un nome utente e una password. Il client calcola un [*hash*](../secgloss/h-gly.md) crittografico della password ed elimina la password effettiva.
2.  Il client invia il nome utente al server (in [*testo non crittografato*](../secgloss/p-gly.md)).
3.  Il server genera un numero casuale a 16 byte, denominato *Challenge* o [*nonce*](../secgloss/n-gly.md), e lo invia al client.
4.  Il client crittografa questa richiesta con l'hash della password dell'utente e restituisce il risultato al server. Questa operazione viene chiamata *risposta*.
5.  Il server invia i seguenti tre elementi al controller di dominio:

    -   Nome utente
    -   Richiesta di verifica inviata al client
    -   Risposta ricevuta dal client

6.  Il controller di dominio utilizza il nome utente per recuperare l'hash della password dell'utente dal database di gestione account di sicurezza. Usa questo hash della password per crittografare la richiesta.
7.  Il controller di dominio confronta la richiesta crittografata calcolata (nel passaggio 6) con la risposta calcolata dal client (nel passaggio 4). Se sono identici, l'autenticazione ha esito positivo.

L'applicazione non deve accedere direttamente al [*pacchetto di sicurezza*](../secgloss/s-gly.md) NTLM. deve invece usare il pacchetto di sicurezza [*Negotiate*](../secgloss/n-gly.md) . Negotiate consente all'applicazione di sfruttare i protocolli di [*sicurezza*](../secgloss/s-gly.md) più avanzati se sono supportati dai sistemi interessati dall'autenticazione. Attualmente, il pacchetto di sicurezza Negotiate seleziona tra [*Kerberos*](../secgloss/k-gly.md) e NTLM. Negotiate seleziona Kerberos a meno che non possa essere usato da uno dei sistemi interessati dall'autenticazione.

 

 
