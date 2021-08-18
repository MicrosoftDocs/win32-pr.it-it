---
title: Livelli di rappresentazione (COM)
description: Se la rappresentazione ha esito positivo, significa che il client ha accettato di consentire al server di essere il client in una certa misura.
ms.assetid: 7539bbee-063f-4788-aece-7b70684826c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca691c89e7ff4a12e279ae0ecd0fd04cb31a951c8ac3f2671201fe99dd5900a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756391"
---
# <a name="impersonation-levels"></a>Livelli di rappresentazione

Se la rappresentazione ha esito positivo, significa che il client ha accettato di consentire al server di essere il client in una certa misura. I diversi gradi di rappresentazione sono detti livelli di rappresentazione e indicano la quantità di autorità data al server quando rappresenta il client.

Attualmente sono disponibili quattro livelli di rappresentazione: *anonimo,* *identificare*, *rappresentare* e *delegare*. L'elenco seguente descrive brevemente ogni livello di rappresentazione:

<dl> <dt>

<span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>anonymous (RPC \_ C \_ IMP LEVEL \_ \_ ANONYMOUS)
</dt> <dd>

Il client è anonimo per il server. Il processo del server può rappresentare il client, ma il token di rappresentazione non contiene informazioni sul client. Questo livello è supportato solo sul trasporto di comunicazione interprocesso locale. Tutti gli altri trasporti alzano di livello automaticamente questo livello per l'identificazione.

</dd> <dt>

<span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identify (RPC \_ C \_ IMP LEVEL \_ \_ IDENTIFY)
</dt> <dd>

Livello predefinito del sistema. Il server può ottenere l'identità del client e può rappresentarlo per le verifiche degli elenchi di controllo dell'accesso (ACL).

</dd> <dt>

<span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>impersonate (RPC \_ C \_ IMP LEVEL \_ \_ IMPERSONATE)
</dt> <dd>

Il server può rappresentare il contesto di sicurezza del client quando rappresenta il client. Il server può accedere alle risorse locali come client. Se il server è locale, può accedere alle risorse di rete come client. Se il server è remoto, può accedere solo alle risorse che si trova nello stesso computer del server.

</dd> <dt>

<span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>delegate (RPC \_ C \_ IMP LEVEL \_ \_ DELEGATE)
</dt> <dd>

Livello massimo di rappresentazione. Quando si seleziona questo livello, il server, sia locale che remoto, può rappresentare il contesto di sicurezza del client quando agisce per conto del client. Durante la rappresentazione, le credenziali del client (sia locali che di rete) possono essere passate a qualsiasi numero di computer.

Per il funzionamento della rappresentazione a livello di delegato, è necessario soddisfare i requisiti seguenti:

-   Il client deve impostare il livello di rappresentazione su RPC \_ C \_ IMP LEVEL \_ \_ DELEGATE.
-   L'account client non deve essere contrassegnato come "L'account è sensibile e non può essere delegato" nel servizio Active Directory.
-   L'account del server deve essere contrassegnato con l'attributo "Trusted for delegation" nel servizio Active Directory.
-   I computer che ospitano il client, il server e tutti i server "downstream" devono essere tutti in esecuzione in un dominio.

</dd> </dl>

Scegliendo il livello di rappresentazione, il client indica al server fino a che punto può rappresentare il client. Il client imposta il livello di rappresentazione nel proxy utilizzato per comunicare con il server.

## <a name="setting-the-impersonation-level"></a>Impostazione del livello di rappresentazione

Esistono due modi per impostare il livello di rappresentazione:

-   Il client può impostarlo a livello di processo tramite una chiamata a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).
-   Un client può impostare la sicurezza a livello di proxy su un'interfaccia di un oggetto remoto tramite una chiamata a [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (o alla funzione helper [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).

Impostare il livello di rappresentazione passando un valore RPC C IMP LEVEL xxx appropriato a \_ \_ \_ \_ [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) tramite *il parametro dwImpLevel.*

Servizi di autenticazione diversi supportano la rappresentazione a livello di delegato in extent diversi. Ad esempio, NTLMSSP supporta la rappresentazione a livello di delegato tra thread e tra processi, ma non tra computer. D'altra parte, il protocollo Kerberos supporta la rappresentazione a livello di delegato attraverso i limiti del computer, mentre Schannel non supporta alcuna rappresentazione a livello di delegato. Se si dispone di un proxy a livello di rappresentazione e si vuole impostare il livello di rappresentazione su delegato, è necessario chiamare [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) usando le costanti predefinite per ogni parametro, ad eccezione del livello di rappresentazione. COM sceglierà NTLM in locale e il protocollo Kerberos in remoto (quando il protocollo Kerberos funzionerà).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Delega e rappresentazione](delegation-and-impersonation.md)
</dt> </dl>

 

 