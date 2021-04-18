---
title: Pattern di controllo SelectionItem
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ISelectionItemProvider, incluse informazioni su proprietà, metodi ed eventi.
ms.assetid: 9314547f-7062-42db-b6a7-8a8eaef21d4e
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo SelectionItem
- Automazione interfaccia utente, pattern di controllo SelectionItem
- Automazione interfaccia utente, ISelectionItemProvider
- ISelectionItemProvider
- implementazione di pattern di controllo SelectionItem di automazione interfaccia utente
- Pattern di controllo SelectionItem
- pattern di controllo, ISelectionItemProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente SelectionItem
- pattern di controllo, SelectionItem
- interfacce, ISelectionItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912be363ea8228d905a600de091d6cbe12b925fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297837"
---
# <a name="selectionitem-control-pattern"></a>Pattern di controllo SelectionItem

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider), incluse informazioni su proprietà, metodi ed eventi. Il pattern di controllo **SelectionItem** viene usato per supportare i controlli che fungono da singoli elementi figlio selezionabili dei controlli contenitore che implementano [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).

Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **ISelectionItemProvider**](#required-members-for-iselectionitemprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **SelectionItem** , tenere presenti le linee guida e le convenzioni seguenti:

-   I controlli a selezione singola che gestiscono i controlli figlio che implementano [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), ad esempio il dispositivo di scorrimento **risoluzione schermo** nella finestra di dialogo **proprietà di visualizzazione** per Windows, devono implementare [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); i relativi elementi figlio devono implementare sia [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) che [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

## <a name="required-members-for-iselectionitemprovider"></a>Membri obbligatori per **ISelectionItemProvider**

Le proprietà, i metodi e gli eventi seguenti sono obbligatori per l'implementazione dell'interfaccia [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) .



| Membri obbligatori                                                                                                                        | Tipo di membro | Note |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------|-------|
| [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-addtoselection)                                                                  | Metodo      | nessuno  |
| [**IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected)                                                                          | Proprietà    | nessuno  |
| [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-removefromselection)                                                        | Metodo      | nessuno  |
| [**Selezionare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select)                                                                                  | Metodo      | nessuno  |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)                                                          | Proprietà    | nessuno  |
| [**\_ElementAddedToSelectionEventId SelectionItem di UIA \_**](uiauto-event-ids.md)         | Evento       | nessuno  |
| [**\_ElementRemovedFromSelectionEventId SelectionItem di UIA \_**](uiauto-event-ids.md) | Evento       | nessuno  |
| [**\_ElementSelectedEventId SelectionItem di UIA \_**](uiauto-event-ids.md)                         | Evento       | nessuno  |



 

Se il risultato di una [**Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select), di [**un AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)o di un [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) è un singolo elemento selezionato, è necessario generare un evento **ElementSelected** ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)); in caso contrario, generare gli eventi **ElementAddedToSelection** ([**UIA SelectionItem ElementAddedToSelectionEventId) o \_ \_**](uiauto-event-ids.md) **ElementRemovedFromSelection** ([**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)) nel modo appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 




