---
title: Uso dell'account LocalSystem come account di accesso al servizio
description: Uno dei vantaggi dell'esecuzione con l'account LocalSystem è che il servizio ha accesso senza restrizioni completo alle risorse locali.
ms.assetid: 2bc2e16d-bd25-4ec6-91a2-8d03052df021
ms.tgt_platform: multiple
keywords:
- account localsystem
- Localsystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4ac31cb7b3e0ad335f9a2781187aadcb03a1529055eb0771856aa01543add0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024579"
---
# <a name="using-the-localsystem-account-as-a-service-logon-account"></a>Uso dell'account LocalSystem come account di accesso al servizio

Uno dei vantaggi dell'esecuzione con l'account LocalSystem è che il servizio ha accesso senza restrizioni completo alle risorse locali. Questo è anche lo svantaggio di LocalSystem perché un servizio LocalSystem può eseguire operazioni che porterebbe all'intero sistema. In particolare, un servizio in esecuzione come LocalSystem in un controller di dominio ha accesso illimitato Active Directory Domain Services. Ciò significa che i bug nel servizio o gli attacchi di sicurezza al servizio possono danneggiare il sistema o, se il servizio si trova in un controller di dominio, danneggiare l'intera rete aziendale.

Per questi motivi, gli amministratori di dominio nelle installazioni sensibili saranno cauti nel consentire l'esecuzione dei servizi come LocalSystem. In effetti, possono avere criteri a esso applicati, in particolare nei controller di dominio. Se il servizio deve essere eseguito come LocalSystem, la documentazione del servizio deve giustificare agli amministratori di dominio i motivi per concedere al servizio il diritto di esecuzione con privilegi elevati. I servizi non devono mai essere eseguiti come LocalSystem in un controller di dominio. Per altre informazioni e un esempio di codice che illustra come un servizio o un programma di installazione del servizio può determinare se è in esecuzione in un controller di dominio, vedere Test dell'esecuzione in [un controller di dominio](testing-whether-running-on-a-domain-controller.md).

Quando un servizio viene eseguito con l'account LocalSystem in un computer membro di dominio, il servizio dispone di qualsiasi accesso di rete concesso all'account computer o a tutti i gruppi di cui l'account computer è membro. Tenere presente che in Windows 2000 un account computer di dominio è un'entità servizio, simile a un account utente. Ciò significa che un account computer può essere in un gruppo di sicurezza e una ACE in un descrittore di sicurezza può concedere l'accesso a un account computer. Tenere presente che l'aggiunta di account computer ai gruppi non è consigliata per due motivi:

-   Gli account computer sono soggetti all'eliminazione e alla ri-creazione se il computer lascia e quindi si ricongiungere al dominio.
-   Se si aggiunge un account computer a un gruppo, a tutti i servizi in esecuzione come LocalSystem in tale computer sono consentiti i diritti di accesso del gruppo. Questo perché tutti i servizi LocalSystem condividono l'account computer del server host. Per questo motivo, è particolarmente importante che gli account computer non siano membri di gruppi di amministratori di dominio.

Gli account computer hanno in genere pochi privilegi e non appartengono ai gruppi. La protezione ACL predefinita in Active Directory Domain Services consente l'accesso minimo per gli account computer. Di conseguenza, i servizi in esecuzione come LocalSystem, in computer diversi dai controller di dominio, hanno solo l'accesso minimo Active Directory Domain Services.

Se il servizio viene eseguito in LocalSystem, è necessario testare il servizio in un server membro per assicurarsi che il servizio disponga di diritti sufficienti per la lettura/scrittura Dominio di Active Directory controller. Un controller di dominio non deve essere l'Windows computer in cui si testa il servizio. Tenere presente che un servizio in esecuzione in LocalSystem in un controller di dominio Windows ha accesso completo a Active Directory Domain Services e che un server membro viene eseguito nel contesto dell'account computer con un numero sostanzialmente inferiore di diritti.

 

 




