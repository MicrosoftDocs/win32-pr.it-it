---
title: Autenticazione reciproca in un servizio Windows Sockets con SCP
description: Negli argomenti di questa sezione sono inclusi esempi di codice in cui viene illustrato come eseguire l'autenticazione reciproca con un servizio che pubblica se stesso utilizzando un punto di connessione del servizio (SCP).
ms.assetid: f730464c-95ac-4285-960c-18862f6f7852
ms.tgt_platform: multiple
keywords:
- Autenticazione reciproca in un servizio Windows Sockets con un annuncio SCP
- Active Directory, utilizzo di, autenticazione reciproca, servizio Windows Sockets con SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527715c4a35dc15cd67f5820e6fa891b56452399
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872289"
---
# <a name="mutual-authentication-in-a-windows-sockets-service-with-scp"></a>Autenticazione reciproca in un servizio Windows Sockets con SCP

Negli argomenti di questa sezione sono inclusi esempi di codice in cui viene illustrato come eseguire l'autenticazione reciproca con un servizio che pubblica se stesso utilizzando un punto di connessione del servizio (SCP). Gli esempi si basano su un servizio Microsoft Windows Sockets che utilizza un pacchetto SSPI per gestire la negoziazione di autenticazione reciproca tra un client e il servizio. Utilizzare le procedure seguenti per implementare l'autenticazione reciproca all'interno di questo scenario.

**Per registrare i nomi SPN in una directory durante l'installazione di un servizio**

1.  Chiamare la funzione [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) per comporre i nomi dell'entità servizio (SPN) per il servizio.
2.  Chiamare la funzione [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) per registrare i nomi SPN nell'account del servizio o nel computer in cui viene eseguito il servizio. Questo passaggio deve essere eseguito da un amministratore di dominio. un'eccezione è che un servizio in esecuzione con l'account LocalSystem può registrare il proprio SPN nel formato " <service class> / <host> " nell'account computer dell'host del servizio.

**Per verificare la configurazione all'avvio del servizio**

-   Verificare che i nomi SPN appropriati siano registrati nell'account con cui è in esecuzione il servizio. Per altre informazioni, vedere [attività di manutenzione degli account di accesso](logon-account-maintenance-tasks.md).

**Per autenticare il servizio all'avvio del client**

1.  Recuperare i dati di connessione dal punto di connessione del servizio del servizio.
2.  Stabilire una connessione al servizio.
3.  Chiamare la funzione [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) per comporre un nome SPN per il servizio. Comporre il nome SPN dalla stringa di classe del servizio nota e i dati recuperati dal punto di connessione del servizio. Questi dati includono il nome host del server in cui è in esecuzione il servizio. Tenere presente che il nome host deve essere un nome DNS.
4.  Usare un pacchetto di sicurezza SSPI per eseguire l'autenticazione:
    1.  Chiamare la funzione [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) per acquisire le credenziali del client.
    2.  Passare le credenziali client e il nome SPN alla funzione [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) per generare un BLOB di sicurezza da inviare al servizio per l'autenticazione. Impostare il flag di autenticazione **\_ \_ reciproca \_ di ISC** per richiedere l'autenticazione reciproca.
    3.  Scambiare i BLOB con il servizio fino al completamento dell'autenticazione.
5.  Verificare la maschera delle funzionalità restituita per il flag di autenticazione **\_ \_ reciproca \_ di ISC req** per verificare che sia stata eseguita l'autenticazione reciproca.
6.  Se l'autenticazione ha avuto esito positivo, scambiare il traffico con il servizio autenticato. Usare la firma digitale per assicurarsi che i messaggi tra il client e il servizio non siano stati manomessi. A meno che i requisiti di prestazioni non siano gravi, utilizzare la crittografia. Per ulteriori informazioni e un esempio di codice in cui viene illustrato come utilizzare le funzioni [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature), [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature), [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)e [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) in un pacchetto SSPI, vedere [garantire l'integrità della comunicazione durante lo scambio di messaggi](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).

**Per autenticare il client dal servizio quando si connette un client**

1.  Caricare un pacchetto di sicurezza SSPI che supporti l'autenticazione reciproca.
2.  Quando un client si connette, usare il pacchetto di sicurezza per eseguire l'autenticazione:
    1.  Chiamare la funzione [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) per acquisire le credenziali del servizio.
    2.  Passare le credenziali del servizio e il BLOB di sicurezza ricevuti dal client alla funzione [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) per generare un BLOB di sicurezza da restituire al client.
    3.  Scambiare i BLOB con il client fino al completamento dell'autenticazione.
3.  Per verificare che sia stata eseguita l'autenticazione reciproca, controllare la maschera delle funzionalità restituita per il flag **ASC \_ ret \_ reciproal \_ AUTH** .
4.  Se l'autenticazione ha avuto esito positivo, scambiare il traffico con il client autenticato. Usare la firma digitale e la crittografia, a meno che le prestazioni non siano un problema.

Per ulteriori informazioni e un esempio di codice per questo scenario di autenticazione reciproca, vedere:

-   [Come un client autentica un servizio Windows Sockets basato su SCP](how-a-client-authenticates-an-scp-based-windows-sockets-service.md)
-   [Composizione e registrazione di nomi SPN per un servizio Windows Sockets basato su SCP](composing-and-registering-spns-for-an-scp-based-windows-sockets-service.md)
-   [Modalità di autenticazione di un client in un servizio Windows Sockets](how-a-windows-sockets-service-authenticates-a-client.md)

Per altre informazioni, vedere:

-   [Pubblicazione con i punti di connessione del servizio](publishing-with-service-connection-points.md)
-   [Documentazione di SSPI](/windows/desktop/SecAuthN/sspi)
-   [Documentazione di Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)

 

 