---
description: Elenca i pacchetti di sicurezza che possono essere utilizzati con SSPI.
ms.assetid: f5999d41-b334-49be-8883-d9b9042d20dc
title: Uso dei pacchetti di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9253ee2ac4cec98e3c68a1f3dab80a71b216e6235af78722864ee0e0958897c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915193"
---
# <a name="using-security-packages"></a>Uso dei pacchetti di sicurezza

È [*possibile usare Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) con i pacchetti di sicurezza [*seguenti:*](../secgloss/s-gly.md)

-   [Pacchetto di sicurezza Kerberos](#kerberos-security-package)
-   [Pacchetto di sicurezza NTLM](#ntlm-security-package)

I [*protocolli Kerberos*](../secgloss/k-gly.md) e NTLM vengono implementati come pacchetti di sicurezza dal Secur32.dll Security Support [*Provider*](../secgloss/s-gly.md) (SSP) fornito con il sistema operativo. Per impostazione predefinita, il supporto per l'autenticazione [](../secgloss/l-gly.md) Kerberos e NTLM viene caricato dall'autorità di sicurezza locale (LSA) in un computer all'avvio del sistema. In Windows Server o Windows, entrambi i pacchetti possono essere usati per autenticare gli accessi alla rete e le connessioni client/server. Quale viene usato dipende dalle funzionalità del computer sull'altro lato della connessione. Il protocollo Kerberos è sempre preferibile, se disponibile.

Dopo aver stabilito un contesto di sicurezza per un utente interattivo, un'altra istanza del pacchetto Kerberos o NTLM può essere caricata da un processo in esecuzione nel contesto di sicurezza dell'utente per supportare lo scambio, la firma, la verifica, la crittografia e la decrittografia dei messaggi. Tuttavia, nessun processo diverso dall'LSA è mai autorizzato ad accedere alle chiavi di sessione o [*ai*](../secgloss/s-gly.md) ticket nella cache delle credenziali.

I servizi di sistema e le applicazioni a livello di trasporto accedono a un SSP tramite SSPI, che fornisce funzioni per l'enumerazione dei pacchetti di sicurezza disponibili in un sistema, la selezione di un pacchetto e l'utilizzo di tale pacchetto per ottenere una connessione autenticata.

I metodi in SSPI sono routine generiche che gli sviluppatori possono usare senza conoscere i dettagli di un particolare protocollo [*di sicurezza.*](../secgloss/s-gly.md) Ad esempio, quando viene autenticata una connessione client/server:

1.  L'applicazione sul lato client [](../secgloss/c-gly.md) della connessione invia le credenziali al server usando la funzione SSPI [**InitializeSecurityContext (Generale).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
2.  L'applicazione sul lato server della connessione risponde con la funzione SSPI [**AcceptSecurityContext (Generale).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
3.  Dopo l'autenticazione della connessione, l'indirizzo LSA sul server usa le informazioni del client per creare un [*token di accesso*](../secgloss/a-gly.md).
4.  Il server può quindi chiamare la funzione SSPI [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) per collegare il token di accesso a un thread di rappresentazione per il servizio.

## <a name="kerberos-security-package"></a>Pacchetto di sicurezza Kerberos

Il pacchetto [*di sicurezza Kerberos*](../secgloss/s-gly.md) è basato sul protocollo di autenticazione [*Kerberos*](../secgloss/k-gly.md).

Se il protocollo Kerberos viene usato per autenticare una connessione client/server, [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) genera un messaggio GSSAPI che include un messaggio REQ AP KRB \_ \_ dal client. [**AcceptSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) genera quindi un messaggio GSSAPI che include un messaggio \_ KRB AP \_ REP dal server.

Per informazioni di base sui passaggi che si svolgono dietro le quinte nell'implementazione di un protocollo Kerberos, vedere [Microsoft Kerberos.](microsoft-kerberos.md)

Tutti i servizi distribuiti usano SSPI per accedere al protocollo Kerberos. Un elenco parziale dei modi in cui il protocollo Kerberos viene usato per l'autenticazione include:

-   Servizi dello spooler di stampa
-   Accesso remoto ai file CIFS/SMB
-   [*Query LDAP*](../secgloss/l-gly.md) in Active Directory
-   Gestione file system e segnalazioni distribuite
-   Autenticazione dell'autorità di sicurezza da host a host IPsec
-   Richieste di prenotazione per la qualità del servizio di rete
-   Autenticazione Intranet per Internet Information Services
-   Gestione remota di server o workstation tramite RPC autenticato
-   [*Richieste di certificati*](../secgloss/c-gly.md) a Servizi certificati per utenti e computer di dominio

## <a name="ntlm-security-package"></a>Pacchetto di sicurezza NTLM

Il pacchetto di sicurezza NTLM è basato sul protocollo di autenticazione NTLM.

 

 
