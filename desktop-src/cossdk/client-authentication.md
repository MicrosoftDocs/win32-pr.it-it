---
description: L'autenticazione è il processo che determina che i chiamanti sono effettivamente chi dichiarano di essere&8212, verificando l'autenticità di un'attestazione \# di identità.
ms.assetid: c1b11f58-5bab-45d9-a686-86c95415990e
title: Client Authentication (Autenticazione client)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472f16e32cb99f9f2c89c21012f1faa7f96af17878c34d16400f7d505c324398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638991"
---
# <a name="client-authentication"></a>Client Authentication (Autenticazione client)

L'autenticazione è il processo che determina che i chiamanti sono effettivamente chi dichiarano di essere, verificando l'autenticità di un'attestazione di identità. In generale, questa operazione può essere eseguita sia dal server che dal client, ognuno dei quali autentica l'altro. Tuttavia, è particolarmente importante per un'applicazione server che autorizza i client, come per la sicurezza basata sui ruoli, a eseguire anche l'autenticazione. L'autenticazione dei client è un prerequisito per un criterio di autorizzazione significativo. È possibile eseguire tutti i controlli dei ruoli desiderati, ma se non si è certi che l'identità client che si sta controllando sia autentica, l'applicazione si basa fondamentalmente sul sistema honor.

Per le applicazioni COM+, l'autenticazione è un elemento che è possibile attivare e configurare a livello amministrativo, dopo di che funziona in modo trasparente per l'applicazione. È possibile specificare un livello di autenticazione a livello amministrativo usando lo strumento amministrativo Servizi componenti o le funzioni amministrative. Per informazioni dettagliate sull'impostazione dell'autenticazione, vedere Impostazione di un livello di autenticazione [per un'applicazione server](setting-an-authentication-level-for-a-server-application.md) e [Abilitazione dell'autenticazione per un'applicazione di libreria.](enabling-authentication-for-a-library-application.md)

L'impostazione dell'autenticazione implica operazioni diverse a seconda che il tipo di applicazione sia un'applicazione server o di libreria.

## <a name="setting-authentication-for-com-server-applications"></a>Impostazione dell'autenticazione per le applicazioni server COM+

Per un'applicazione server COM+, si imposta un livello di autenticazione che determina come verrà eseguita l'autenticazione quando i client chiamano componenti all'interno dell'applicazione. È possibile scegliere tra diversi livelli di autenticazione che offrono diversi livelli di sicurezza, da nessuna autenticazione alla crittografia di ogni pacchetto e di tutti i parametri di chiamata al metodo. Per altre informazioni, vedere [Impostazione di un livello di autenticazione per un'applicazione server.](setting-an-authentication-level-for-a-server-application.md)

Una maggiore sicurezza presenta tuttavia alcuni costi in termini di prestazioni, che è consigliabile prendere in considerazione durante la configurazione dell'applicazione. COM+ negozierà tra il livello di autenticazione specificato da client e server. Il modo in cui viene eseguita questa negoziazione ha il vantaggio di consentire il controllo amministrativo dell'autenticazione solo dal lato server. Per informazioni dettagliate, vedere [Negoziazione del livello di autenticazione.](negotiation-of-authentication-level.md)

> [!Note]  
> È consigliabile non specificare mai un livello di autenticazione a livello di codice usando [**CoInitializeSecurity all'interno**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) di un'applicazione COM+. COM+ chiama **CoInitializeSecurity** per l'utente e può essere chiamato una sola volta per ogni processo.

 

I servizi di autenticazione sottostanti vengono forniti da COM e Microsoft Windows. In un servizio di autenticazione, una terza parte fornisce un certificato per un utente, attestando l'autenticità dell'identità dell'utente. Questa certificazione è attendibile quanto l'autorità di certificazione e, nello stesso modo in cui la patente di un tassista o un passport funge da documento di certificazione, dipende dall'autorità emittente. Per informazioni più dettagliate sui servizi di autenticazione, vedere [COM and Security Packages (Pacchetti di sicurezza](/windows/desktop/com/com-and-security-packages) e COM) nella documentazione COM.

## <a name="setting-authentication-for-com-library-applications"></a>Impostazione dell'autenticazione per le applicazioni della libreria COM+

Per un'applicazione di libreria COM+, abilitare o disabilitare l'autenticazione per determinare se l'applicazione sarà soggetta all'autenticazione eseguita dal processo di hosting. Anche se l'autenticazione per un'applicazione di libreria COM+ è in gran parte controllata dal processo di hosting, è possibile configurare l'applicazione di libreria in modo che non partecipi all'autenticazione. Ciò significa che le chiamate all'applicazione possono essere autenticate o non autenticate e, nel secondo caso, l'"autenticazione" dei client ha sempre esito positivo. Per altre informazioni, vedere [Abilitazione dell'autenticazione per un'applicazione di libreria.](enabling-authentication-for-a-library-application.md)

Inoltre, potrebbe essere necessario o necessario autenticare il client nel database o in un'applicazione downstream. L'autenticazione dei client solo nell'applicazione COM+ potrebbe non essere sufficiente. In questo caso, è necessario rappresentare il client in modo che l'identità del client sia propagata a valle. Per informazioni dettagliate sulla rappresentazione, vedere [Rappresentazione e delega del client.](client-impersonation-and-delegation.md) Per una descrizione dei problemi relativi alla decisione di eseguire l'autenticazione a livello di dati, vedere [Sicurezza delle applicazioni multilivello.](multi-tier-application-security.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rappresentazione e delega del client](client-impersonation-and-delegation.md)
</dt> <dt>

[Sicurezza delle applicazioni della libreria](library-application-security.md)
</dt> <dt>

[Sicurezza delle applicazioni multilivello](multi-tier-application-security.md)
</dt> <dt>

[Sicurezza dei componenti a livello di codice](programmatic-component-security.md)
</dt> <dt>

[Amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md)
</dt> <dt>

[Uso dei criteri di restrizione software in COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
