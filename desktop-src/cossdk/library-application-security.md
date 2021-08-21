---
description: Poiché un'applicazione di libreria COM+ è ospitata da un altro processo, che può avere impostazioni di sicurezza specifiche, la sicurezza per le applicazioni di libreria richiede particolare attenzione.
ms.assetid: a966020c-a0bd-467c-b6d3-e09267cf5574
title: Sicurezza delle applicazioni della libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9fa2d03f21707af42fa108cb9c4ecbce6d2a352ea03714961a0eef4f028119
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813520"
---
# <a name="library-application-security"></a>Sicurezza delle applicazioni della libreria

Poiché un'applicazione di libreria COM+ è ospitata da un altro processo, che può avere impostazioni di sicurezza specifiche, la sicurezza per le applicazioni di libreria richiede particolare attenzione.

Alla sicurezza delle applicazioni della libreria si applicano i vincoli seguenti:

-   Le applicazioni di libreria vengono eseguite con il token di sicurezza del processo client anziché con la propria identità utente. Hanno solo la quantità di privilegi del client.
-   Le applicazioni di libreria non controllano la sicurezza a livello di processo. Nessun utente nei ruoli verrà aggiunto al descrittore di sicurezza per il processo. L'unico modo per un'applicazione di libreria di eseguire i propri controlli di accesso è usare la sicurezza a livello di componente. Vedere [Limiti di sicurezza.](security-boundaries.md)
-   Le applicazioni di libreria possono essere configurate per partecipare o meno all'autenticazione del processo host abilitando o disabilitando l'autenticazione. Vedere [Abilitazione dell'autenticazione per un'applicazione di libreria.](enabling-authentication-for-a-library-application.md)
-   Le applicazioni di libreria non possono impostare un livello di rappresentazione. usano quello del processo host.

## <a name="using-library-applications-to-limit-application-privilege"></a>Uso di applicazioni di libreria per limitare i privilegi dell'applicazione

In alcuni casi, è possibile configurare un'applicazione in modo specifico come applicazione di libreria in modo che venga eseguita con l'identità del processo di hosting. Questa operazione limita fondamentalmente l'applicazione in modo che possa accedere solo alle risorse a cui il client, il processo host, può accedere. I thread in cui vengono eseguiti i componenti dell'applicazione della libreria useranno il token di processo per impostazione predefinita e pertanto, quando effettuano chiamate all'esterno dell'applicazione o accedono a risorse quali file sorvegliati con un descrittore di sicurezza, verranno visualizzati come client. Per le applicazioni che eseguono operazioni sensibili, questo può essere un modo semplice per controllare l'ambito delle azioni.

## <a name="effectively-securing-library-applications"></a>Protezione efficace delle applicazioni di libreria

La configurazione della sicurezza basata sui ruoli e dell'autenticazione per le applicazioni di libreria in modo che funzionino come previsto, è necessario tenere presenti alcune considerazioni speciali. Per informazioni dettagliate, vedere [Configuring Security for Library Applications.](configuring-security-for-library-applications.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione client](client-authentication.md)
</dt> <dt>

[Rappresentazione e delega del client](client-impersonation-and-delegation.md)
</dt> <dt>

[Sicurezza delle applicazioni multilivello](multi-tier-application-security.md)
</dt> <dt>

[Sicurezza dei componenti a livello di codice](programmatic-component-security.md)
</dt> <dt>

[Amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md)
</dt> <dt>

[Uso dei criteri di restrizione software in COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



