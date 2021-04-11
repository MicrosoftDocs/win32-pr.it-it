---
description: Si usa la sicurezza basata sui ruoli per stabilire un criterio di autorizzazione, che determina quali client o client possono entrare e con quale autorità. Si decide chi deve essere in grado di eseguire le azioni e accedere alle risorse.
ms.assetid: 8fc27fe1-e50a-44ba-a595-70b1fe463e24
title: Utilizzo dei ruoli per l'autorizzazione client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ae748ddfec438a79e3d0440a00ed7c2f672aed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127006"
---
# <a name="using-roles-for-client-authorization"></a>Utilizzo dei ruoli per l'autorizzazione client

Si usa la sicurezza basata sui ruoli per stabilire un criterio di autorizzazione, che determina quali client o client possono entrare e con quale autorità. Si decide chi deve essere in grado di eseguire le azioni e accedere alle risorse.

I ruoli facilitano questa operazione agendo come un meccanismo di controllo di accesso richiamato ogni volta che un utente tenta di accedere a una risorsa dell'applicazione. Un ruolo è fondamentalmente un elenco di utenti, più precisamente, una categoria simbolica di utenti che condividono lo stesso privilegio di sicurezza. Quando si assegna un ruolo a una risorsa dell'applicazione, si concede l'autorizzazione di accesso per tale risorsa a chiunque sia un membro di tale ruolo.

Pertanto, è possibile definire un privilegio di sicurezza molto particolare dichiarando come ruolo e quindi assegnando il ruolo a risorse specifiche. Quando l'applicazione viene distribuita, l'amministratore di sistema può popolare il ruolo con utenti e gruppi di utenti effettivi. Quando viene eseguita l'applicazione, COM+ applica i criteri eseguendo i controlli del ruolo.

Fondamentalmente, i ruoli consentono di proteggere il codice, ovvero i metodi che possono essere chiamati dai client di un'applicazione COM+. L'appartenenza al ruolo viene controllata ogni volta che un client tenta di chiamare un metodo esposto da un componente in un'applicazione. Se il chiamante si trova in un ruolo assegnato al metodo chiamato, o alla risorsa, la chiamata ha esito positivo; in caso contrario, l'operazione avrà esito negativo.

## <a name="declarative-role-based-security"></a>Sicurezza dichiarativa Role-Based

Con la sicurezza dichiarativa basata sui ruoli, si dichiarano a livello amministrativo i ruoli, usando lo strumento di amministrazione Servizi componenti o le funzioni amministrative, e li si assegnano a livello amministrativo alle risorse dell'applicazione. La posizione e la modalità di impostazione della sicurezza dichiarativa determinano dove vengono disegnati i limiti di sicurezza per l'applicazione. Per informazioni dettagliate, vedere [limiti di sicurezza](security-boundaries.md).

È possibile assegnare un determinato ruolo all'intera applicazione, a un particolare componente, a una particolare interfaccia in un componente o a un particolare metodo su un'interfaccia. Le assegnazioni di ruolo vengono ereditate dalla catena di inclusione naturale, ovvero se si assegna un ruolo a un componente, questo viene assegnato in modo implicito a ogni interfaccia e metodo esposto da tale componente.

Con la disponibilità di assegnazioni di ruolo a livello di metodo, è possibile proteggere in modo efficace i componenti e le interfacce che non sono state progettate tenendo conto della sicurezza. Tuttavia, se i metodi non sono a protezione diretta con assegnazioni di ruolo dichiarative, potrebbe essere necessario eseguire il controllo del ruolo a livello di codice. È in genere consigliabile tenere in considerazione la sicurezza quando si decide come scomporre le funzionalità aziendali tramite i metodi; in caso contrario, potrebbe essere necessario aggiungere un codice correlato alla sicurezza nell'ultimo minuto.

Per le procedure dettagliate per l'impostazione della sicurezza basata sui ruoli, vedere [configurazione Role-Based sicurezza](configuring-role-based-security.md).

## <a name="programmatic-security"></a>Sicurezza a livello di codice

In alcuni casi è possibile che si desideri inserire la logica di sicurezza nei componenti di, pur continuando a utilizzare la protezione basata sui ruoli. È possibile che non sia possibile, o scegliere di non eseguire, il factoring di tutte le decisioni di accesso tramite metodi. Si supponga, ad esempio, di disporre di una risorsa dell'applicazione privata, ad esempio un database specifico, per consentire l'accesso solo a alcuni chiamanti di un metodo, esclusi gli altri. In alternativa, è possibile che si disponga di un solo metodo TransferMoney e si desidera limitare alcuni chiamanti limitando la quantità che è possibile trasferire.

In questi casi, è possibile eseguire il controllo dei ruoli nel codice. Viene fornita un'API semplice, che consente di controllare se è attivata la sicurezza e se un chiamante o un utente specifico si trova in un determinato ruolo. Questa funzionalità è disponibile solo quando è abilitata la sicurezza basata sui ruoli. Ciò significa che è comunque possibile usufruire della sicurezza dichiarativa basata sui ruoli dove è sufficiente, quindi è possibile estenderla a livello di codice a un livello di granularità più preciso quando necessario.

Inoltre, quando si usa la sicurezza basata sui ruoli, è possibile accedere a livello di codice alle informazioni relative a tutti i chiamanti upstream nella catena di chiamate al componente. Questa operazione è particolarmente utile quando si vuole contenere una audit trail dettagliata.

Per le descrizioni di come eseguire il controllo del ruolo nel codice e come accedere alle informazioni sul contesto delle chiamate di sicurezza, vedere [sicurezza dei componenti programmatici](programmatic-component-security.md).

## <a name="authorization-and-authentication"></a>Autorizzazione e autenticazione

Un'autorizzazione significativa presuppone che si sia certi che i client siano effettivamente quelli che affermano di essere. La verifica dell'identità del client viene gestita separatamente da un servizio di autenticazione. Senza l'autenticazione, i chiamanti vengono in pratica rilasciati nel sistema Honor. Per le descrizioni dell'autenticazione in quanto influisca sulle applicazioni COM+, vedere [autenticazione client](client-authentication.md).

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

 

 



