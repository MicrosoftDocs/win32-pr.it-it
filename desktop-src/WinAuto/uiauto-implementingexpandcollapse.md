---
title: Pattern di controllo ExpandCollapse
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IExpandCollapseProvider, incluse informazioni su proprietà, metodi ed eventi.
ms.assetid: 0ffc26c3-8696-44f9-b463-902a69e06d21
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo ExpandCollapse
- Automazione interfaccia utente,Pattern di controllo ExpandCollapse
- Automazione interfaccia utente,IExpandCollapseProvider
- IExpandCollapseProvider
- Implementazione Automazione interfaccia utente pattern di controllo ExpandCollapse
- Pattern di controllo ExpandCollapse
- pattern di controllo,IExpandCollapseProvider
- pattern di controllo, implementazione Automazione interfaccia utente ExpandCollapse
- pattern di controllo,ExpandCollapse
- interfacce,IExpandCollapseProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7fa1461110a7fcdee83b8b3c20c15653e7bd5740187b89337620f5410b2bf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998041"
---
# <a name="expandcollapse-control-pattern"></a>Pattern di controllo ExpandCollapse

Vengono descritte le linee guida e le convenzioni per [**l'implementazione di IExpandCollapseProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)incluse informazioni su proprietà, metodi ed eventi. Il **pattern di controllo ExpandCollapse** viene usato per supportare i controlli che si espandono visivamente per visualizzare più contenuto e comprimere per nascondere il contenuto.

Per esempi di controlli che implementano questo pattern di controllo, vedere [Tipi di controllo e pattern di controllo supportati.](uiauto-controlpatternmapping.md)

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IExpandCollapseProvider**](#required-members-for-iexpandcollapseprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il **pattern di controllo ExpandCollapse,** tenere presente le linee guida e le convenzioni seguenti:

-   I controlli aggregati, compilati con oggetti figlio che forniscono all'interfaccia utente la funzionalità di espansione/compressione, devono supportare il pattern di **controllo ExpandCollapse,** mentre i relativi elementi figlio non lo fanno. Ad esempio, un controllo casella combinata viene compilato con una combinazione di controlli casella di riepilogo, pulsante e modifica, ma è solo la casella combinata padre che deve supportare il pattern **di controllo ExpandCollapse.**
    > [!Note]  
    > Un'eccezione è il controllo menu, che è un'aggregazione di singoli oggetti voce di menu. Gli oggetti voce di menu possono supportare il **pattern di controllo ExpandCollapse,** ma il controllo menu padre non può. Un'eccezione simile si applica ai controlli albero e degli elementi della struttura ad albero.

     

-   Quando la proprietà [**IExpandCollapseProvider::ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) di un controllo è impostata su **ExpandCollapseState \_ LeafNode,** qualsiasi funzionalità **ExpandCollapse** è attualmente inattiva per il controllo e l'unica informazione che può essere ottenuta usando questo pattern di controllo è **ExpandCollapseState**. Se successivamente vengono aggiunti oggetti figlio, le **funzionalità ExpandCollapseState** e **ExpandCollapse** vengono attivate.
-   [**ExpandCollapseState fa**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) riferimento alla visibilità solo degli oggetti figlio immediati. non fa riferimento alla visibilità di tutti gli oggetti discendenti.
-   [**La funzionalità IExpandCollapseProvider::Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) e [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) è specifica del controllo. Di seguito sono riportati alcuni esempi di questo comportamento.
    -   Il menu Office Personale può essere una voce di menu a tre stati ("Espanso", "Compresso" e "Parzialmenteesperato") in cui il controllo specifica lo stato da adottare quando viene chiamato [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) o [**Collapse.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)
    -   La [**chiamata di Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) su un elemento della struttura ad albero può visualizzare tutti i discendenti o solo gli elementi figlio immediati.
    -   Se la [**chiamata a Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) o [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) in un controllo mantiene lo stato dei relativi discendenti, deve essere inviato un evento di modifica della visibilità, non un evento di modifica dello stato. Se il controllo padre non mantiene lo stato dei discendenti quando viene compresso, il controllo può eliminare tutti i discendenti che non sono più visibili e generare un evento eliminato. oppure può modificare [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) per ogni discendente e generare un evento di modifica della visibilità.
-   Per garantire la navigazione, è consigliabile che un oggetto si trova nell'albero di Microsoft Automazione interfaccia utente (con lo stato di visibilità appropriato) indipendentemente dall'elemento [**padre ExpandCollapseState.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) Se i discendenti vengono generati su richiesta, possono essere visualizzati nell'albero Automazione interfaccia utente solo dopo essere stati visualizzati per la prima volta o solo quando sono visibili.

## <a name="required-members-for-iexpandcollapseprovider"></a>Membri obbligatori per **IExpandCollapseProvider**

Per l'implementazione dell'interfaccia [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) sono necessarie le proprietà, i metodi e gli eventi seguenti.



| Membri obbligatori                                                                                    | Tipo di membro | Note                                                                  |
|-----------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------|
| [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate)                   | Proprietà    | Nessuno                                                                   |
| [**Espandere**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)                                             | Metodo      | Nessuno                                                                   |
| [**Comprimi**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)                                         | Metodo      | Nessuno                                                                   |
| [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | Evento       | A questo controllo non sono associati eventi. usare questo gestore eventi generico. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e relativi pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 




