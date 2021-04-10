---
title: Pattern di controllo Dock
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IDockProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo Dock viene usato per esporre le proprietà di ancoraggio di un controllo all'interno di un contenitore di ancoraggio.
ms.assetid: a6ea269b-632e-48ce-ac3b-edd7cc34d986
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Dock
- Automazione interfaccia utente, pattern di controllo Dock
- Automazione interfaccia utente, IDockProvider
- IDockProvider
- implementazione di pattern di controllo Dock di automazione interfaccia utente
- modelli di controllo Dock
- pattern di controllo, IDockProvider
- pattern di controllo, implementazione del dock di automazione interfaccia utente
- pattern di controllo, ancoraggio
- interfacce, IDockProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87381669889ca7dd33811a030a718448f4b79cb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855990"
---
# <a name="dock-control-pattern"></a>Pattern di controllo Dock

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider), incluse informazioni su proprietà e metodi. Il pattern di controllo **Dock** viene usato per esporre le proprietà di ancoraggio di un controllo all'interno di un contenitore di ancoraggio.

Un contenitore di ancoraggio è un controllo che consente di disporre gli elementi figlio orizzontalmente e verticalmente, uno rispetto all'altro. La figura seguente mostra un contenitore di ancoraggio con due elementi figlio. Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

![screenshot che mostra il contenitore di ancoraggio con due elementi figlio ancorati](images/dockxmpl.jpg)

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IDockProvider**](#required-members-for-idockprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **Dock** , tenere presenti le linee guida e le convenzioni seguenti:

-   [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) non espone le proprietà del contenitore di ancoraggio o le proprietà dei controlli ancorati adiacenti al controllo corrente all'interno del contenitore di ancoraggio.
-   I controlli vengono ancorati reciprocamente in base al relativo ordine z corrente, ovvero più elevata è la posizione nell'ordine z, più lontano verrà inserito il controllo rispetto al bordo specificato del contenitore di ancoraggio.
-   Se il contenitore di ancoraggio viene ridimensionato, i controlli ancorati all'interno del contenitore verranno riposizionati e allineati allo stesso bordo a cui sono stati originariamente ancorati. Anche i controlli ancorati vengono ridimensionati per riempire lo spazio all'interno del contenitore in base al comportamento di ancoraggio della relativa proprietà [**impostata su DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) . Se, ad esempio, si specifica **impostata su DockPosition \_ Top** , il lato sinistro e destro del controllo si espanderà in modo da riempire lo spazio disponibile. Se si specifica **impostata su DockPosition \_ Fill** , tutti e quattro i lati del controllo si espanderanno in modo da riempire lo spazio disponibile.
-   In un sistema con più monitor i controlli devono essere ancorati al lato sinistro o destro del monitor corrente. Se ciò non è possibile, devono essere ancorati al lato sinistro del monitor all'estrema sinistra o al lato destro del monitor all'estrema destra.

## <a name="required-members-for-idockprovider"></a>Membri obbligatori per **IDockProvider**

Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) .



| Membri obbligatori                                                | Tipo di membro | Note |
|-----------------------------------------------------------------|-------------|-------|
| [**Impostata su DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition)       | Proprietà    | nessuno  |
| [**SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) | Metodo      | nessuno  |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 




