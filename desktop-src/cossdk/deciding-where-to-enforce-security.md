---
description: I compromessi sono intrinseci nell'applicazione della sicurezza.
ms.assetid: f01573f3-aae6-400e-bdd9-6f34f4e262f6
title: Decidere dove applicare la protezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac994fb98d50a7e26f1b8142e77dc9ff771f6b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523258"
---
# <a name="deciding-where-to-enforce-security"></a>Decidere dove applicare la protezione

I compromessi sono intrinseci nell'applicazione della sicurezza. Un database può essere un luogo naturale per applicare la logica di sicurezza, dato che in definitiva i dati sono la cosa più importante da proteggere. Questa operazione, tuttavia, ha implicazioni significative sulle prestazioni. L'applicazione della sicurezza nel database può essere molto costosa, ridimensionata in modo non corretto e non è flessibile.

## <a name="enforcing-security-in-the-middle-tier"></a>Applicazione della sicurezza nel livello intermedio

La regola generale da seguire con le applicazioni multilivello scalabili mediante COM+ è che, laddove possibile, è necessario applicare una sicurezza dettagliata nell'applicazione COM+ a livello intermedio. Questa operazione consente di sfruttare appieno i servizi scalabili forniti da COM+. Applicare l'autenticazione al database solo quando è assolutamente necessario e valutare in modo completo le implicazioni relative alle prestazioni.

La situazione ottimale consiste nell'essere in grado di proteggere le tabelle di database in modo che l'applicazione COM+ sia in grado di accedervi con una propria identità. Il database deve semplicemente autenticare l'applicazione COM+ e considerarla attendibile per autenticare e autorizzare i client che accederanno ai dati. I vantaggi di questo approccio sono i seguenti:

-   Consente il pool di connessioni tra tutti i client, poiché le connessioni sono completamente generiche.
-   In genere ottimizza l'accesso ai dati, spesso un problema di soffocamento quando si ridimensionano le applicazioni.
-   Può ridurre al minimo il sovraccarico della logica per l'applicazione della sicurezza, in particolare se è possibile utilizzare la sicurezza dichiarativa basata sui ruoli.
-   Può garantire una grande flessibilità nei criteri di sicurezza. È possibile configurarlo e riconfigurarlo facilmente, come descritto in [amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md).

Tuttavia, come illustrato in [progettazione dei ruoli in modo efficiente](designing-roles-effectively.md), mentre i ruoli possono essere applicati in modo semplice ed efficace ad alcune relazioni utente-dati, non sono una soluzione universale per le decisioni di accesso alla sicurezza.

## <a name="enforcing-security-at-the-database"></a>Applicazione della sicurezza nel database

Nonostante la preferibilità dell'applicazione della sicurezza a livello intermedio, esistono diversi motivi per applicare la sicurezza al database, ad esempio:

-   Non si ha la possibilità di scegliere, forse per motivi legacy o forse perché la decisione non è semplicemente a portata di mano.
-   Il database è accessibile da un'ampia gamma di applicazioni e la relativa sicurezza non può essere configurata in base a una singola applicazione.
-   È possibile rendere il database protetto in modo prevedibile. Se si mantengono i dati aziendali critici in un database, è possibile tracciare un vagone e aiutarlo a controllare chi lo vede.
-   L'autenticazione dei client originali nel database consente la registrazione dettagliata di chi ha eseguito le operazioni nel database.
-   Alcuni dati sono associati in modo innato a utenti specifici e la logica di prendere decisioni di accesso con granularità fine può essere eseguita in modo più efficiente nel database stesso, vicino ai dati.

Quando si ha il lusso di progettare la sicurezza del database e dell'applicazione COM+ in parallelo, la maggior parte di questi problemi riguarda le caratteristiche dei dati stessi e la relativa relazione con gli utenti che vi accedono. Con i dati a cui è possibile accedere da categorie stimabili di utenti, è efficace controllare l'accesso nel livello intermedio usando i ruoli. Con i dati che sono strettamente associati a classi molto piccole di utenti, tali relazioni devono essere spesso espresse con i dati stessi e pertanto è necessario applicare una certa sicurezza al database.

### <a name="performance-implications-of-enforcing-security-at-the-database"></a>Implicazioni relative alle prestazioni dell'applicazione della sicurezza nel database

Se si esegue l'autenticazione o l'autorizzazione degli utenti nel database, l'identità utente deve essere propagata al database per supportare questa operazione. Se il database considera attendibile l'applicazione di livello intermedio a tale scopo, è possibile passare le informazioni di sicurezza dell'utente nei parametri. In caso contrario, la chiamata al database deve essere eseguita con l'identità dell'utente, ovvero l'applicazione server deve rappresentare il client. Questa operazione può avere implicazioni sulle prestazioni, come le seguenti:

-   La rappresentazione del client può essere molto più lenta rispetto all'esecuzione della chiamata direttamente nell'identità dell'applicazione. Per informazioni dettagliate, vedere [rappresentazione e delega del client](client-impersonation-and-delegation.md).
-   Non è possibile raggruppare in pool una connessione di database eseguita con un'identità utente specifica.
-   L'aggiunta della logica nel database esegue il rischio di creare un collo di bottiglia di ridimensionamento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scenari di base per la protezione dei dati nelle applicazioni multilivello](basic-scenarios-for-securing-data-in-multi-tier-applications.md)
</dt> <dt>

[Sicurezza delle applicazioni a più livelli](multi-tier-application-security.md)
</dt> </dl>

 

 



