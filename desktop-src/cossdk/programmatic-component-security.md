---
description: Quando si utilizza la sicurezza basata sui ruoli nell'applicazione COM+ che contiene il componente, è possibile accedere alla funzionalità di sicurezza a livello di codice dall'interno del componente.
ms.assetid: 6117970c-5dbd-485e-978e-3aa96e42b359
title: Sicurezza del componente a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31622608e4d4f54aeb53b403b5d8711ff9c6a9af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304941"
---
# <a name="programmatic-component-security"></a>Sicurezza del componente a livello di codice

Quando si utilizza la sicurezza basata sui ruoli nell'applicazione COM+ che contiene il componente, è possibile accedere alla funzionalità di sicurezza a livello di codice dall'interno del componente. È possibile controllare l'appartenenza ai ruoli per determinare se vengono eseguite specifiche sezioni di codice, è possibile accedere alle informazioni di sicurezza utilizzando l'oggetto contesto delle chiamate di sicurezza e determinare se la sicurezza è abilitata per la chiamata corrente. È possibile eseguire tutte queste attività usando un riferimento a un oggetto [**SecurityCallContext**](securitycallcontext.md) (per le applicazioni Microsoft Visual Basic) o un puntatore all'interfaccia [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) (per le applicazioni C e Microsoft Visual C++).

Per ulteriori informazioni sulla sicurezza basata sui ruoli a livello di codice, vedere gli argomenti seguenti in questa sezione:

-   [Verifica dell'appartenenza ai ruoli](checking-role-membership.md)
-   [Determinare se Role-Based sicurezza è abilitata](determining-whether-role-based-security-is-enabled.md)
-   [Accesso alle informazioni sul contesto delle chiamate di sicurezza](accessing-security-call-context-information.md)

## <a name="impersonation-and-com-security-features"></a>Rappresentazione e funzionalità di sicurezza COM

Se il componente viene utilizzato in un'applicazione COM+ che non utilizza la protezione basata sui ruoli, non sono disponibili informazioni sul contesto di controllo dei ruoli e delle chiamate di sicurezza a livello di codice. Tuttavia, è possibile usare la funzionalità di sicurezza a livello di codice fornita da COM. Per ulteriori informazioni, vedere [sicurezza in com](/windows/desktop/com/security-in-com).

Sebbene sia possibile utilizzare la maggior parte delle funzionalità di sicurezza fornite da COM, non è possibile chiamare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) da un componente che fa parte di un'applicazione com+ perché **CoInitializeSecurity** viene chiamato dal surrogato in cui viene eseguita l'applicazione com+. Tuttavia, è possibile chiamare altre funzioni di sicurezza, ad esempio [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), che recupera le informazioni sul client.

In particolare, quando è necessario usare l'identità del client per accedere a una risorsa, ad esempio l'accesso a un file protetto da un descrittore di sicurezza o la propagazione dell'identità del client tramite a un database, è possibile eseguire la rappresentazione a livello di codice. Per informazioni dettagliate su quando e come eseguire questa operazione, vedere [rappresentazione e delega del client](client-impersonation-and-delegation.md).

## <a name="testing-security-functionality"></a>Test della funzionalità di sicurezza

Se si utilizza la sicurezza a livello di codice COM+ nel componente, è necessario integrare il componente in un'applicazione COM+ quando si è pronti per testare la funzionalità di sicurezza del componente. Se un componente che utilizza la sicurezza a livello di codice COM+ viene eseguito senza essere integrato in un'applicazione COM+, verranno generate eccezioni. Pertanto, se si desidera garantire che tale componente sia anche in grado di integrarsi correttamente in un'applicazione che non fa parte dell'ambiente COM+, è necessario assicurarsi che tali eccezioni vengano gestite in modo appropriato.

## <a name="documenting-security-requirements"></a>Documentazione dei requisiti di sicurezza

Se si sta scrivendo un componente autonomo per applicazioni COM+ che utilizzano la sicurezza basata sui ruoli, è necessario documentare il componente in modo che la sicurezza possa essere configurata in modo appropriato quando il componente è integrato in un'applicazione COM+. È ad esempio necessario identificare i ruoli che devono essere aggiunti e spiegare i metodi e le interfacce a cui deve essere assegnato ogni ruolo. Se, inoltre, viene chiamato un metodo, ad esempio IsCallerInRole ("Teller"), è necessario descrivere la funzionalità a cui hanno accesso solo i cassieri. È inoltre necessario specificare se un ruolo è necessario per consentire la protezione dell'accesso all'intero componente.

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

[Amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md)
</dt> <dt>

[Uso dei criteri di restrizione software in COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
