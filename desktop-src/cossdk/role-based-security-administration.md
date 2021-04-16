---
description: Amministrazione della sicurezza Role-Based
ms.assetid: 7247758e-f486-4ce2-afca-f0d10fffe626
title: Amministrazione della sicurezza Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714cede74e105a68b0a5fed2371858054add954e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524041"
---
# <a name="role-based-security-administration"></a>Amministrazione della sicurezza Role-Based

La protezione basata sui ruoli è un servizio automatico fornito da COM+ che consente di costruire e applicare in modo amministrativo un criterio di controllo di accesso per l'applicazione COM+. Con un modello di configurazione della sicurezza flessibile ed estendibile, la protezione basata sui ruoli offre un notevole vantaggio rispetto all'applicazione di tutta la sicurezza all'interno dei componenti e offre i vantaggi seguenti:

-   È possibile configurare la sicurezza in modo amministrativo, usando lo strumento di amministrazione Servizi componenti o le funzioni amministrative.
-   Non è necessario scrivere logica correlata alla sicurezza nei componenti quando la protezione dei ruoli a livello di metodo offre un controllo di accesso sufficientemente preciso.
-   Non è necessario eseguire il factoring della sicurezza nella progettazione di interfacce o componenti. È invece possibile impostare la sicurezza in base al metodo.
-   È possibile concentrarsi sulla struttura dei criteri di sicurezza che si desidera applicare e, tramite i ruoli, che i criteri possono essere chiaramente espressi agli amministratori che distribuiscono l'applicazione.
-   È possibile modificare facilmente i criteri di sicurezza per adattarsi ai requisiti di sicurezza in evoluzione per un'applicazione.
-   È possibile creare criteri di sicurezza più granulari a livello di codice, se necessario, usando la protezione basata sui ruoli come piattaforma di supporto.
-   È possibile sfruttare la protezione basata sui ruoli per eseguire controlli dettagliati, perché è possibile ottenere informazioni sulla sicurezza del chiamante per un'intera catena di chiamate upstream.

> [!Note]  
> Gli utenti con ruolo di amministratore per l'applicazione di sistema devono essere membri del gruppo Administrators locale. Inoltre, a partire da Windows Server 2003, la funzionalità di autenticazione per l'applicazione di sistema COM+ include il valore EOAC \_ Disable \_ AAA. Questo valore, che disabilita le attivazioni di Activate-As-Activator (AAA), viene usato nella chiamata [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) quando viene avviata l'applicazione di sistema. Impostando la funzionalità di autenticazione su EOAC \_ Disable AAA è possibile consentire a \_ un'applicazione in esecuzione con un account con privilegi, ad esempio LocalSystem, di impedire l'utilizzo dell'identità per l'avvio di componenti non attendibili.

 

Vedere gli argomenti seguenti in questa sezione per informazioni sul funzionamento della sicurezza basata sui ruoli e sui problemi da considerare quando si usa per creare criteri di sicurezza per un'applicazione:

-   [Utilizzo dei ruoli per l'autorizzazione client](using-roles-for-client-authorization.md)
-   [Progettazione efficace dei ruoli](designing-roles-effectively.md)
-   [Limiti di sicurezza](security-boundaries.md)
-   [Informazioni sul contesto delle chiamate di sicurezza](security-call-context-information.md)
-   [Proprietà del contesto di sicurezza](security-context-property.md)

Per una descrizione dettagliata dei passaggi necessari per la configurazione della sicurezza basata sui ruoli per un'applicazione, vedere [configurazione Role-Based sicurezza](configuring-role-based-security.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione client](client-authentication.md)
</dt> <dt>

[Rappresentazione e delega client](client-impersonation-and-delegation.md)
</dt> <dt>

[Sicurezza delle applicazioni di libreria](library-application-security.md)
</dt> <dt>

[Sicurezza delle applicazioni a più livelli](multi-tier-application-security.md)
</dt> <dt>

[Sicurezza del componente a livello di codice](programmatic-component-security.md)
</dt> <dt>

[Uso dei criteri di restrizione software in COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
