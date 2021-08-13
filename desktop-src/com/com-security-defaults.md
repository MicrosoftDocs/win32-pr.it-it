---
title: Impostazioni predefinite per la sicurezza COM
description: È possibile usare le impostazioni predefinite per la sicurezza COM per l'applicazione anziché specificare impostazioni di sicurezza personalizzate.
ms.assetid: 6f1f6925-a6ab-4cfa-b0b4-b4b4012979f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6287e00971eca3afe94e598555225943709d1c42546fccb76a442a0dfe3be4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550596"
---
# <a name="com-security-defaults"></a>Impostazioni predefinite per la sicurezza COM

È possibile usare le impostazioni predefinite per la sicurezza COM per l'applicazione anziché specificare impostazioni di sicurezza personalizzate. In tal caso, COM inizializza e gestisce automaticamente la sicurezza. Non è necessario configurare il Registro di sistema o chiamare funzioni di sicurezza nel programma.

Tuttavia, se alcuni valori denominati del Registro di sistema sono stati impostati o modificati, le impostazioni predefinite per la sicurezza utilizzate da COM saranno interessate. Nell'elenco seguente vengono descritti i valori predefiniti della sicurezza COM e viene illustrato in che modo alcuni valori sono influenzati dalle impostazioni del Registro di sistema.

Di seguito sono riportati i valori di sicurezza predefiniti utilizzati da COM:

-   Il provider del servizio di sicurezza predefinito è quello determinato da COM come il più compatibile con l'ambiente. COM sceglie il protocollo Kerberos v5 o NTLMSSP, con il protocollo Kerberos come scelta predefinita. Nessuno dei protocolli forniti da Schannel viene mai scelto come predefinito.
-   Il sistema identifica un chiamante tramite nome utente e password e crea automaticamente un token di identificazione utilizzato dal sistema di sicurezza.
-   Se il [valore denominato LegacyAuthenticationLevel](legacyauthenticationlevel.md) esiste e se il relativo valore è stato impostato, viene usato tale valore. In caso contrario, il livello di autenticazione viene impostato in fase di connessione (RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT). Questo livello significa che alla prima chiamata di un client al server COM esegue un controllo di autenticazione. Se il client supera il controllo, non viene eseguita alcuna ulteriore autenticazione. Il valore AuthenticationLevel può essere impostato anche sotto la [chiave AppID.](appid-key.md)
-   Se il [valore denominato LegacyImpersonationLevel](legacyimpersonationlevel.md) esiste e se il relativo valore è stato impostato, viene usato tale valore. In caso contrario, il livello di rappresentazione è impostato su identify (RPC \_ C \_ IMP LEVEL \_ \_ IDENTIFY). I diritti di rappresentazione vengono concessi dal client al server. Livello di identificazione significa che il server può ottenere l'identità del client. Il server può rappresentare il client per il controllo dell'elenco di controllo di accesso (ACL), ma non può accedere agli oggetti di sistema come client. Per altre informazioni, vedere [Livelli di rappresentazione](impersonation-levels.md) e [Cloaking.](cloaking.md)
-   Se il [valore denominato AccessPermission](accesspermission.md) in **AppID** esiste ed è stato impostato, viene usato tale valore. In caso contrario, COM verifica la presenza [di una voce DefaultAccessPermission.](defaultaccesspermission.md) Se presente, viene usato tale valore. Se questo valore non è presente, COM costruisce un ACL che concede le autorizzazioni all'identità del server e al sistema locale.
-   Se il [valore denominato SRPTrustLevel](srptrustlevel.md) in **AppID** esiste ed è stato impostato, viene usato tale valore. In caso contrario, il livello di attendibilità di Criteri di restrizione software è impostato su Non consentito (SAFER \_ LEVELID DISALLOWED), che indica che l'applicazione viene eseguita in un ambiente vincolato e non è consentito l'accesso a qualsiasi privilegio utente sensibile alla sicurezza \_ dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 




