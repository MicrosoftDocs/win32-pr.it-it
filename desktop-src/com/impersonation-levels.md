---
title: Livelli di rappresentazione (COM)
description: Se la rappresentazione ha esito positivo, significa che il client ha accettato di consentire al server di essere il client a un certo livello.
ms.assetid: 7539bbee-063f-4788-aece-7b70684826c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85286e5fa880ea7620d6f6ccb6107bf139ec2005
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103872978"
---
# <a name="impersonation-levels"></a>Livelli di rappresentazione

Se la rappresentazione ha esito positivo, significa che il client ha accettato di consentire al server di essere il client a un certo livello. I vari gradi di rappresentazione sono denominati *livelli di rappresentazione* e indicano la quantità di autorità assegnata al server durante la rappresentazione del client.

Attualmente sono disponibili quattro livelli di rappresentazione: *anonima*, *Identificazione*, *rappresentazione* e *delegato*. Nell'elenco seguente viene brevemente descritto ogni livello di rappresentazione:

<dl> <dt>

<span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>Anonimo ( \_ \_ livello IMP C \_ RPC \_ anonimo)
</dt> <dd>

Il client è anonimo per il server. Il processo del server può rappresentare il client, ma il token di rappresentazione non contiene informazioni sul client. Questo livello è supportato solo per il trasporto di comunicazione interprocesso locale. Tutti gli altri trasporti promuovono automaticamente questo livello per identificare.

</dd> <dt>

<span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identificazione ( \_ Identificazione del \_ livello IMP C di RPC \_ \_ )
</dt> <dd>

Livello predefinito del sistema. Il server può ottenere l'identità del client e può rappresentarlo per le verifiche degli elenchi di controllo dell'accesso (ACL).

</dd> <dt>

<span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>rappresenta (rappresentazione a livello di RPC \_ C \_ Imp \_ \_ )
</dt> <dd>

Il server può rappresentare il contesto di sicurezza del client quando rappresenta il client. Il server può accedere alle risorse locali come client. Se il server è locale, può accedere alle risorse di rete come client. Se il server è remoto, può accedere solo alle risorse che si trovano nello stesso computer del server.

</dd> <dt>

<span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>Delegate ( \_ \_ delegato livello IMP C RPC \_ \_ )
</dt> <dd>

Livello massimo di rappresentazione. Quando si seleziona questo livello, il server, sia locale che remoto, può rappresentare il contesto di sicurezza del client quando agisce per conto del client. Durante la rappresentazione, le credenziali del client, sia locali che di rete, possono essere passate a un numero qualsiasi di computer.

Affinché la rappresentazione funzioni a livello di delegato, è necessario soddisfare i requisiti seguenti:

-   Il client deve impostare il livello di rappresentazione sul delegato RPC \_ C \_ Imp \_ level \_ .
-   L'account client non deve essere contrassegnato come "l'account è sensibile e non può essere delegato" nel servizio Active Directory.
-   L'account del server deve essere contrassegnato con l'attributo "trusted per la delega" nel servizio Active Directory.
-   I computer che ospitano il client, il server e tutti i server "downstream" devono essere tutti in esecuzione in un dominio.

</dd> </dl>

Scegliendo il livello di rappresentazione, il client comunica al server fino a che punto può passare a rappresentare il client. Il client imposta il livello di rappresentazione sul proxy utilizzato per comunicare con il server.

## <a name="setting-the-impersonation-level"></a>Impostazione del livello di rappresentazione

Esistono due modi per impostare il livello di rappresentazione:

-   Il client può impostarlo processwide tramite una chiamata a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).
-   Un client può impostare la sicurezza a livello di proxy su un'interfaccia di un oggetto remoto tramite una chiamata a [**IClientSecurity:: Seblankt**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (o alla funzione helper [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).

Per impostare il livello di rappresentazione, passare un \_ \_ valore xxx del livello di RPC C appropriato \_ \_ a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) tramite il parametro *dwImpLevel* .

Diversi servizi di autenticazione supportano la rappresentazione a livello di delegato in extent diversi. Ad esempio, NTLMSSP supporta la rappresentazione a livello di delegato cross-thread e tra processi, ma non tra computer. D'altra parte, il protocollo Kerberos supporta la rappresentazione a livello di delegato attraverso i limiti del computer, mentre Schannel non supporta alcuna rappresentazione a livello di delegato. Se si dispone di un proxy al livello di rappresentazione e si desidera impostare il livello di rappresentazione su delegare, è necessario chiamare il metodo [**Seblankt**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) utilizzando le costanti predefinite per ogni parametro eccetto il livello di rappresentazione. COM sceglierà NTLM localmente e il protocollo Kerberos in modalità remota (quando il protocollo Kerberos funzionerà).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Delega e rappresentazione](delegation-and-impersonation.md)
</dt> </dl>

 

 