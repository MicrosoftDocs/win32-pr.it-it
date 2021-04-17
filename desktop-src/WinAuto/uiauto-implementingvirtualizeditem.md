---
title: Pattern di controllo VirtualizedItem
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IVirtualizedItemProvider, incluse informazioni su proprietà e metodi.
ms.assetid: 7a95e92f-7ccb-4c9b-8986-1d2de7038e47
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo VirtualizedItem
- Automazione interfaccia utente, pattern di controllo VirtualizedItem
- Automazione interfaccia utente, IVirtualizedItemProvider
- IVirtualizedItemProvider
- implementazione di pattern di controllo VirtualizedItem di automazione interfaccia utente
- Pattern di controllo VirtualizedItem
- pattern di controllo, IVirtualizedItemProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente VirtualizedItem
- pattern di controllo, VirtualizedItem
- interfacce, IVirtualizedItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8dac9e34dd9bff5d0ba2d245aa2fb8de621f40a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104222097"
---
# <a name="virtualizeditem-control-pattern"></a>Pattern di controllo VirtualizedItem

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider), incluse informazioni su proprietà e metodi. Il pattern di controllo **VirtualizedItem** viene usato per supportare elementi virtualizzati, ovvero elementi rappresentati da elementi di automazione segnaposto nell'albero di automazione interfaccia utente Microsoft.

Gli elementi virtualizzati possono includere elementi recuperati da un controllo che supporta il pattern di controllo [ItemContainer](uiauto-implementingitemcontainer.md) o un oggetto incorporato virtualizzato recuperato da un controllo che supporta il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) . Il segnaposto di un elemento virtualizzato potrebbe non avere caricato i dati per tutte le proprietà di automazione interfaccia utente e può restituire l' [**\_ \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) e la restituzione in risposta a query per le proprietà che non sono disponibili. Il pattern di controllo **VirtualizedItem** fornisce un metodo per la realizzazione di un elemento virtuale in modo da rendere disponibili le informazioni complete per l'elemento ed è possibile creare un elemento di automazione completo per l'elemento nell'albero di automazione interfaccia utente.

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IVirtualizedItemProvider**](#required-members-for-ivirtualizeditemprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **VirtualizedItem** , tenere presenti le linee guida e le convenzioni seguenti:

-   Qualsiasi elemento segnaposto di automazione interfaccia utente che può essere virtualizzato deve supportare il pattern di controllo **VirtualizedItem** esponendo l'interfaccia [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) .
-   Quando viene chiamato [**IVirtualizedItemProvider:: realizzate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) , l'oggetto segnaposto deve essere aggiornato con implementazioni complete delle proprietà e dei pattern di controllo.
-   Quando viene chiamato [**IVirtualizedItemProvider:: réalisateur**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) , il provider può modificare il viewport in modo da visualizzare l'elemento virtualizzato. Non è necessario portare l'elemento nella visualizzazione. gli elementi non virtualizzati, tuttavia, devono supportare il metodo [**IScrollItemProvider:: ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) .

## <a name="required-members-for-ivirtualizeditemprovider"></a>Membri obbligatori per **IVirtualizedItemProvider**

Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) .



| Membri obbligatori                                           | Tipo di membro | Note |
|------------------------------------------------------------|-------------|-------|
| [**Tenere presente**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) | Metodo      | nessuno  |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Implementazione del pattern di controllo ItemContainer di automazione interfaccia utente](uiauto-implementingitemcontainer.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> <dt>

[Utilizzo degli elementi virtualizzati](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




