---
title: Utilizzo dell'account LocalSystem come account di accesso al servizio
description: Un vantaggio dell'esecuzione con l'account LocalSystem è che il servizio ha un accesso illimitato illimitato alle risorse locali.
ms.assetid: 2bc2e16d-bd25-4ec6-91a2-8d03052df021
ms.tgt_platform: multiple
keywords:
- account LocalSystem
- LocalSystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bec3826984e28e29d3156b784da229f8e53e34e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955129"
---
# <a name="using-the-localsystem-account-as-a-service-logon-account"></a>Utilizzo dell'account LocalSystem come account di accesso al servizio

Un vantaggio dell'esecuzione con l'account LocalSystem è che il servizio ha un accesso illimitato illimitato alle risorse locali. Questo è anche lo svantaggio di LocalSystem perché un servizio LocalSystem può eseguire operazioni che potrebbero comportare l'arresto dell'intero sistema. In particolare, un servizio in esecuzione come LocalSystem in un controller di dominio (DC) ha accesso illimitato ai Active Directory Domain Services. Ciò significa che i bug nel servizio o gli attacchi alla sicurezza del servizio possono danneggiare il sistema o, se il servizio si trova in un controller di dominio, danneggiare l'intera rete aziendale.

Per questi motivi, gli amministratori di dominio nelle installazioni riservate saranno cauti per consentire l'esecuzione dei servizi come LocalSystem. In realtà, è possibile che dispongano di criteri in base ai controller di dominio. Se il servizio deve essere eseguito come LocalSystem, la documentazione per il servizio deve giustificare agli amministratori di dominio i motivi per concedere al servizio il diritto di esecuzione con privilegi elevati. I servizi non devono mai essere eseguiti come LocalSystem in un controller di dominio. Per ulteriori informazioni e un esempio di codice in cui viene illustrato come un servizio o un programma di installazione del servizio possa determinare se è in esecuzione in un controller di dominio, vedere [Verifica dell'esecuzione in un controller di dominio](testing-whether-running-on-a-domain-controller.md).

Quando un servizio viene eseguito con l'account LocalSystem in un computer che è membro di un dominio, il servizio dispone di qualsiasi accesso alla rete concesso all'account computer o ai gruppi di cui l'account del computer è membro. Tenere presente che in Windows 2000, un account computer di dominio è un'entità servizio, simile a un account utente. Ciò significa che un account computer può trovarsi in un gruppo di sicurezza e una voce ACE in un descrittore di sicurezza può concedere l'accesso a un account computer. Tenere presente che l'aggiunta di account computer ai gruppi non è consigliata per due motivi:

-   Gli account computer sono soggetti a eliminazione e ricreazione se il computer lascia e quindi si aggiunge nuovamente al dominio.
-   Se si aggiunge un account computer a un gruppo, tutti i servizi in esecuzione come LocalSystem nel computer sono autorizzati ai diritti di accesso del gruppo. Poiché tutti i servizi LocalSystem condividono l'account computer del server host. Per questo motivo, è particolarmente importante che gli account computer non siano membri di alcun gruppo di amministratori di dominio.

Gli account computer in genere hanno pochi privilegi e non appartengono a gruppi. La protezione ACL predefinita in Active Directory Domain Services consente un accesso minimo per gli account computer. Di conseguenza, i servizi in esecuzione come LocalSystem, in computer diversi da controller di dominio, hanno solo l'accesso minimo ai Active Directory Domain Services.

Se il servizio viene eseguito in LocalSystem, è necessario testare il servizio in un server membro per verificare che il servizio disponga di diritti sufficienti per la lettura/scrittura per i controller Dominio di Active Directory. Un controller di dominio non deve essere l'unico computer Windows in cui viene testato il servizio. Tenere presente che un servizio in esecuzione in LocalSystem in un controller di dominio Windows dispone dell'accesso completo alla Active Directory Domain Services e che un server membro viene eseguito nel contesto dell'account computer con un numero di diritti notevolmente inferiore.

 

 




