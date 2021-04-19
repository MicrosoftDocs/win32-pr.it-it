---
description: Sicurezza delle applicazioni a più livelli
ms.assetid: ff84eeed-ddfd-40e8-8f42-625b4d49ecd5
title: Sicurezza delle applicazioni a più livelli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150f7894c7d11e832786e31ab028f9dbac35f6e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304817"
---
# <a name="multi-tier-application-security"></a>Sicurezza delle applicazioni a più livelli

È possibile affrontare scelte difficili nel decidere esattamente dove applicare la protezione in un'applicazione multilivello basata su componenti: nel database? Al livello intermedio? Nei componenti? Altrove? Ovunque? Con l'aumentare del numero e della complessità dei meccanismi di sicurezza, il calo delle prestazioni e il comportamento dell'applicazione diventano meno prevedibili. Tuttavia, è necessario assicurarsi che i dati siano protetti, che vengano seguite le regole business e che venga registrata un'attività significativa e che l'applicazione funzioni per i client come previsto. È necessario essere certi che ogni percorso client nell'applicazione sia corretto e che i checkpoint di sicurezza disponibili siano sufficienti.

La decisione più complessa è spesso la possibilità di applicare la protezione al database. Storicamente, questo è il punto in cui la sicurezza è più stretta perché viene percepita come un Regno che deve essere effettivamente sicuro e gli amministratori di database sono molto riluttanti a fidarsi di un altro utente per applicare la protezione. Tuttavia, l'applicazione della sicurezza nel database può essere piuttosto costosa e difficile da scalare, che è esattamente il punto di scrittura di applicazioni multilivello in primo luogo.

La regola generale da seguire con le applicazioni multilivello scalabili mediante COM+ è che, laddove possibile, è necessario applicare una sicurezza dettagliata nell'applicazione COM+ a livello intermedio. Questa operazione consente di sfruttare appieno i servizi scalabili forniti da COM+. Eseguire l'autenticazione nel database solo quando è assolutamente necessario e valutare completamente le implicazioni delle prestazioni.

Per informazioni sui problemi da prendere in considerazione per decidere dove eseguire i controlli di sicurezza, vedere [decidere dove applicare la sicurezza](deciding-where-to-enforce-security.md).

Per informazioni su alcuni scenari di base per la protezione di applicazioni multilivello, vedere [scenari di base per la protezione dei dati nelle applicazioni multilivello](basic-scenarios-for-securing-data-in-multi-tier-applications.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione client](client-authentication.md)
</dt> <dt>

[Rappresentazione e delega client](client-impersonation-and-delegation.md)
</dt> <dt>

[Sicurezza delle applicazioni di libreria](library-application-security.md)
</dt> <dt>

[Sicurezza del componente a livello di codice](programmatic-component-security.md)
</dt> <dt>

[Amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md)
</dt> <dt>

[Uso dei criteri di restrizione software in COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



