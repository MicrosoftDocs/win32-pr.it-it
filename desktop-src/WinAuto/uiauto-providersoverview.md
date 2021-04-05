---
title: Cenni preliminari sui provider di automazione interfaccia utente
description: Questo argomento fornisce una panoramica del modo in cui gli sviluppatori di controlli implementano i provider di automazione interfaccia utente.
ms.assetid: 8928c889-0e0a-439f-87e8-a9d121fcf73f
keywords:
- Automazione interfaccia utente, panoramica provider
- Automazione interfaccia utente, tipi di provider
- Automazione interfaccia utente, concetti relativi ai provider
- provider, informazioni
- provider, tipi
- provider, concetti
- provider, elementi
- provider, navigazione
- provider, viste
- provider, Framework
- provider, frammenti
- provider, host
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f70a806fe33b16eed2555c123cc50f1f2b28da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955353"
---
# <a name="ui-automation-providers-overview"></a>Cenni preliminari sui provider di automazione interfaccia utente

Un provider di automazione interfaccia utente Microsoft è un oggetto software che espone un elemento dell'interfaccia utente di un'applicazione in modo che le applicazioni client di accessibilità possano recuperare le informazioni sull'elemento e richiamarne la funzionalità. In generale, ogni controllo o un altro elemento distinto in un'interfaccia utente dispone di un provider.

Microsoft include un provider per ognuno dei controlli standard forniti con Microsoft Win32, Windows Form e Windows Presentation Foundation (WPF). Ciò significa che i controlli standard vengono esposti automaticamente ai client di automazione interfaccia utente; non è necessario implementare interfacce di accessibilità per i controlli standard.

Se l'applicazione include controlli personalizzati, è necessario implementare i provider di automazione interfaccia utente per tali controlli per renderli accessibili alle applicazioni client di accessibilità. È anche necessario implementare i provider per tutti i controlli di terze parti che non includono un provider. È possibile implementare un provider implementando interfacce del provider di automazione interfaccia utente e interfacce del pattern di controllo.

Questo argomento fornisce una panoramica del modo in cui gli sviluppatori di controlli implementano i provider di automazione interfaccia utente. Include le sezioni seguenti.

