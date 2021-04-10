---
title: Valori del registro di sistema per System-Wide sicurezza
description: Valori del registro di sistema per System-Wide sicurezza
ms.assetid: f1db42b8-4328-4b39-b87f-583382395235
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7addfb59bd8074a5a1392e5f74f9cee73d64f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955331"
---
# <a name="registry-values-for-system-wide-security"></a>Valori del registro di sistema per System-Wide sicurezza

Non è consigliabile modificare le impostazioni di sicurezza a livello di sistema, in quanto questa operazione influirà su tutte le applicazioni server COM che non impostano una sicurezza a livello di processo e potrebbe impedire il corretto funzionamento. Se si modificano le impostazioni di sicurezza a livello di sistema in modo da influire sulle impostazioni di sicurezza per una particolare applicazione COM, è necessario modificare le impostazioni di sicurezza a livello di processo per quella particolare applicazione COM. Per ulteriori informazioni sull'impostazione della sicurezza a livello di processo, vedere [impostazione Process-Wide sicurezza](setting-processwide-security.md).

Determinati valori del registro di sistema vengono utilizzati per determinare le impostazioni di sicurezza per le applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). È possibile utilizzare Dcomcnfg.exe per modificare queste impostazioni di sicurezza predefinite per un computer. Per le procedure dettagliate che descrivono come usare Dcomcnfg.exe a questo scopo, vedere [impostazione della sicurezza System-Wide tramite DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).

Un altro modo per modificare le impostazioni predefinite a livello di sistema consiste nel modificare direttamente i valori del registro di sistema. Tuttavia, solo gli amministratori e il sistema hanno accesso completo alla parte del registro di sistema che contiene le impostazioni predefinite per la protezione delle chiamate a livello di sistema. Tutti gli altri utenti hanno solo l'accesso in lettura.

I valori denominati che influiscono sulle impostazioni predefinite di sicurezza a livello di sistema sono i seguenti:

-   [DefaultLaunchPermission](defaultlaunchpermission.md)
-   [DefaultAccessPermission](defaultaccesspermission.md)
-   [LegacyAuthenticationLevel](legacyauthenticationlevel.md)
-   [LegacyImpersonationLevel](legacyimpersonationlevel.md)
-   [LegacySecureReferences](legacysecurereferences.md)
-   [SRPRunningObjectChecks](srprunningobjectchecks.md)
-   [SRPActivateAsActivatorChecks](srpactivateasactivatorchecks.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza Process-Wide](setting-processwide-security.md)
</dt> </dl>

 

 




