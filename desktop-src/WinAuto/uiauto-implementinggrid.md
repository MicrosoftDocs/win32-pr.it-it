---
title: Pattern di controllo Grid
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IGridProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo Grid viene usato per supportare i controlli che fungono da contenitori per una raccolta di elementi figlio.
ms.assetid: c50fb6f7-884a-4147-a6b2-c59d787fc04b
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Grid
- Automazione interfaccia utente, pattern di controllo Grid
- Automazione interfaccia utente, IGridProvider
- IGridProvider
- implementazione di pattern di controllo Grid di automazione interfaccia utente
- Pattern di controllo Grid
- pattern di controllo, IGridProvider
- pattern di controllo, implementazione della griglia di automazione interfaccia utente
- pattern di controllo, griglia
- interfacce, IGridProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328d8536a367389a6d17422bd6f6476a3e82aa11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044477"
---
# <a name="grid-control-pattern"></a>Pattern di controllo Grid

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), incluse informazioni su proprietà e metodi. Il pattern di controllo **Grid** viene usato per supportare i controlli che fungono da contenitori per una raccolta di elementi figlio.

Gli elementi figlio di questo elemento devono implementare [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) ed essere organizzati in un sistema di coordinate logico bidimensionale che può essere attraversato da righe e colonne. Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IGridProvider**](#required-members-for-igridprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **Grid** , tenere presenti le linee guida e le convenzioni seguenti:

-   Le coordinate della griglia sono in base zero, con la cella in alto a sinistra o in alto a destra, in base alle impostazioni locali, con coordinate (0, 0).
-   Se una cella è vuota, è necessario che venga restituito un elemento di automazione interfaccia utente Microsoft per supportare la proprietà [**IGridItemProvider:: ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) per tale cella. Ciò è possibile quando il layout degli elementi figlio nella griglia è simile a una matrice irregolare (vedere l'esempio riportato di seguito).

    ![esempio di controllo griglia con coordinate vuote](images/grid.png)

-   Una griglia con un solo elemento è ancora necessaria per implementare [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) se è considerata logicamente una griglia. Il numero di elementi figlio nella griglia non ha importanza.
-   Le righe e le colonne nascoste, a seconda dell'implementazione del provider, possono essere caricate nell'albero di automazione interfaccia utente e pertanto verranno riflesse nelle proprietà [**IGridProvider:: RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) e [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) . Se le righe e colonne nascoste non sono ancora state caricate, non devono essere contate.
-   [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) non consente la modifica attiva di una griglia; Per abilitare questa funzionalità, è necessario implementare [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) .
-   Usare un [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) per restare in ascolto delle modifiche strutturali o di layout della griglia, ad esempio le celle che sono state aggiunte, rimosse o unite.
-   Usare un [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) per tenere traccia dell'attraversamento attraverso gli elementi o le celle di una griglia.

## <a name="required-members-for-igridprovider"></a>Membri obbligatori per **IGridProvider**

Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) .



| Membri obbligatori                                        | Tipo di membro | Note |
|---------------------------------------------------------|-------------|-------|
| [**RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount)       | Proprietà    | nessuno  |
| [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) | Proprietà    | nessuno  |
| [**GetItem**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-getitem)         | Metodo      | nessuno  |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Pattern di controllo GridItem](uiauto-implementinggriditem.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 




