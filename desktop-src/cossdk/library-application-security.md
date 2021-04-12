---
description: Poiché un'applicazione libreria COM+ è ospitata da un altro processo, che può avere le proprie impostazioni di sicurezza, la sicurezza per le applicazioni di libreria richiede una particolare attenzione.
ms.assetid: a966020c-a0bd-467c-b6d3-e09267cf5574
title: Sicurezza delle applicazioni di libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2885173f3798d33ed26a5b447fde4429b9bf96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523418"
---
# <a name="library-application-security"></a>Sicurezza delle applicazioni di libreria

Poiché un'applicazione libreria COM+ è ospitata da un altro processo, che può avere le proprie impostazioni di sicurezza, la sicurezza per le applicazioni di libreria richiede una particolare attenzione.

I vincoli seguenti si applicano alla sicurezza dell'applicazione della libreria:

-   Le applicazioni di libreria vengono eseguite con il token di sicurezza del processo client anziché con la propria identità utente. Hanno solo il privilegio del client.
-   Le applicazioni di libreria non controllano la sicurezza a livello di processo. Nessun utente nei ruoli verrà aggiunto al descrittore di sicurezza per il processo. L'unico modo per eseguire controlli di accesso a un'applicazione libreria consiste nell'usare la sicurezza a livello di componente. Vedere i [limiti di sicurezza](security-boundaries.md).
-   Le applicazioni di libreria possono essere configurate per partecipare o non partecipare all'autenticazione del processo host, abilitando o disabilitando l'autenticazione. Vedere [Abilitazione dell'autenticazione per un'applicazione di libreria](enabling-authentication-for-a-library-application.md).
-   Le applicazioni di libreria non possono impostare un livello di rappresentazione. usano quello del processo host.

## <a name="using-library-applications-to-limit-application-privilege"></a>Uso delle applicazioni di libreria per limitare i privilegi dell'applicazione

In alcuni casi, può essere necessario configurare un'applicazione in modo specifico come applicazione di libreria in modo che venga eseguita con l'identità del processo di hosting. Questa operazione limita fondamentalmente l'applicazione in modo che possa accedere solo alle risorse accessibili dal client, ovvero dal processo host. I thread sui quali vengono eseguiti i componenti dell'applicazione della libreria utilizzeranno il token di processo per impostazione predefinita e, pertanto, quando effettuano chiamate all'esterno dell'applicazione o accedono alle risorse, ad esempio i file sorvegliati con un descrittore di sicurezza, verranno visualizzati come client. Per le applicazioni che eseguono operazioni riservate, questo può essere un modo semplice per controllare l'ambito delle proprie azioni.

## <a name="effectively-securing-library-applications"></a>Protezione efficace delle applicazioni di libreria

Per la configurazione della sicurezza basata sui ruoli e dell'autenticazione per le applicazioni di libreria è necessario tenere presenti alcune considerazioni speciali, in modo che vengano eseguite come previsto. Per informazioni dettagliate, vedere [configurazione della protezione per le applicazioni di libreria](configuring-security-for-library-applications.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione client](client-authentication.md)
</dt> <dt>

[Rappresentazione e delega client](client-impersonation-and-delegation.md)
</dt> <dt>

[Sicurezza delle applicazioni a più livelli](multi-tier-application-security.md)
</dt> <dt>

[Sicurezza del componente a livello di codice](programmatic-component-security.md)
</dt> <dt>

[Amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md)
</dt> <dt>

[Uso dei criteri di restrizione software in COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



