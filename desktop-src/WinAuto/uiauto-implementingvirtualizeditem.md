---
title: Pattern di controllo VirtualizedItem
description: Descrive le linee guida e le convenzioni per l'implementazione di IVirtualizedItemProvider, incluse le informazioni su proprietà e metodi.
ms.assetid: 7a95e92f-7ccb-4c9b-8986-1d2de7038e47
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo VirtualizedItem
- Automazione interfaccia utente, pattern di controllo VirtualizedItem
- Automazione interfaccia utente,IVirtualizedItemProvider
- IVirtualizedItemProvider
- Implementazione Automazione interfaccia utente pattern di controllo VirtualizedItem
- Pattern di controllo VirtualizedItem
- pattern di controllo, IVirtualizedItemProvider
- pattern di controllo, implementazione Automazione interfaccia utente VirtualizedItem
- pattern di controllo, VirtualizedItem
- interfacce, IVirtualizedItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d883eec2e0f5fa4c4ede4c3fa2ef73770cc706114b6536ad002d11ff73f8ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997761"
---
# <a name="virtualizeditem-control-pattern"></a>Pattern di controllo VirtualizedItem

Descrive le linee guida e le convenzioni per l'implementazione [**di IVirtualizedItemProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)incluse le informazioni su proprietà e metodi. Il **pattern di controllo VirtualizedItem** viene usato per supportare gli elementi virtualizzati, ovvero gli elementi rappresentati da elementi di automazione segnaposto nell'albero Automazione interfaccia utente Microsoft.

Gli elementi virtualizzati possono includere elementi recuperati da un controllo che supporta il pattern di controllo [ItemContainer](uiauto-implementingitemcontainer.md) o un oggetto incorporato virtualizzato recuperato da un controllo che supporta il pattern [di controllo Text.](uiauto-implementingtextandtextrange.md) Il segnaposto per un elemento virtualizzato potrebbe non avere caricato dati per tutte le proprietà Automazione interfaccia utente e può restituire [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) in risposta alle query per le proprietà non disponibili. Il pattern di **controllo VirtualizedItem** fornisce un metodo per la realizzazione di un elemento virtuale in modo che siano disponibili informazioni complete per l'elemento e che sia possibile creare un elemento di automazione completo per l'elemento nella struttura Automazione interfaccia utente albero.

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IVirtualizedItemProvider**](#required-members-for-ivirtualizeditemprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern **di controllo VirtualizedItem,** tenere presente le linee guida e le convenzioni seguenti:

-   Qualsiasi Automazione interfaccia utente segnaposto che può essere virtualizzato deve supportare il pattern di controllo **VirtualizedItem** esponendo [**l'interfaccia IVirtualizedItemProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)
-   Quando [**viene chiamato IVirtualizedItemProvider::Realize,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) l'oggetto segnaposto deve essere aggiornato con implementazioni complete delle relative proprietà e pattern di controllo.
-   Quando [**viene chiamato IVirtualizedItemProvider::Realize,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) il provider può modificare il viewport in modo che l'elemento virtualizzato venga visualizzato. Non è necessario visualizzare l'elemento. Tuttavia, gli elementi non virtualizzati fuori schermo devono supportare il [**metodo IScrollItemProvider::ScrollIntoView.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview)

## <a name="required-members-for-ivirtualizeditemprovider"></a>Membri obbligatori per **IVirtualizedItemProvider**

Per implementare l'interfaccia [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) sono necessari i metodi e le proprietà seguenti.



| Membri obbligatori                                           | Tipo di membro | Note |
|------------------------------------------------------------|-------------|-------|
| [**Realizzare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) | Metodo      | Nessuno  |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Implementazione del pattern Automazione interfaccia utente ItemContainer](uiauto-implementingitemcontainer.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> <dt>

[Utilizzo di elementi virtualizzati](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




