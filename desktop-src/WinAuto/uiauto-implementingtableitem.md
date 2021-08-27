---
title: Pattern di controllo TableItem
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ITableItemProvider, incluse le informazioni sui metodi. Il pattern di controllo TableItem viene usato per supportare i controlli figlio dei contenitori che implementano ITableProvider.
ms.assetid: e00c7a58-410c-4818-8f61-57ee98527d6e
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo TableItem
- Automazione interfaccia utente,Pattern di controllo TableItem
- Automazione interfaccia utente,ITableItemProvider
- ITableItemProvider
- Implementazione di Automazione interfaccia utente di controllo TableItem
- Pattern di controllo TableItem
- pattern di controllo,ITableItemProvider
- pattern di controllo, implementazione Automazione interfaccia utente TableItem
- pattern di controllo,TableItem
- interfacce,ITableItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babb64114bb761b0b6e93a7cc9c0036cb01bb8946eb813bcd0fc3e821d44a183
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098271"
---
# <a name="tableitem-control-pattern"></a>Pattern di controllo TableItem

Vengono descritte le linee guida e le convenzioni per [**l'implementazione di ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), incluse le informazioni sui metodi. Il **pattern di controllo TableItem** viene usato per supportare i controlli figlio dei contenitori che [**implementano ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).

L'accesso alle singole funzionalità delle celle viene fornito dall'implementazione simultanea richiesta di [**IGridItemProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) Questo pattern di controllo è analogo a **IGridItemProvider** con la distinzione che qualsiasi controllo che implementa [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) deve esporre a livello di codice la relazione tra la singola cella e le relative informazioni su riga e colonna. Per esempi di controlli che implementano questo pattern di controllo, vedere [Tipi di controllo e pattern di controllo supportati.](uiauto-controlpatternmapping.md)

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **ITableItemProvider**](#required-members-for-itableitemprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il **pattern di controllo TableItem,** tenere presente le linee guida e le convenzioni seguenti:

-   Per le funzionalità correlate degli elementi della griglia, vedere [GridItem Control Pattern](uiauto-implementinggriditem.md).

## <a name="required-members-for-itableitemprovider"></a>Membri obbligatori per **ITableItemProvider**

Per l'implementazione [**dell'interfaccia ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) sono necessari i metodi seguenti.



| Membri obbligatori                                                               | Tipo di membro | Note |
|--------------------------------------------------------------------------------|-------------|-------|
| [**GetColumnHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getcolumnheaderitems) | Metodo      | Nessuno  |
| [**GetRowHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getrowheaderitems)       | Metodo      | Nessuno  |



 

Questo pattern di controllo non è associato a proprietà o eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tipi di controllo e relativi pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Pattern di controllo tabella](uiauto-implementingtable.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 




