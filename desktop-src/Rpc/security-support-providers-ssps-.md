---
title: Security Support Provider (SSP)
description: A partire da Windows 2000, RPC supporta un'ampia gamma di provider e pacchetti di sicurezza.
ms.assetid: f82eba3d-412e-4cb6-9353-2e66bd0f377a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92cc5417dd6142c693005a1aab9d39738d108ae2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118339"
---
# <a name="security-support-providers-ssps"></a>Security Support Provider (SSP)

A partire da Windows 2000, RPC supporta un'ampia gamma di provider e pacchetti di sicurezza. Tra queste sono incluse:

-   **Pacchetto di sicurezza del protocollo Kerberos.** Il protocollo Kerberos V5 è un pacchetto di sicurezza standard del settore. USA i nomi dell'entità fullsic.
-   **SSP SCHANNEL.** Questo SSP implementa il pacchetto di sicurezza del provider di protocollo unificato Microsoft, che unifica SSL, tecnologia di comunicazione privata (PCT) e TLS (Transport Level Security) in un unico pacchetto di sicurezza. Riconosce i nomi dell'entità msstd e fullsic.
-   **Pacchetto di sicurezza NTLM.** Questo è il pacchetto di sicurezza principale per le reti NTLM precedenti a Windows 2000.

Microsoft RPC fornisce inoltre uno *pseudo-SSP* che consente alle applicazioni di negoziare tra l'uso di SSP reali. Questo pseudo-SSP, denominato SSP Simple GSS-API Negotiation Mechanism (Snego), non fornisce funzionalità di autenticazione effettive. L'unico utilizzo è quello di consentire alle applicazioni di selezionare un SSP reale. Attualmente, i programmi client e server possono utilizzare il provider di servizi condivisi Snego per negoziare tra l'utilizzo del pacchetto di sicurezza del protocollo Kerberos e del pacchetto di sicurezza NTLM. Per ulteriori informazioni sulla selezione di SSP, vedere [costanti del servizio di autenticazione](authentication-service-constants.md).

Tutti i provider di servizi condivisi forniti da Microsoft, ad eccezione di SCHANNEL, riconoscono le credenziali di autenticazione nel formato fornito dalla struttura di [**\_ \_ \_ identità di autenticazione WinNT sec**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) . Per informazioni dettagliate, vedere [credenziali di autenticazione client](client-authentication-credentials.md). Per informazioni su come usare SSP specifici, vedere [funzioni SSPI](/windows/desktop/SecMgmt/management-functions) e [uso del provider di sicurezza Schannel](/windows/desktop/SecAuthN/secure-channel) nella documentazione relativa alla sicurezza di Platform Software Development Kit (SDK).

 

 