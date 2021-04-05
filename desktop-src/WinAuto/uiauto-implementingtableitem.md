---
title: Pattern di controllo TableItem
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ITableItemProvider, incluse informazioni sui metodi. Il pattern di controllo TableItem viene usato per supportare i controlli figlio di contenitori che implementano ITableProvider.
ms.assetid: e00c7a58-410c-4818-8f61-57ee98527d6e
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo TableItem
- Automazione interfaccia utente, pattern di controllo TableItem
- Automazione interfaccia utente, ITableItemProvider
- ITableItemProvider
- implementazione di pattern di controllo TableItem di automazione interfaccia utente
- Pattern di controllo TableItem
- pattern di controllo, ITableItemProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente TableItem
- pattern di controllo, TableItem
- interfacce, ITableItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bae3e6d5379ec9a662e31ec6181476b112631381
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709277"
---
# <a name="tableitem-control-pattern"></a>Pattern di controllo TableItem

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), incluse informazioni sui metodi. Il pattern di controllo **TableItem** viene usato per supportare i controlli figlio di contenitori che implementano [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).

L'accesso alle singole funzionalità delle celle viene fornito dall'implementazione simultanea obbligatoria di [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider). Questo pattern di controllo è analogo a **IGridItemProvider** con la differenza che qualsiasi controllo che implementa [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) deve esporre a livello di codice la relazione tra la singola cella e le relative informazioni di riga e colonna. Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **ITableItemProvider**](#required-members-for-itableitemprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **TableItem** , tenere presenti le linee guida e le convenzioni seguenti:

-   Per la funzionalità degli elementi della griglia correlata, vedere [pattern di controllo GridItem](uiauto-implementinggriditem.md).

## <a name="required-members-for-itableitemprovider"></a>Membri obbligatori per **ITableItemProvider**

I metodi seguenti sono necessari per implementare l'interfaccia [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) .



| Membri obbligatori                                                               | Tipo di membro | Note |
|--------------------------------------------------------------------------------|-------------|-------|
| [**GetColumnHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getcolumnheaderitems) | Metodo      | nessuno  |
| [**GetRowHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getrowheaderitems)       | Metodo      | nessuno  |



 

Questo pattern di controllo non è associato a proprietà o eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Pattern di controllo Table](uiauto-implementingtable.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 




