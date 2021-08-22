---
description: Quando si usa la sicurezza basata sui ruoli nell'applicazione COM+ che contiene il componente, è possibile accedere alle funzionalità di sicurezza a livello di codice dall'interno del componente.
ms.assetid: 6117970c-5dbd-485e-978e-3aa96e42b359
title: Sicurezza dei componenti a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b3fc8813b6aff98f19e7c051067f3246c25b336ea7a99a2371f03c7f3f50883
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462111"
---
# <a name="programmatic-component-security"></a>Sicurezza dei componenti a livello di codice

Quando si usa la sicurezza basata sui ruoli nell'applicazione COM+ che contiene il componente, è possibile accedere alle funzionalità di sicurezza a livello di codice dall'interno del componente. È possibile controllare l'appartenenza al ruolo per determinare se vengono eseguite determinate sezioni di codice, è possibile accedere alle informazioni di sicurezza usando l'oggetto contesto di chiamata di sicurezza ed è possibile determinare se la sicurezza è abilitata per la chiamata corrente. È possibile eseguire tutte queste attività usando un riferimento a un oggetto [**SecurityCallContext**](securitycallcontext.md) (per le applicazioni Microsoft Visual Basic) o un puntatore all'interfaccia [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) (per applicazioni C e Microsoft Visual C++).

Per altre informazioni sulla sicurezza basata su ruoli a livello di codice, vedere gli argomenti seguenti in questa sezione:

-   [Controllo dell'appartenenza al ruolo](checking-role-membership.md)
-   [Determinare se Role-Based sicurezza è abilitata](determining-whether-role-based-security-is-enabled.md)
-   [Accesso alle informazioni sul contesto delle chiamate di sicurezza](accessing-security-call-context-information.md)

## <a name="impersonation-and-com-security-features"></a>Rappresentazione e funzionalità di sicurezza COM

Se il componente viene usato in un'applicazione COM+ che non usa la sicurezza basata sui ruoli, il controllo dei ruoli a livello di codice e le informazioni sul contesto delle chiamate di sicurezza non sono disponibili. Tuttavia, è possibile usare la funzionalità di sicurezza a livello di codice fornita da COM. Per altre informazioni, vedere [Sicurezza in COM](/windows/desktop/com/security-in-com).

Anche se è possibile usare la maggior parte delle funzionalità di sicurezza fornite da COM, non è possibile chiamare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) da un componente che fa parte di un'applicazione COM+ perché **CoInitializeSecurity** viene chiamato dal surrogato in cui viene eseguita l'applicazione COM+. Tuttavia, è possibile chiamare altre funzioni di sicurezza, ad esempio [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), che recupera informazioni sul client.

In particolare, quando è necessario usare l'identità del client per accedere ad alcune risorse, ad esempio l'accesso a un file protetto da un descrittore di sicurezza o la propagazione dell'identità del client a un database, è possibile eseguire la rappresentazione a livello di codice. Per altre informazioni su quando e come eseguire questa operazione, vedere [Rappresentazione e delega del client](client-impersonation-and-delegation.md).

## <a name="testing-security-functionality"></a>Test delle funzionalità di sicurezza

Se si usa la sicurezza a livello di codice COM+ nel componente, è necessario integrare il componente in un'applicazione COM+ quando si è pronti per testare la funzionalità di sicurezza del componente. Se un componente che usa la sicurezza a livello di codice COM+ viene eseguito senza essere integrato in un'applicazione COM+, verranno generate eccezioni. Pertanto, se si vuole garantire che un componente di questo tipo sia anche in grado di essere integrato correttamente in un'applicazione che non fa parte dell'ambiente COM+, è necessario assicurarsi che queste eccezioni vengano gestite in modo appropriato.

## <a name="documenting-security-requirements"></a>Documentazione dei requisiti di sicurezza

Se si scrive un componente autonomo per le applicazioni COM+ che usano la sicurezza basata sui ruoli, è necessario documentare il componente in modo che la sicurezza possa essere configurata in modo appropriato quando il componente è integrato in un'applicazione COM+. Ad esempio, è necessario identificare i ruoli che devono essere aggiunti e spiegare a quali metodi e interfacce deve essere assegnato ogni ruolo. Inoltre, se viene chiamato un metodo, ad esempio IsCallerInRole("Teller"), è necessario descrivere la funzionalità a cui solo gli teller hanno accesso. È anche necessario specificare se è necessario un ruolo per proteggere l'accesso all'intero componente.

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

[Amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md)
</dt> <dt>

[Uso dei criteri di restrizione software in COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
