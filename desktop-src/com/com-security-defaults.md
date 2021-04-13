---
title: Impostazioni predefinite di sicurezza COM
description: È possibile usare le impostazioni predefinite di sicurezza COM per l'applicazione, anziché specificare impostazioni di sicurezza personalizzate.
ms.assetid: 6f1f6925-a6ab-4cfa-b0b4-b4b4012979f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cba607044d6e93c9f01243809feae6e5a600851
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328503"
---
# <a name="com-security-defaults"></a>Impostazioni predefinite di sicurezza COM

È possibile usare le impostazioni predefinite di sicurezza COM per l'applicazione, anziché specificare impostazioni di sicurezza personalizzate. In tal caso, COM Inizializza e gestisce la sicurezza. Non è necessario configurare il registro di sistema o chiamare funzioni di sicurezza nel programma.

Tuttavia, se alcuni valori denominati del registro di sistema sono stati impostati o modificati, verranno interessate le impostazioni predefinite di sicurezza utilizzate da COM. Nell'elenco seguente vengono descritti i valori predefiniti di sicurezza COM e viene illustrato come alcuni valori sono influenzati dalle impostazioni del registro di sistema.

Di seguito sono riportati i valori di sicurezza predefiniti usati da COM:

-   Il provider di servizi di sicurezza predefinito è quello determinato da COM come più compatibile con l'ambiente. COM sceglie il protocollo Kerberos V5 o NTLMSSP, con il protocollo Kerberos che è la scelta predefinita. Nessuno dei protocolli forniti da Schannel viene scelto come valore predefinito.
-   Il sistema identifica un chiamante tramite nome utente e password e crea automaticamente un token di identificazione utilizzato dal sistema di sicurezza.
-   Se il valore denominato [LegacyAuthenticationLevel](legacyauthenticationlevel.md) esiste e se il relativo valore è stato impostato, verrà usato tale valore. In caso contrario, il livello di autenticazione viene impostato in fase di connessione (connessione a livello di autenticazione RPC \_ C \_ \_ \_ ). Questo livello indica che, alla prima chiamata eseguita da un client al server, COM esegue un controllo di autenticazione. Se il client supera la verifica, non viene eseguita alcuna ulteriore autenticazione. Il valore AuthenticationLevel può essere impostato anche sotto la chiave [AppID](appid-key.md) .
-   Se il valore denominato [LegacyImpersonationLevel](legacyimpersonationlevel.md) esiste e se il relativo valore è stato impostato, verrà usato tale valore. In caso contrario, il livello di rappresentazione è impostato in modo da identificare (identificazione del livello di RPC \_ C \_ \_ \_ ). I diritti di rappresentazione vengono concessi dal client al server. Il livello di identificazione indica che il server può ottenere l'identità del client. Il server può rappresentare il client per il controllo dell'elenco di controllo di accesso (ACL) ma non può accedere agli oggetti di sistema come client. Per ulteriori informazioni, vedere [livelli di rappresentazione](impersonation-levels.md) e [mascheramento](cloaking.md).
-   Se il valore denominato [AccessPermission](accesspermission.md) in **AppID** esiste e è stato impostato, viene utilizzato tale valore. In caso contrario, COM controlla la presenza di una voce [DefaultAccessPermission](defaultaccesspermission.md) . Se presente, viene utilizzato tale valore. Se questo valore non è presente, COM costruisce un ACL che concede le autorizzazioni per l'identità del server e il sistema locale.
-   Se il valore denominato [SRPTrustLevel](srptrustlevel.md) in **AppID** esiste e è stato impostato, viene utilizzato tale valore. In caso contrario, il livello di attendibilità del criterio di restrizione software (SRP) viene impostato su non consentito (sicurezza \_ LEVELID non \_ consentita), che indica che l'applicazione viene eseguita in un ambiente vincolato e non è consentito l'accesso a tutti i privilegi utente sensibili per la sicurezza dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 




