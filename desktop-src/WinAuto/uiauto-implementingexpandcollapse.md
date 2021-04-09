---
title: Pattern di controllo ExpandCollapse
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IExpandCollapseProvider, incluse informazioni su proprietà, metodi ed eventi.
ms.assetid: 0ffc26c3-8696-44f9-b463-902a69e06d21
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo ExpandCollapse
- Automazione interfaccia utente, pattern di controllo ExpandCollapse
- Automazione interfaccia utente, IExpandCollapseProvider
- IExpandCollapseProvider
- implementazione di pattern di controllo ExpandCollapse di automazione interfaccia utente
- Pattern di controllo ExpandCollapse
- pattern di controllo, IExpandCollapseProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente ExpandCollapse
- pattern di controllo, ExpandCollapse
- interfacce, IExpandCollapseProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bd28ddcc201dcff0a4811a1eb8e04670f93091
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044478"
---
# <a name="expandcollapse-control-pattern"></a>Pattern di controllo ExpandCollapse

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider), incluse informazioni su proprietà, metodi ed eventi. Il pattern di controllo **ExpandCollapse** viene usato per supportare i controlli che si espandono visivamente per visualizzare più contenuto e comprimere per nascondere il contenuto.

Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IExpandCollapseProvider**](#required-members-for-iexpandcollapseprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **ExpandCollapse** , tenere presenti le linee guida e le convenzioni seguenti:

-   I controlli aggregati, compilati con oggetti figlio che forniscono l'interfaccia utente con funzionalità di espansione/compressione, devono supportare il pattern di controllo **ExpandCollapse** , mentre i relativi elementi figlio non lo sono. Ad esempio, un controllo casella combinata viene compilato con una combinazione di controlli casella di riepilogo, pulsante e modifica, ma è solo la casella combinata padre che deve supportare il pattern di controllo **ExpandCollapse** .
    > [!Note]  
    > Un'eccezione è rappresentata dal controllo menu, che è un'aggregazione di singoli oggetti voce di menu. Gli oggetti voce di menu possono supportare il pattern di controllo **ExpandCollapse** , ma il controllo menu padre non può. Un'eccezione simile si applica ai controlli dell'albero e dell'elemento dell'albero.

     

-   Quando l'oggetto [**IExpandCollapseProvider:: ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) di un controllo è impostato su **ExpandCollapseState \_ leafnode**, tutte le funzionalità di **ExpandCollapse** sono attualmente inattive per il controllo e le uniche informazioni che è possibile ottenere utilizzando questo pattern di controllo sono **ExpandCollapseState**. Se successivamente vengono aggiunti oggetti figlio, viene attivata la funzionalità **ExpandCollapseState** e **ExpandCollapse** .
-   [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) si riferisce solo alla visibilità degli oggetti figlio diretti; non si riferisce alla visibilità di tutti gli oggetti discendenti.
-   La funzionalità [**IExpandCollapseProvider:: Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) e [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) è specifica del controllo. Di seguito sono riportati alcuni esempi di questo comportamento.
    -   Il menu personale di Office può essere una voce di menu a tre stati ("espanso", "compresso" e "PartiallyExpanded") in cui il controllo specifica lo stato da adottare quando viene chiamato [**Espandi**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) o [**Comprimi**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) .
    -   La chiamata di [**expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) su un elemento dell'albero può visualizzare tutti i discendenti o solo gli elementi figlio immediati.
    -   Se la chiamata a [**expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) o [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) su un controllo mantiene lo stato dei relativi discendenti, deve essere inviato un evento di modifica della visibilità, non un evento di modifica dello stato. Se il controllo padre non mantiene lo stato dei relativi discendenti quando viene compresso, il controllo può eliminare tutti i discendenti non più visibili e generare un evento eliminato definitivamente; oppure può modificare il valore di [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) per ogni discendente e generare un evento di modifica della visibilità.
-   Per garantire la navigazione, è consigliabile che un oggetto si trovi nell'albero di automazione interfaccia utente Microsoft (con lo stato di visibilità appropriato) indipendentemente dagli elementi padre [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate). Se i discendenti vengono generati su richiesta, possono essere visualizzati solo nell'albero di automazione interfaccia utente dopo essere stati visualizzati per la prima volta o solo quando sono visibili.

## <a name="required-members-for-iexpandcollapseprovider"></a>Membri obbligatori per **IExpandCollapseProvider**

Le proprietà, i metodi e gli eventi seguenti sono obbligatori per l'implementazione dell'interfaccia [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) .



| Membri obbligatori                                                                                    | Tipo di membro | Note                                                                  |
|-----------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------|
| [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate)                   | Proprietà    | nessuno                                                                   |
| [**Espandere**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)                                             | Metodo      | nessuno                                                                   |
| [**Comprimi**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)                                         | Metodo      | nessuno                                                                   |
| [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | Evento       | A questo controllo non sono associati eventi. utilizzare questo gestore dell'evento generico. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 




