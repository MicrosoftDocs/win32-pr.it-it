---
title: Negoziazione della copertura della sicurezza
description: Negoziazione della copertura della sicurezza
ms.assetid: 5a01912d-611c-4a6e-ab9d-0243cba331f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51407de908eaaf0f79eea452046f8e424ccf900
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047435"
---
# <a name="security-blanket-negotiation"></a>Negoziazione della copertura della sicurezza

Una copertura di sicurezza è un gruppo di valori che descrivono le impostazioni di sicurezza che si applicano a tutti i proxy in un processo o solo a un particolare proxy di interfaccia. Una copertura di sicurezza comprende i valori seguenti:

-   Servizio di autenticazione
-   Servizio di autorizzazione
-   Nome principale
-   Livello di autenticazione
-   Livello di rappresentazione
-   Identità di autenticazione
-   Funzionalità
-   Un elenco di controllo di accesso (ACL) (solo server)

La negoziazione della copertura di sicurezza è il processo usato da COM per scegliere le impostazioni di sicurezza per un proxy al momento della creazione. Questo processo comporta il confronto della copertura della sicurezza del server con la coperta di sicurezza del client e l'utilizzo di tali valori per creare una copertura di sicurezza predefinita appropriata per il proxy. I paragrafi seguenti spiegano dove provengono le coperte di sicurezza del client e del server e descrivono in che modo COM negozia la copertura di sicurezza per il proxy usando le coperte di sicurezza del server e del client.

Il client e il server possono chiamare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) per specificare le rispettive coperte di sicurezza. Se un'applicazione non chiama **CoInitializeSecurity** in modo esplicito, com la chiama in modo implicito per l'applicazione, usando i valori predefiniti appropriati. Per ulteriori informazioni su questi valori predefiniti, vedere la pagina relativa alle [impostazioni predefinite di sicurezza com](com-security-defaults.md).

Alcuni parametri per [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) si applicano quando l'applicazione è un server e altri si applicano quando l'applicazione è un client. Quando l'applicazione funge da server, questi parametri sono rilevanti: un ACL, un elenco di Tuple servizio di autenticazione/servizio di autorizzazione/nome entità e un livello di autenticazione. La chiamata di un server a **CoInitializeSecurity**, implicita o esplicita, determina la copertura della sicurezza del server, che rimane fissa.

Quando l'applicazione funge da client, i valori seguenti passati a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) sono rilevanti: un livello di autenticazione, un livello di rappresentazione, l'identità di autenticazione e le funzionalità. Una chiamata implicita o esplicita di un client a **CoInitializeSecurity** indica la copertura di sicurezza che il client desidera.

Quando viene creato un proxy, COM utilizza i valori specificati dalla copertura di sicurezza del server e la copertura di sicurezza del client per negoziare una copertura di sicurezza predefinita appropriata per il proxy. COM sceglie un servizio di autenticazione che funziona sia nel client che nel server. Il servizio di autorizzazione e il nome dell'entità vengono scelti per lavorare con il servizio di autenticazione. Per il livello di autenticazione, COM sceglie maggiore dei livelli di autenticazione specificati dal client e dal server. Il livello di rappresentazione e le funzionalità scelte da COM sono quelli specificati dal client. L'identità di autenticazione è quella specificata dal client per il servizio di autenticazione scelto.

Una volta calcolata la copertura di sicurezza predefinita, i relativi valori vengono assegnati al proxy appena creato. Il client può eseguire l'override delle impostazioni di sicurezza per il proxy chiamando [**IClientSecurity:: Seblankt**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket). I valori specificati per il **Seblankt** non vengono negoziati; vengono semplicemente assegnati al proxy specificato. Tuttavia, se i parametri predefiniti (ad esempio, il \_ livello IMP C di RPC \_ \_ \_ ) vengono passati a **seblankt**, com usa l'algoritmo di negoziazione della copertura di sicurezza descritto in precedenza per calcolare i parametri predefiniti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 