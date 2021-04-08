---
description: L'autenticazione è il processo che consente di determinare che i chiamanti sono in realtà quelli che dicono che sono&\# 8212, verificando l'autenticità di un'attestazione di identità.
ms.assetid: c1b11f58-5bab-45d9-a686-86c95415990e
title: Client Authentication (Autenticazione client)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd24edf341fc2033807587b01fd37420d781d5f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966218"
---
# <a name="client-authentication"></a>Client Authentication (Autenticazione client)

L'autenticazione è il processo che consente di determinare che i chiamanti sono in realtà quelli che affermano di essere, verificando l'autenticità di un'attestazione di identità. In generale, questa operazione può essere eseguita sia dal server che dal client, ciascuno dei quali esegue l'autenticazione dell'altro. Ma è particolarmente importante per un'applicazione server che autorizza i client, come per la protezione basata sui ruoli, anche per l'autenticazione. L'autenticazione dei client è un prerequisito per un criterio di autorizzazione significativo. È possibile eseguire tutte le operazioni di controllo del ruolo desiderate, ma se non si è certi che l'identità del client che si sta controllando sia autentica, l'applicazione si basa essenzialmente sul sistema rispettato.

Per le applicazioni COM+, l'autenticazione è un elemento che è possibile attivare e configurare in modo amministrativo, dopo il quale funziona in modo trasparente per l'applicazione. È possibile specificare un livello di autenticazione amministrativo utilizzando lo strumento di amministrazione Servizi componenti o le funzioni amministrative. Per informazioni dettagliate sull'impostazione dell'autenticazione, vedere [impostazione di un livello di autenticazione per un'applicazione server](setting-an-authentication-level-for-a-server-application.md) e [Abilitazione dell'autenticazione per un'applicazione di libreria](enabling-authentication-for-a-library-application.md).

L'impostazione dell'autenticazione indica diversi elementi a seconda che il tipo di applicazione sia un'applicazione server o libreria.

## <a name="setting-authentication-for-com-server-applications"></a>Impostazione dell'autenticazione per le applicazioni server COM+

Per un'applicazione server COM+, è necessario impostare un livello di autenticazione che determini come verrà eseguita l'autenticazione quando i client eseguono la chiamata ai componenti all'interno dell'applicazione. È possibile scegliere tra diversi livelli di autenticazione che forniscono diversi gradi di sicurezza, che variano da nessuna autenticazione alla crittografia di ogni pacchetto e tutti i parametri di chiamata al metodo. Per ulteriori informazioni, vedere [impostazione di un livello di autenticazione per un'applicazione server](setting-an-authentication-level-for-a-server-application.md).

Una maggiore sicurezza comporta tuttavia un certo costo in termini di prestazioni, che è opportuno prendere in considerazione durante la configurazione dell'applicazione. COM+ negozierà tra il livello di autenticazione specificato dal client e il server. Il modo in cui viene eseguita questa negoziazione ha il vantaggio di consentire di controllare amministrativamente l'autenticazione solo dal lato server. Per informazioni dettagliate, vedere [negoziazione del livello di autenticazione](negotiation-of-authentication-level.md).

> [!Note]  
> Non specificare mai un livello di autenticazione a livello di codice utilizzando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) all'interno di un'applicazione com+. COM+ chiama **CoInitializeSecurity** per l'utente e può essere chiamato solo una volta per processo.

 

I servizi di autenticazione sottostanti sono forniti da COM e Microsoft Windows. In un servizio di autenticazione, una terza parte fornisce un certificato per un utente che attesta l'autenticità dell'identità dell'utente. Questa certificazione è credibile come l'autorità di certificazione e, nello stesso modo in cui la licenza di un driver o un passaporto funge da documento di certificazione, dipende dall'autorità dell'emittente. Per informazioni più dettagliate sui servizi di autenticazione, vedere [pacchetti com e di sicurezza](/windows/desktop/com/com-and-security-packages) nella documentazione com.

## <a name="setting-authentication-for-com-library-applications"></a>Impostazione dell'autenticazione per le applicazioni della libreria COM+

Per un'applicazione libreria COM+, abilitare o disabilitare l'autenticazione per determinare se l'applicazione sarà soggetta all'autenticazione eseguita dal processo di hosting. Anche se l'autenticazione per un'applicazione libreria COM+ è ampiamente controllata dal processo di hosting, è possibile configurare l'applicazione della libreria in modo che non partecipi all'autenticazione. Ovvero, le chiamate all'applicazione possono essere autenticate o non autenticate e, nel secondo caso, l'autenticazione dei client ha sempre esito positivo. Per ulteriori informazioni, vedere [Abilitazione dell'autenticazione per un'applicazione di libreria](enabling-authentication-for-a-library-application.md).

Inoltre, potrebbe essere necessario o essere richiesti per autenticare il client nel database o in un'applicazione downstream. l'autenticazione dei client solo nell'applicazione COM+ potrebbe non essere sufficiente. In tal caso, è necessario rappresentare il client in modo che l'identità del client venga propagata a valle. Per informazioni dettagliate sulla rappresentazione, vedere [rappresentazione e delega del client](client-impersonation-and-delegation.md). Per informazioni sui problemi relativi alla scelta di eseguire l'autenticazione a livello di dati, vedere [sicurezza delle applicazioni](multi-tier-application-security.md)a più livelli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rappresentazione e delega client](client-impersonation-and-delegation.md)
</dt> <dt>

[Sicurezza delle applicazioni di libreria](library-application-security.md)
</dt> <dt>

[Sicurezza delle applicazioni a più livelli](multi-tier-application-security.md)
</dt> <dt>

[Sicurezza del componente a livello di codice](programmatic-component-security.md)
</dt> <dt>

[Amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md)
</dt> <dt>

[Uso dei criteri di restrizione software in COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
