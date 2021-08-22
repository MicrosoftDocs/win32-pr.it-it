---
title: Utilizzo di elementi virtualizzati
description: Questo argomento descrive come usare le funzionalità fornite dai pattern di controllo ItemContainer e VirtualizedItem per trovare e recuperare informazioni sugli elementi virtualizzati.
ms.assetid: e1898ba0-5ffa-4c61-b378-c7ef7c4a2c52
keywords:
- client, Automazione interfaccia utente virtualizzati
- client, elementi virtualizzati
- client, pattern di controllo
- client, pattern di controllo VirtualizedItem
- client, pattern di controllo ItemContainer
- client, Automazione interfaccia utente di controllo VirtualizedItem
- client, Automazione interfaccia utente pattern di controllo
- client, Automazione interfaccia utente pattern di controllo ItemContainer
- Automazione interfaccia utente, elementi virtualizzati
- Automazione interfaccia utente,pattern di controllo
- Automazione interfaccia utente,Pattern di controllo VirtualizedItem
- Automazione interfaccia utente,Pattern di controllo ItemContainer
- Pattern di controllo VirtualizedItem
- Pattern di controllo ItemContainer
- pattern di controllo, VirtualizedItem
- pattern di controllo, ItemContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2c0e84f91af6bcaadef5af373b73057fb4a137480255f3ee1af4456e45eaf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570371"
---
# <a name="working-with-virtualized-items"></a>Utilizzo di elementi virtualizzati

Questo argomento descrive come usare le funzionalità fornite dai pattern di controllo [ItemContainer](uiauto-implementingitemcontainer.md) e [VirtualizedItem](uiauto-implementingvirtualizeditem.md) per trovare e recuperare informazioni sugli elementi virtualizzati.

-   [Panoramica della virtualizzazione](#overview-of-virtualization)
-   [Supporto della virtualizzazione da parte di un controllo](#how-a-control-supports-virtualization)
-   [Come i client trovano e realizzano gli elementi virtualizzati](#how-clients-find-and-realize-virtualized-items)
-   [Esempio](#example)
-   [Argomenti correlati](#related-topics)

## <a name="overview-of-virtualization"></a>Panoramica della virtualizzazione

I controlli che contengono un numero elevato di elementi figlio possono usare la virtualizzazione per gestire in modo efficiente gli elementi. Con la virtualizzazione, il controllo mantiene le informazioni complete in memoria solo per un subset di elementi in un determinato momento. In genere, il subset include solo gli elementi attualmente visibili all'utente. Le informazioni complete sugli elementi virtualizzati rimanenti vengono mantenute nella memoria e caricate in memoria o realizzati, in base alle esigenze del controllo, ad esempio quando i nuovi elementi diventano visibili all'utente.

I controlli che usano la virtualizzazione rappresentano una sfida perché solo gli elementi realizzati sono completamente disponibili come elementi Automazione interfaccia utente Microsoft nell'Automazione interfaccia utente albero. Gli elementi virtualizzati non esistono nell'albero, quindi le relative informazioni non sono disponibili per i client. Per recuperare informazioni sugli elementi virtualizzati, i client necessitano di un modo per forzare Automazione interfaccia utente passare la richiesta per realizzare gli elementi al controllo. Dopo che gli elementi sono stati realizzati, Automazione interfaccia utente creare Automazione interfaccia utente per gli elementi. Automazione interfaccia utente include due pattern di controllo per consentire ai client di usare elementi virtualizzati: [ItemContainer](uiauto-implementingitemcontainer.md) [e VirtualizedItem.](uiauto-implementingvirtualizeditem.md)

## <a name="how-a-control-supports-virtualization"></a>Supporto della virtualizzazione da parte di un controllo

Qualsiasi controllo che può contenere elementi virtualizzati deve supportare il pattern [di controllo ItemContainer.](uiauto-implementingitemcontainer.md) Inoltre, qualsiasi elemento che può essere virtualizzato deve supportare il pattern [di controllo VirtualizedItem.](uiauto-implementingvirtualizeditem.md) La funzionalità esposta dai pattern di controllo ItemContainer e VirtualizedItem è accessibile ai client tramite le interfacce [**IUIAutomationItemContainerPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationitemcontainerpattern) e [**IUIAutomationVirtualizedItemPattern.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern)

## <a name="how-clients-find-and-realize-virtualized-items"></a>Come i client trovano e realizzano gli elementi virtualizzati

I client possono usare il metodo [**IUIAutomationItemContainerPattern::FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) per cercare elementi figlio nel contenitore in base al valore di una determinata proprietà. Il metodo può anche recuperare il primo elemento nel contenitore o l'elemento che segue l'elemento specificato. Se viene trovato un elemento figlio corrispondente, **FindItemByProperty** recupera [**un'interfaccia IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per l'elemento. Tuttavia, se l'elemento figlio è virtualizzato, **l'interfaccia IUIAutomationElement** è un segnaposto. [**L'errore \_ UIA E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) si verifica quando il client tenta di usare l'interfaccia **IUIAutomationElement** per recuperare i valori delle proprietà o chiamare metodi non ancora disponibili. Le proprietà o i metodi disponibili tramite un segnaposto dipendono dall'implementazione del controllo. L'unico requisito per un segnaposto è supportare [**l'interfaccia IUIAutomationVirtualizedItemPattern.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern)

[**L'errore \_ UIA E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) indica al client che un elemento può essere virtualizzato. Il client deve rispondere recuperando l'interfaccia [**IUIAutomationVirtualizedItemPattern per**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) l'elemento e quindi realizzando l'elemento chiamando il metodo [**IUIAutomationVirtualizedItemPattern::Realize.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) Se l'operazione riesce, [**l'interfaccia IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) è completamente funzionante con tutte le proprietà appropriate disponibili.

A seconda dell'implementazione del controllo, la chiamata a [**IUIAutomationVirtualizedItemPattern::Realize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) può causare lo scorrimento dell'elemento nella visualizzazione da parte del controllo. Tuttavia, un client non deve basarsi sullo scorrimento dell'elemento nella visualizzazione o reso visibile. Per assicurarsi che l'elemento sia visibile, il client può usare il metodo [**IUIAutomationScrollItemPattern::ScrollIntoView.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollitempattern-scrollintoview)

## <a name="example"></a>Esempio

Per un esempio di codice che illustra come usare il Automazione interfaccia utente per la virtualizzazione, vedere [Come recuperare un elemento virtualizzato.](uiauto-howto-retrieve-virtualized-item.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




