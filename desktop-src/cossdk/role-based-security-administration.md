---
description: Role-Based amministrazione della sicurezza
ms.assetid: 7247758e-f486-4ce2-afca-f0d10fffe626
title: Role-Based amministrazione della sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c72ed2f1fdd5eb0b650b991b776364bf982c774b3ffcaff1358ea2c3ed1ee4d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547073"
---
# <a name="role-based-security-administration"></a>Role-Based amministrazione della sicurezza

La sicurezza basata sui ruoli è un servizio automatico fornito da COM+ che consente di costruire e applicare a livello amministrativo criteri di controllo di accesso per l'applicazione COM+. Con un modello di configurazione della sicurezza flessibile ed estendibile, la sicurezza basata sui ruoli offre un notevole vantaggio rispetto all'applicazione di tutta la sicurezza all'interno dei componenti e offre i vantaggi seguenti:

-   È possibile configurare la sicurezza a livello amministrativo usando lo strumento amministrativo Servizi componenti o le funzioni amministrative.
-   Non è necessario scrivere la logica correlata alla sicurezza nei componenti quando la protezione dei ruoli a livello di metodo offre un controllo di accesso sufficientemente fine.
-   Non è necessario fattori di sicurezza nella progettazione dell'interfaccia o dei componenti. È invece possibile impostare la sicurezza in base al metodo.
-   È possibile concentrarsi sulla struttura dei criteri di sicurezza da applicare e, tramite i ruoli, tale criterio può essere espresso chiaramente agli amministratori che distribuiscono l'applicazione.
-   È possibile modificare facilmente i criteri di sicurezza per adattarsi ai requisiti di sicurezza in continua evoluzione per un'applicazione.
-   Se necessario, è possibile creare criteri di sicurezza più granulari a livello di codice, usando la sicurezza basata sui ruoli come piattaforma di supporto.
-   È possibile sfruttare la sicurezza basata sui ruoli per eseguire un controllo dettagliato, perché è possibile ottenere informazioni sulla sicurezza del chiamante per un'intera catena di chiamate upstream.

> [!Note]  
> Gli utenti con ruolo Amministratore per l'applicazione di sistema devono essere membri del gruppo Administrators locale. Inoltre, a Windows Server 2003, la funzionalità di autenticazione per l'applicazione di sistema COM+ include il valore EOAC \_ DISABLE \_ AAA. Questo valore, che disabilita le attivazioni activate-as-activator (AAA), viene usato nella chiamata [**a CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) all'avvio dell'applicazione di sistema. L'impostazione della funzionalità di autenticazione su EOAC DISABLE AAA consente a un'applicazione eseguita con un account con privilegi (ad esempio LocalSystem) di impedire che la relativa identità venga usata per avviare componenti non \_ \_ attendibili.

 

Vedere gli argomenti seguenti in questa sezione per informazioni sul funzionamento della sicurezza basata sui ruoli e sui problemi da considerare quando la si usa per costruire criteri di sicurezza per un'applicazione:

-   [Uso dei ruoli per l'autorizzazione client](using-roles-for-client-authorization.md)
-   [Progettazione efficace dei ruoli](designing-roles-effectively.md)
-   [Limiti di sicurezza](security-boundaries.md)
-   [Informazioni sul contesto di chiamata di sicurezza](security-call-context-information.md)
-   [Proprietà del contesto di sicurezza](security-context-property.md)

Per descrizioni dettagliate delle procedure necessarie per configurare la sicurezza basata sui ruoli per un'applicazione, vedere [Configuring Role-Based Security](configuring-role-based-security.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione client](client-authentication.md)
</dt> <dt>

[Rappresentazione e delega del client](client-impersonation-and-delegation.md)
</dt> <dt>

[Sicurezza delle applicazioni della libreria](library-application-security.md)
</dt> <dt>

[Sicurezza delle applicazioni multilivello](multi-tier-application-security.md)
</dt> <dt>

[Sicurezza dei componenti a livello di codice](programmatic-component-security.md)
</dt> <dt>

[Uso dei criteri di restrizione software in COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
