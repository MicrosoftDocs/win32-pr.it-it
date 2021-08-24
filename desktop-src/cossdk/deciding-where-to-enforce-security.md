---
description: I compromessi sono intrinseci nell'applicazione della sicurezza.
ms.assetid: f01573f3-aae6-400e-bdd9-6f34f4e262f6
title: Scelta della posizione in cui applicare la sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c13bb81a74b329c662370f24db51559c9dd83f0c1c521ba70dfdcb8be1c813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128772"
---
# <a name="deciding-where-to-enforce-security"></a>Scelta della posizione in cui applicare la sicurezza

I compromessi sono intrinseci nell'applicazione della sicurezza. Un database può essere un luogo naturale in cui inserire la logica di sicurezza, dato che in definitiva i dati sono la cosa più importante da proteggere. Tuttavia, questa operazione ha implicazioni significative sulle prestazioni. L'applicazione della sicurezza nel database può essere molto costosa, la scalabilità è scarsa ed è poco rigida.

## <a name="enforcing-security-in-the-middle-tier"></a>Applicazione della sicurezza nel livello intermedio

La regola generale da seguire con le applicazioni multilivello scalabili con COM+ è che, quando possibile, è consigliabile applicare la sicurezza dettagliata nell'applicazione COM+ a livello intermedio. In questo modo è possibile sfruttare appieno i servizi scalabili offerti da COM+. Applicare l'autenticazione al database solo quando è assolutamente necessario e valutare completamente le implicazioni in termini di prestazioni di questa operazione.

La situazione ottimale è la possibilità di proteggere le tabelle di database in modo che l'applicazione COM+ sia in grado di accedervi con la propria identità. Il database deve semplicemente autenticare l'applicazione COM+ e considerarla attendibile per autenticare e autorizzare correttamente i client che accederanno ai dati. I vantaggi di questo approccio sono i seguenti:

-   Consente il pool di connessioni tra tutti i client, poiché le connessioni sono completamente generiche.
-   In genere ottimizza l'accesso ai dati, spesso un punto problematico per il ridimensionamento delle applicazioni.
-   Può ridurre al minimo l'overhead della logica per l'applicazione della sicurezza, in particolare se è possibile usare la sicurezza dichiarativa basata sui ruoli.
-   Può offrire una grande flessibilità nei criteri di sicurezza. È possibile configurarlo e riconfigurarlo facilmente, come descritto in [Amministrazione della sicurezza basata sui ruoli.](role-based-security-administration.md)

Tuttavia, come illustrato [in](designing-roles-effectively.md)Progettazione efficace dei ruoli, anche se i ruoli possono essere applicati in modo semplice ed efficace ad alcune relazioni utente-dati, non sono una soluzione universale per le decisioni relative all'accesso di sicurezza.

## <a name="enforcing-security-at-the-database"></a>Applicazione della sicurezza nel database

Nonostante la preferenza di applicare la sicurezza a livello intermedio, esistono diversi motivi per applicare la sicurezza al database, ad esempio:

-   Non è possibile scegliere, ad esempio per motivi legacy o forse perché la decisione non è semplicemente nelle mani dell'utente.
-   Il database è accessibile da un'ampia gamma di applicazioni e la sicurezza non può essere configurata in base a una singola applicazione.
-   Un database può essere reso protetto in modo prevedibile. Se si mantengono i dati aziendali critici in un database, è possibile creare un'organizzazione stretta intorno a esso e controllare chi può vederlo.
-   L'autenticazione dei client originali nel database consente la registrazione dettagliata degli utenti che hanno eseguito le operazioni nel database.
-   Alcuni dati sono associati in modo innato a utenti specifici e la logica di prendere decisioni di accesso estremamente granulari potrebbe essere eseguita in modo più efficiente nel database stesso, vicino ai dati.

Quando si ha il massimo della progettazione della sicurezza del database e dell'applicazione COM+ in tandem, la maggior parte di questi problemi riguarda le caratteristiche dei dati stessi e la relazione con gli utenti che vi accedono. Con i dati accessibili da categorie stimabili di utenti, è efficiente controllare l'accesso nel livello intermedio usando i ruoli. Con i dati associati a classi molto piccole di utenti, tali relazioni devono spesso essere espresse con i dati stessi e pertanto è necessario applicare una certa sicurezza al database.

### <a name="performance-implications-of-enforcing-security-at-the-database"></a>Implicazioni per le prestazioni dell'applicazione della sicurezza nel database

Se si autenticano o autorizzano utenti nel database, l'identità utente deve essere propagata al database per supportare questa operazione. Se il database considera attendibile l'applicazione di livello intermedio a tale scopo, è possibile passare le informazioni di sicurezza utente nei parametri. In caso contrario, la chiamata al database deve essere effettuata con l'identità dell'utente, vale a dire che l'applicazione server deve rappresentare il client. Ciò può avere implicazioni in termini di prestazioni, ad esempio:

-   La rappresentazione del client può essere molto più lenta rispetto all'esecuzione della chiamata direttamente sotto l'identità dell'applicazione. Per altri dettagli, vedere [Rappresentazione e delega del client.](client-impersonation-and-delegation.md)
-   Non è possibile eseguire il pool di una connessione di database effettuata con un'identità utente specifica.
-   L'aggiunta di logica nel database stesso rischia di creare un collo di bottiglia per il ridimensionamento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scenari di base per la protezione dei dati in applicazioni multilivello](basic-scenarios-for-securing-data-in-multi-tier-applications.md)
</dt> <dt>

[Sicurezza delle applicazioni multilivello](multi-tier-application-security.md)
</dt> </dl>

 

 



