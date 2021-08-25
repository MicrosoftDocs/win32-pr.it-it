---
title: Pattern di controllo Dock
description: Descrive le linee guida e le convenzioni per l'implementazione di IDockProvider, incluse le informazioni su proprietà e metodi. Il pattern di controllo Dock viene usato per esporre le proprietà di ancoraggio di un controllo all'interno di un contenitore di ancoraggio.
ms.assetid: a6ea269b-632e-48ce-ac3b-edd7cc34d986
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo dock
- Automazione interfaccia utente,ancorare il pattern di controllo
- Automazione interfaccia utente,IDockProvider
- IDockProvider
- implementazione di Automazione interfaccia utente pattern di controllo di ancoraggio
- pattern di controllo dock
- pattern di controllo, IDockProvider
- pattern di controllo, implementazione Automazione interfaccia utente dock
- pattern di controllo, ancoraggio
- interfacce, IDockProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb0afd6a291a9e26c43d1aff957c7b7e9cd8c752040a661551b8eaf5b12b86e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115101"
---
# <a name="dock-control-pattern"></a>Pattern di controllo Dock

Descrive le linee guida e le convenzioni per l'implementazione [**di IDockProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)incluse le informazioni su proprietà e metodi. Il **pattern di** controllo Dock viene usato per esporre le proprietà di ancoraggio di un controllo all'interno di un contenitore di ancoraggio.

Un contenitore di ancoraggio è un controllo che consente di disporre gli elementi figlio orizzontalmente e verticalmente, uno rispetto all'altro. L'immagine seguente mostra un contenitore di ancoraggio con due elementi figlio. Per esempi di controlli che implementano questo pattern di controllo, vedere [Tipi di controllo e pattern di controllo supportati.](uiauto-controlpatternmapping.md)

![Screenshot che mostra il contenitore di ancoraggio con due elementi figlio ancorati](images/dockxmpl.jpg)

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IDockProvider**](#required-members-for-idockprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **Dock,** tenere presente le linee guida e le convenzioni seguenti:

-   [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) non espone proprietà del contenitore di ancoraggio o proprietà dei controlli ancorati adiacenti al controllo corrente all'interno del contenitore di ancoraggio.
-   I controlli vengono ancorati reciprocamente in base al relativo ordine z corrente, ovvero più elevata è la posizione nell'ordine z, più lontano verrà inserito il controllo rispetto al bordo specificato del contenitore di ancoraggio.
-   Se il contenitore di ancoraggio viene ridimensionato, i controlli ancorati all'interno del contenitore verranno riposizionati e allineati allo stesso bordo a cui sono stati originariamente ancorati. I controlli ancorati verranno ridimensionati anche per riempire qualsiasi spazio all'interno del contenitore in base al comportamento di ancoraggio della relativa [**proprietà DockPosition.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) Ad esempio, se **viene specificato DockPosition \_ Top,** i lati sinistro e destro del controllo si espandono per riempire qualsiasi spazio disponibile. Se **viene specificato DockPosition \_ Fill,** tutti e quattro i lati del controllo verranno espansi per riempire qualsiasi spazio disponibile.
-   In un sistema con più monitor i controlli devono essere ancorati al lato sinistro o destro del monitor corrente. Se ciò non è possibile, devono essere ancorati al lato sinistro del monitor all'estrema sinistra o al lato destro del monitor all'estrema destra.

## <a name="required-members-for-idockprovider"></a>Membri obbligatori per **IDockProvider**

Le proprietà e i metodi seguenti sono necessari per l'implementazione [**dell'interfaccia IDockProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)



| Membri obbligatori                                                | Tipo di membro | Note |
|-----------------------------------------------------------------|-------------|-------|
| [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition)       | Proprietà    | Nessuno  |
| [**SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) | Metodo      | Nessuno  |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e relativi pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 




