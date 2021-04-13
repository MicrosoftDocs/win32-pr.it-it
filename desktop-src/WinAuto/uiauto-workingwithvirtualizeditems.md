---
title: Utilizzo degli elementi virtualizzati
description: Questo argomento descrive come usare la funzionalità fornita dai pattern di controllo ItemContainer e VirtualizedItem per trovare e recuperare informazioni sugli elementi virtualizzati.
ms.assetid: e1898ba0-5ffa-4c61-b378-c7ef7c4a2c52
keywords:
- client, elementi virtualizzati di automazione interfaccia utente
- client, elementi virtualizzati
- client, pattern di controllo
- client, pattern di controllo VirtualizedItem
- client, pattern di controllo ItemContainer
- client, pattern di controllo VirtualizedItem di automazione interfaccia utente
- client, pattern di controllo di automazione interfaccia utente
- client, pattern di controllo ItemContainer di automazione interfaccia utente
- Automazione interfaccia utente, elementi virtualizzati
- Automazione interfaccia utente, pattern di controllo
- Automazione interfaccia utente, pattern di controllo VirtualizedItem
- Automazione interfaccia utente, pattern di controllo ItemContainer
- Pattern di controllo VirtualizedItem
- Pattern di controllo ItemContainer
- pattern di controllo, VirtualizedItem
- pattern di controllo, ItemContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb29232b06304079ad5b9dfdfb589ad510a5b51f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331404"
---
# <a name="working-with-virtualized-items"></a>Utilizzo degli elementi virtualizzati

Questo argomento descrive come usare la funzionalità fornita dai pattern di controllo [ItemContainer](uiauto-implementingitemcontainer.md) e [VirtualizedItem](uiauto-implementingvirtualizeditem.md) per trovare e recuperare informazioni sugli elementi virtualizzati.

-   [Panoramica della virtualizzazione](#overview-of-virtualization)
-   [Come un controllo supporta la virtualizzazione](#how-a-control-supports-virtualization)
-   [Come i client trovano e realizzano elementi virtualizzati](#how-clients-find-and-realize-virtualized-items)
-   [Esempio](#example)
-   [Argomenti correlati](#related-topics)

## <a name="overview-of-virtualization"></a>Panoramica della virtualizzazione

I controlli che contengono un numero elevato di elementi figlio possono utilizzare la virtualizzazione per gestire in modo efficiente gli elementi. Con la virtualizzazione, il controllo mantiene le informazioni complete in memoria solo per un subset di elementi in un determinato momento. In genere, il subset include solo gli elementi attualmente visibili all'utente. Le informazioni complete sugli elementi virtualizzati rimanenti vengono mantenute nello spazio di archiviazione e vengono caricate in memoria, o realizzate, perché il controllo lo richiede, ad esempio, perché i nuovi elementi diventano visibili all'utente.

I controlli che usano la virtualizzazione rappresentano una sfida perché solo gli elementi realizzati sono completamente disponibili come elementi di automazione interfaccia utente Microsoft nell'albero di automazione interfaccia utente. Gli elementi virtualizzati non esistono nell'albero, quindi le informazioni su di essi non sono disponibili per i client. Per recuperare informazioni sugli elementi virtualizzati, i client devono avere un modo per forzare l'automazione dell'interfaccia utente a passare la richiesta per realizzare gli elementi al controllo. Una volta realizzati gli elementi, l'automazione interfaccia utente può creare elementi di automazione interfaccia utente. Automazione interfaccia utente include due pattern di controllo per consentire ai client di usare elementi virtualizzati: [ItemContainer](uiauto-implementingitemcontainer.md) e [VirtualizedItem](uiauto-implementingvirtualizeditem.md).

## <a name="how-a-control-supports-virtualization"></a>Come un controllo supporta la virtualizzazione

Qualsiasi controllo che può contenere elementi virtualizzati deve supportare il pattern di controllo [ItemContainer](uiauto-implementingitemcontainer.md) . Inoltre, qualsiasi elemento che può essere virtualizzato deve supportare il pattern di controllo [VirtualizedItem](uiauto-implementingvirtualizeditem.md) . Le funzionalità esposte dai pattern di controllo ItemContainer e VirtualizedItem sono accessibili ai client tramite le interfacce [**IUIAutomationItemContainerPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationitemcontainerpattern) e [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) .

## <a name="how-clients-find-and-realize-virtualized-items"></a>Come i client trovano e realizzano elementi virtualizzati

I client possono usare il metodo [**IUIAutomationItemContainerPattern:: FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) per cercare gli elementi figlio nel contenitore in base al valore di una determinata proprietà. Il metodo può anche recuperare il primo elemento nel contenitore o l'elemento che segue l'elemento specificato. Se viene trovato un elemento figlio corrispondente, **FindItemByProperty** recupera un'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per l'elemento. Tuttavia, se l'elemento figlio è virtualizzato, l'interfaccia **IUIAutomationElement** è un segnaposto. L'errore [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) si verifica quando il client tenta di usare l'interfaccia **IUIAutomationElement** per recuperare i valori di proprietà o chiamare metodi non ancora disponibili. Le proprietà o i metodi disponibili tramite un segnaposto dipendono dall'implementazione del controllo. L'unico requisito per un segnaposto è supportare l'interfaccia [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) .

L'errore [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) indica al client che un elemento può essere virtualizzato. Il client deve rispondere recuperando l'interfaccia [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) per l'elemento e quindi realizzando l'elemento chiamando il metodo [**IUIAutomationVirtualizedItemPattern:: réalisateur**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) . Se l'operazione ha esito positivo, l'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) è completamente funzionante con tutte le proprietà appropriate disponibili.

A seconda dell'implementazione del controllo, la chiamata a [**IUIAutomationVirtualizedItemPattern:: rende**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) possibile il controllo per scorrere l'elemento nella visualizzazione. Tuttavia, un client non deve basarsi sullo scorrimento della visualizzazione o rendere visibile l'elemento. Per assicurarsi che l'elemento sia visibile, il client può usare il metodo [**IUIAutomationScrollItemPattern:: ScrollIntoView**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollitempattern-scrollintoview) .

## <a name="example"></a>Esempio

Per un esempio di codice che illustra come usare il supporto di automazione interfaccia utente per la virtualizzazione, vedere [come recuperare un elemento virtualizzato](uiauto-howto-retrieve-virtualized-item.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




