---
description: Elenca i pacchetti di sicurezza che possono essere utilizzati con SSPI.
ms.assetid: f5999d41-b334-49be-8883-d9b9042d20dc
title: Uso dei pacchetti di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df24bba0f910ba74a633e8a43f961cee4fb505db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315854"
---
# <a name="using-security-packages"></a>Uso dei pacchetti di sicurezza

[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) può essere utilizzato con i seguenti [*pacchetti di sicurezza*](../secgloss/s-gly.md):

-   [Pacchetto di sicurezza Kerberos](#kerberos-security-package)
-   [Pacchetto di sicurezza NTLM](#ntlm-security-package)

I protocolli [*Kerberos*](../secgloss/k-gly.md) e NTLM vengono implementati come pacchetti di sicurezza da Secur32.dll [*Security Support Provider*](../secgloss/s-gly.md) (SSP) forniti con il sistema operativo. Per impostazione predefinita, il supporto per l'autenticazione Kerberos e NTLM viene caricato dall' [*autorità di sicurezza locale*](../secgloss/l-gly.md) (LSA) in un computer all'avvio del sistema. Nei domini Windows Server o Windows, è possibile usare entrambi i pacchetti per autenticare gli accessi di rete e le connessioni client/server. Quello utilizzato dipende dalle funzionalità del computer sull'altro lato della connessione. Il protocollo Kerberos è sempre preferito, se disponibile.

Dopo che è stato stabilito un contesto di sicurezza per un utente interattivo, un'altra istanza del pacchetto Kerberos o NTLM può essere caricata da un processo in esecuzione nel contesto di sicurezza dell'utente per supportare lo scambio, la firma, la verifica, la crittografia e la decrittografia dei messaggi. Tuttavia, non è consentito l'accesso alle chiavi o ai ticket della [*sessione*](../secgloss/s-gly.md) nella cache delle credenziali.

I servizi di sistema e le applicazioni a livello di trasporto accedono a un SSP tramite SSPI, che fornisce funzioni per l'enumerazione dei pacchetti di sicurezza disponibili in un sistema, la selezione di un pacchetto e l'utilizzo di tale pacchetto per ottenere una connessione autenticata.

I metodi in SSPI sono routine generiche che possono essere utilizzate dagli sviluppatori senza conoscere i dettagli di un particolare [*protocollo di sicurezza*](../secgloss/s-gly.md). Ad esempio, quando viene autenticata una connessione client/server:

1.  L'applicazione sul lato client della connessione Invia le [*credenziali*](../secgloss/c-gly.md) al server utilizzando la funzione SSPI [**InitializeSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).
2.  L'applicazione sul lato server della connessione risponde con la funzione SSPI [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).
3.  Dopo che la connessione è stata autenticata, l'LSA sul server utilizza le informazioni del client per compilare un [*token di accesso*](../secgloss/a-gly.md).
4.  Il server può quindi chiamare la funzione SSPI [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) per alleghiare il token di accesso a un thread di rappresentazione per il servizio.

## <a name="kerberos-security-package"></a>Pacchetto di sicurezza Kerberos

Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) Kerberos è basato sul [*protocollo di autenticazione Kerberos*](../secgloss/k-gly.md).

Se il protocollo Kerberos viene utilizzato per autenticare una connessione client/server, [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) genera un messaggio GSSAPI che include un \_ \_ messaggio di KRB AP REQ dal client. [**AcceptSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) genera quindi un messaggio GSSAPI che include un \_ \_ messaggio di KRB AP Rep dal server.

Per informazioni generali sui passaggi che si verificano in background nell'implementazione di un protocollo Kerberos, vedere [Microsoft Kerberos](microsoft-kerberos.md).

Tutti i servizi distribuiti utilizzano SSPI per accedere al protocollo Kerberos. Un elenco parziale delle modalità di utilizzo del protocollo Kerberos per l'autenticazione include:

-   Servizi spooler di stampa
-   Accesso al file remoto CIFS/SMB
-   Query [*LDAP*](../secgloss/l-gly.md) al Active Directory
-   Gestione file system distribuita e riferimenti
-   Autenticazione dell'autorità di sicurezza da host a host IPsec
-   Richieste di prenotazione per la qualità del servizio di rete
-   Autenticazione Intranet per Internet Information Services
-   Gestione remota del server o della workstation mediante RPC autenticato
-   [*Richieste di certificati*](../secgloss/c-gly.md) ai Servizi certificati per utenti e computer di dominio

## <a name="ntlm-security-package"></a>Pacchetto di sicurezza NTLM

Il pacchetto di sicurezza NTLM è basato sul protocollo di autenticazione NTLM.

 

 