-   [Tipi di provider](#types-of-providers)
-   [Concetti relativi al provider di automazione interfaccia utente](#ui-automation-provider-concepts)
    -   [Elementi](#elements)
    -   [Framework](#frameworks)
    -   [Frammenti](#fragments)
    -   [Host](#hosts)
-   [Argomenti correlati](#related-topics)

## <a name="types-of-providers"></a>Tipi di provider

I provider di automazione interfaccia utente rientrano in due categorie: provider lato server e provider lato client (o *proxy*).

Un provider lato server è un oggetto, ad esempio un controllo personalizzato, che contiene la propria implementazione nativa delle interfacce del provider di automazione interfaccia utente pertinenti. Un provider lato server comunica con le applicazioni client attraverso il limite di processo esponendo l'implementazione delle interfacce del provider al nucleo di automazione interfaccia utente, che consente di soddisfare le richieste dei client. Per ulteriori informazioni sui provider lato server, vedere [implementazione di un provider di automazione interfaccia utente di Server-Side](uiauto-serversideprovider.md).

Un provider lato client, o un proxy, è un oggetto che implementa le interfacce del provider di automazione interfaccia utente per conto di un controllo non include un'implementazione del provider completa autonomamente. Senza un proxy, questo controllo è in gran parte opaco per l'automazione dell'interfaccia utente, che può fornire solo le informazioni di base disponibili dall'handle di finestra (**HWND**), ad esempio la posizione del controllo. In genere, i provider proxy comunicano con l'applicazione attraverso il limite di processo inviando e ricevendo messaggi di Windows. Per ulteriori informazioni, vedere [implementazione di un provider di automazione interfaccia utente Client-Side (proxy)](uiauto-clientsideprovider.md).

## <a name="ui-automation-provider-concepts"></a>Concetti relativi al provider di automazione interfaccia utente

In questa sezione viene presentata una breve spiegazione di alcuni concetti chiave fondamentali per l'implementazione di provider di automazione interfaccia utente.

### <a name="elements"></a>Elementi

Gli elementi di automazione interfaccia utente sono parti dell'interfaccia utente, in genere finestre o controlli, visibili ai client di automazione interfaccia utente. ad esempio finestre delle applicazioni, riquadri, pulsanti, descrizioni comandi, caselle di riepilogo e voci di elenco.

Gli elementi di automazione interfaccia utente vengono esposti ai client sotto forma di albero. L'automazione interfaccia utente costruisce l'albero passando da un elemento a un altro. Lo spostamento viene abilitato dal provider per ogni elemento. Ogni elemento può puntare al proprio elemento padre, ai relativi elementi di pari livello e ai relativi primi e ultimi elementi figlio.

Un client può vedere l'albero di automazione interfaccia utente in tre visualizzazioni principali, come descritto nella tabella seguente:



| Visualizzazione         | Descrizione                                                    |
|--------------|----------------------------------------------------------------|
| Visualizzazione non elaborata     | Include tutti gli elementi.                                         |
| Visualizzazione controlli | Include gli elementi che sono controlli.                           |
| Visualizzazione contenuto | Include gli elementi di controllo che trasmettono informazioni all'utente. |



 

È responsabilità dell'implementazione del provider definire un elemento come elemento contenuto o elemento controllo. Gli elementi controllo possono essere anche elementi contenuto, mentre tutti gli elementi contenuto sono elementi controllo.

Per ulteriori informazioni sulla visualizzazione client dell'albero di, vedere [UI Automation Tree Overview](uiauto-treeoverview.md).

### <a name="frameworks"></a>Framework

Un framework è un componente che gestisce controlli figlio, hit testing e rendering in un'area dello schermo. Ad esempio, una finestra Win32, spesso denominata **HWND**, può fungere da Framework che contiene più elementi di automazione interfaccia utente, ad esempio una barra dei menu, una barra di stato e pulsanti.

I controlli contenitore Win32, ad esempio caselle di riepilogo e controlli visualizzazione albero, sono considerati Framework perché contengono il proprio codice per il rendering degli elementi figlio e l'esecuzione di hit testing su di essi. Al contrario, una casella di riepilogo WPF non è un Framework, perché il rendering e l'hit testing sono gestiti dalla finestra che lo contiene.

L'interfaccia utente di un'applicazione può essere costituita da Framework diversi. Ad esempio, un **HWND** in un'applicazione potrebbe contenere codice HTML dinamico (DHTML) che a sua volta può contenere un componente, ad esempio una casella combinata in un **HWND**.

### <a name="fragments"></a>Frammenti

Un sottoalbero completo di elementi di un particolare Framework è denominato frammento. L'elemento in corrispondenza del nodo radice del sottoalbero è definito radice del frammento. Una radice del frammento non ha un elemento padre, ma è ospitata in un altro Framework, in genere una finestra Win32 (**HWND**).

### <a name="hosts"></a>Hosts

Il nodo radice di ogni frammento deve essere ospitato in un elemento, in genere una finestra Win32 (**HWND**). L'eccezione è rappresentata dal desktop, che non è ospitato in nessun altro elemento. L'host di un controllo personalizzato è **HWND** del controllo stesso, non la finestra dell'applicazione o qualsiasi altra finestra che potrebbe contenere gruppi di controlli di primo livello.

L'host di un frammento svolge un ruolo importante nella fornitura dei servizi di automazione interfaccia utente. Consente lo spostamento alla radice del frammento e rende disponibili alcune proprietà predefinite in modo che il provider personalizzato debba implementarle.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di un provider di automazione interfaccia utente Client-Side](uiauto-clientsideprovider.md)
</dt> <dt>

[Implementazione di un provider di automazione interfaccia utente Server-Side](uiauto-serversideprovider.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 




