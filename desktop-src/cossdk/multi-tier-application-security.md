---
description: Sicurezza delle applicazioni multilivello
ms.assetid: ff84eeed-ddfd-40e8-8f42-625b4d49ecd5
title: Sicurezza delle applicazioni multilivello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69ba43970c2af5ff6c7abb733767b721091f6a3d3407178d5360e5f96db11d99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070470"
---
# <a name="multi-tier-application-security"></a>Sicurezza delle applicazioni multilivello

È possibile affrontare scelte difficili per decidere con precisione dove applicare la sicurezza in un'applicazione multilivello basata su componenti: nel database? Al livello intermedio? Nei componenti? Altrove? Ovunque? Con l'aumentare del numero e della complessità dei meccanismi di sicurezza, le prestazioni diminuiscono e il comportamento dell'applicazione diventa meno prevedibile. Tuttavia, è necessario assicurarsi che i dati siano protetti, che le regole business siano seguite e che siano registrate attività significative e che l'applicazione funzioni per i client come previsto. È necessario essere certi che ogni percorso client tramite l'applicazione sia corretto e che i checkpoint di sicurezza presenti siano sufficiente.

La decisione più difficile è spesso se applicare la sicurezza nel database. In un momento storico, la sicurezza è più stretta perché viene percepita come l'unico regno che deve essere realmente sicuro e gli amministratori di database sono molto restii a affidarsi a un altro utente per imporre la sicurezza per loro. Tuttavia, l'applicazione della sicurezza nel database può essere piuttosto costosa e difficile da ridimensionare, che è esattamente il punto di scrittura di applicazioni multilivello.

La regola generale da seguire con le applicazioni multilivello scalabili con COM+ è che, quando possibile, è necessario applicare una sicurezza dettagliata nell'applicazione COM+ nel livello intermedio. In questo modo è possibile sfruttare completamente i servizi scalabili forniti da COM+. Eseguire l'autenticazione nel database solo quando è assolutamente necessario e valutare completamente le implicazioni in termini di prestazioni di questa operazione.

Per una descrizione dei problemi da considerare per decidere dove eseguire i controlli di sicurezza, vedere [Decidere dove applicare la sicurezza.](deciding-where-to-enforce-security.md)

Per una descrizione di alcuni scenari di base per la protezione di applicazioni multilivello, vedere Scenari di base per la protezione dei dati [in applicazioni multilivello](basic-scenarios-for-securing-data-in-multi-tier-applications.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione client](client-authentication.md)
</dt> <dt>

[Rappresentazione e delega del client](client-impersonation-and-delegation.md)
</dt> <dt>

[Sicurezza delle applicazioni della libreria](library-application-security.md)
</dt> <dt>

[Sicurezza dei componenti a livello di codice](programmatic-component-security.md)
</dt> <dt>

[Amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md)
</dt> <dt>

[Uso dei criteri di restrizione software in COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



