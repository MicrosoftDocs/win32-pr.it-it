---
description: La sicurezza basata sui ruoli viene utilizzata per stabilire un criterio di autorizzazione, determinando il client o i client da consentire e con quale autorità. Si sta decidendo chi deve essere in grado di eseguire le azioni e di accedere alle risorse.
ms.assetid: 8fc27fe1-e50a-44ba-a595-70b1fe463e24
title: Uso dei ruoli per l'autorizzazione client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a808abc08d5360ba0b7fae0a7c31af80a4cab28c43e6014076c549204e6f28e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499646"
---
# <a name="using-roles-for-client-authorization"></a>Uso dei ruoli per l'autorizzazione client

La sicurezza basata sui ruoli viene utilizzata per stabilire un criterio di autorizzazione, determinando il client o i client da consentire e con quale autorità. Si sta decidendo chi deve essere in grado di eseguire le azioni e di accedere alle risorse.

I ruoli facilitano questa operazione fungendo da meccanismo di controllo di accesso richiamato ogni volta che un utente tenta di accedere a qualsiasi risorsa dell'applicazione. Un ruolo è fondamentalmente un elenco di utenti, più precisamente una categoria simbolica di utenti che condividono lo stesso privilegio di sicurezza. Quando si assegna un ruolo a una risorsa dell'applicazione, si concede l'autorizzazione di accesso per tale risorsa a chiunque sia membro di tale ruolo.

È quindi possibile definire un privilegio di sicurezza molto particolare dichiarandolo come ruolo e assegnando il ruolo a risorse specifiche. Quando l'applicazione viene distribuita, l'amministratore di sistema può popolare il ruolo con utenti e gruppi di utenti effettivi. Quando l'applicazione viene eseguita, COM+ applica i criteri eseguendo controlli del ruolo.

Fondamentalmente, i ruoli consentono di proteggere il codice, ovvero i metodi che possono essere chiamati dai client di un'applicazione COM+. L'appartenenza al ruolo viene verificata ogni volta che un client tenta di chiamare un metodo esposto da un componente in un'applicazione. Se il chiamante è in un ruolo assegnato al metodo o alla risorsa chiamata, la chiamata ha esito positivo; in caso contrario, l'operazione ha esito negativo.

## <a name="declarative-role-based-security"></a>Sicurezza Role-Based dichiarativa

Con la sicurezza dichiarativa basata sui ruoli, si dichiarano a livello amministrativo i ruoli, usando lo strumento amministrativo Servizi componenti o le funzioni amministrative, e li si assegnano a livello amministrativo alle risorse dell'applicazione. Dove e come si imposta la sicurezza dichiarativa determineranno dove vengono tracciati i limiti di sicurezza per l'applicazione. Per altre informazioni, vedere [Limiti di sicurezza](security-boundaries.md).

È possibile assegnare un determinato ruolo all'intera applicazione, a un componente specifico, a una particolare interfaccia in un componente o a un metodo specifico in un'interfaccia. Le assegnazioni di ruolo vengono ereditate lungo la catena naturale di inclusione, ovvero se si assegna un ruolo a un componente, viene assegnato in modo implicito a ogni interfaccia e metodo esposto da tale componente.

Con la disponibilità delle assegnazioni di ruolo a livello di metodo, è possibile proteggere in modo efficace componenti e interfacce che non sono stati progettati in base alla sicurezza. Tuttavia, se i metodi stessi non sono a protezione diretta con assegnazioni di ruolo dichiarative, potrebbe essere necessario eseguire il controllo dei ruoli a livello di codice. È in genere consigliabile tenere presente la sicurezza quando si decide come fattoriare le funzionalità aziendali tramite i metodi. In caso contrario, è possibile aggiungere codice correlato alla sicurezza all'ultimo minuto.

Per procedure dettagliate per l'impostazione della sicurezza basata sui ruoli, vedere [Configuring Role-Based Security](configuring-role-based-security.md).

## <a name="programmatic-security"></a>Sicurezza a livello di codice

In alcuni casi può essere necessario inserire la logica di sicurezza nei componenti pur continuando a usare la sicurezza basata sui ruoli. Potrebbe non essere possibile o scegliere di non prendere in fattore tutte le decisioni di accesso tramite metodi. Ad esempio, si potrebbe avere una risorsa dell'applicazione privata, ad esempio un database specifico, a cui si vuole consentire l'accesso solo ad alcuni chiamanti di un metodo escludendo altri. Oppure si potrebbe avere un singolo metodo TransferMoney e si vuole limitare alcuni chiamanti limitando la quantità che possono trasferire.

In questi casi, è possibile eseguire il controllo dei ruoli nel codice. Viene fornita una semplice API che consente di controllare se la sicurezza è attivata e se un chiamante o un utente specifico è in un determinato ruolo. Questa funzionalità è disponibile solo quando è abilitata la sicurezza basata sui ruoli. Ciò significa che è comunque possibile sfruttare la sicurezza dichiarativa basata sui ruoli in cui è sufficiente e quindi estenderla a livello di codice a un livello di granularità più fine quando necessario.

Inoltre, quando si usa la sicurezza basata sui ruoli, si ha accesso a livello di codice alle informazioni relative a tutti i chiamanti upstream nella catena di chiamate al componente. Ciò è particolarmente utile quando si vuole mantenere un'audit trail.

Per descrizioni su come eseguire il controllo dei ruoli nel codice e su come accedere alle informazioni sul contesto delle chiamate di sicurezza, vedere Sicurezza dei componenti a [livello di codice.](programmatic-component-security.md)

## <a name="authorization-and-authentication"></a>Autorizzazione e autenticazione

L'autorizzazione significativa presuppone che si sia certi che i client siano effettivamente quelli che affermano di essere. La verifica dell'identità client viene gestita separatamente da un servizio di autenticazione. Senza autenticazione, si consente fondamentalmente ai chiamanti di eseguire l'accesso al sistema honor. Per descrizioni dell'autenticazione in quanto influisce sulle applicazioni COM+, vedere [Autenticazione client](client-authentication.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione efficace dei ruoli](designing-roles-effectively.md)
</dt> <dt>

[Limiti di sicurezza](security-boundaries.md)
</dt> <dt>

[Informazioni sul contesto delle chiamate di sicurezza](security-call-context-information.md)
</dt> <dt>

[Proprietà del contesto di sicurezza](security-context-property.md)
</dt> </dl>

 

 



