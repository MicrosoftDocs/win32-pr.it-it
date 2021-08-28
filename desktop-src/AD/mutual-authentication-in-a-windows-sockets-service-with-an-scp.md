---
title: Autenticazione reciproca in un Windows Sockets con SCP
description: Negli argomenti di questa sezione sono inclusi esempi di codice che illustrano come eseguire l'autenticazione reciproca con un servizio che si pubblica tramite un punto di connessione del servizio.
ms.assetid: f730464c-95ac-4285-960c-18862f6f7852
ms.tgt_platform: multiple
keywords:
- Autenticazione reciproca in un Windows Sockets con SCP AD
- Active Directory, uso, autenticazione reciproca, Windows socket con un SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ede3f05744e402cb483e46d6eb116f653e20d9e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881380"
---
# <a name="mutual-authentication-in-a-windows-sockets-service-with-scp"></a>Autenticazione reciproca in un Windows Sockets con SCP

Negli argomenti di questa sezione sono inclusi esempi di codice che illustrano come eseguire l'autenticazione reciproca con un servizio che si pubblica tramite un punto di connessione del servizio. Gli esempi sono basati su un servizio Microsoft Windows Sockets che usa un pacchetto SSPI per gestire la negoziazione di autenticazione reciproca tra un client e il servizio. Utilizzare le procedure seguenti per implementare l'autenticazione reciproca all'interno di questo scenario.

**Per registrare i nomi SPN in una directory quando viene installato un servizio**

1.  Chiamare la [**funzione DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) per comporre i nomi dell'entità servizio (SPN) per il servizio.
2.  Chiamare la [**funzione DsWriteAccountSpn per**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) registrare i nomi SPN nell'account del servizio o nell'account computer nel cui contesto verrà eseguito il servizio. Questo passaggio deve essere eseguito da un amministratore di dominio. un'eccezione è che un servizio in esecuzione con l'account LocalSystem può registrare il proprio nome SPN nel formato " host " <service class> / &lt; nell'account &gt; computer dell'host del servizio.

**Per verificare la configurazione all'avvio del servizio**

-   Verificare che i nomi SPN appropriati siano registrati nell'account con cui è in esecuzione il servizio. Per altre informazioni, vedere [Attività di manutenzione dell'account di accesso.](logon-account-maintenance-tasks.md)

**Per autenticare il servizio all'avvio del client**

1.  Recuperare i dati di connessione dal punto di connessione del servizio.
2.  Stabilire una connessione al servizio.
3.  Chiamare la [**funzione DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) per comporre un nome SPN per il servizio. Comporre il nome SPN dalla stringa della classe del servizio nota e i dati recuperati dal punto di connessione del servizio. Questi dati includono il nome host del server in cui è in esecuzione il servizio. Tenere presente che il nome host deve essere un nome DNS.
4.  Usare un pacchetto di sicurezza SSPI per eseguire l'autenticazione:
    1.  Chiamare la [**funzione AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) per acquisire le credenziali del client.
    2.  Passare le credenziali client e il nome SPN alla funzione [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) per generare un BLOB di sicurezza da inviare al servizio per l'autenticazione. Impostare il flag **ISC \_ REQ \_ MUTUAL \_ AUTH** per richiedere l'autenticazione reciproca.
    3.  Exchange blob con il servizio fino al completamento dell'autenticazione.
5.  Verificare la maschera delle funzionalità restituita per il flag **ISC \_ REQ \_ MUTUAL \_ AUTH** per verificare che sia stata eseguita l'autenticazione reciproca.
6.  Se l'autenticazione ha avuto esito positivo, scambiare il traffico con il servizio autenticato. Usare la firma digitale per assicurarsi che i messaggi tra client e servizio non siano stati manomissionati. A meno che i requisiti di prestazioni non siano gravi, usare la crittografia. Per altre informazioni e un esempio di codice che illustra come usare le funzioni [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature), [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature), [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)e [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) in un pacchetto SSPI, vedere Ensuring [Communication Integrity During Message Exchange](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).

**Per autenticare il client dal servizio quando un client si connette**

1.  Caricare un pacchetto di sicurezza SSPI che supporta l'autenticazione reciproca.
2.  Quando un client si connette, usare il pacchetto di sicurezza per eseguire l'autenticazione:
    1.  Chiamare la [**funzione AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) per acquisire le credenziali del servizio.
    2.  Passare le credenziali del servizio e il BLOB di sicurezza ricevuto dal client alla funzione [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) per generare un BLOB di sicurezza da inviare al client.
    3.  Exchange blob con il client fino al completamento dell'autenticazione.
3.  Controllare la maschera delle funzionalità restituita per il flag **ASC \_ RET \_ MUTUAL \_ AUTH** per verificare che sia stata eseguita l'autenticazione reciproca.
4.  Se l'autenticazione ha avuto esito positivo, scambiare il traffico con il client autenticato. Usare la firma digitale e la crittografia, a meno che le prestazioni non siano un problema.

Per altre informazioni e un esempio di codice per questo scenario di autenticazione reciproca, vedere:

-   [Come un client autentica un servizio Sockets Windows SCP](how-a-client-authenticates-an-scp-based-windows-sockets-service.md)
-   [Composizione e registrazione di nomi SPN per un servizio Windows Sockets basato su SCP](composing-and-registering-spns-for-an-scp-based-windows-sockets-service.md)
-   [Come un Windows Sockets autentica un client](how-a-windows-sockets-service-authenticates-a-client.md)

Per altre informazioni, vedere:

-   [Pubblicazione con punti di connessione del servizio](publishing-with-service-connection-points.md)
-   [Documentazione di SSPI](/windows/desktop/SecAuthN/sspi)
-   [Windows Documentazione dei socket](/windows/desktop/WinSock/windows-sockets-start-page-2)

 

 
