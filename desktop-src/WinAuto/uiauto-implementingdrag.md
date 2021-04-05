---
title: Trascinare il pattern di controllo
description: Vengono fornite linee guida e convenzioni per l'implementazione del pattern di controllo di trascinamento mediante IDragProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo di trascinamento viene usato per supportare i controlli trascinabili o i controlli con elementi trascinabili.
ms.assetid: 9853E9CB-D04B-4F67-8E9E-7F1F99BACEA7
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo drag
- Automazione interfaccia utente, trascinare pattern di controllo
- Automazione interfaccia utente, IDragProvider
- IDragProvider
- implementazione di pattern di controllo drag di automazione interfaccia utente
- Trascinare i pattern di controllo
- pattern di controllo, IDragProvider
- pattern di controllo, implementazione del drag di automazione interfaccia utente
- pattern di controllo, trascinamento
- interfacce, IDragProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f0212eca37e1890596143f27e9af70e1fb19a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046965"
---
# <a name="drag-control-pattern"></a>Trascinare il pattern di controllo

Vengono fornite linee guida e convenzioni per l'implementazione del pattern di controllo di **trascinamento** mediante [**IDragProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider), incluse informazioni su proprietà e metodi. Il pattern di controllo di **trascinamento** viene usato per supportare i controlli trascinabili o i controlli con elementi trascinabili.

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **drag** , usare le linee guida e le convenzioni seguenti:

-   L'interfaccia [**IDragProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider) supporta due stili di trascinamento diversi, ovvero lo stile di origine/destinazione e lo stile di sola origine. È necessario scegliere lo stile più adatto per gli scenari di trascinamento della selezione:
    -   **Stile di origine/destinazione:** Ogni destinazione di rilascio può essere rappresentata da un elemento che implementa l'interfaccia [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) . Durante un'operazione di trascinamento, gli eventi di automazione interfaccia utente Microsoft provengono dall'elemento trascinato e dagli elementi della destinazione di rilascio.
    -   **Stile di sola origine:** Gli obiettivi di rilascio non sono rappresentati dagli elementi di automazione interfaccia utente. Durante un'operazione di trascinamento, gli eventi hanno origine solo dall'elemento trascinato.
-   [**IDragProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider) è un'interfaccia di sola lettura progettata per il monitoraggio delle operazioni di trascinamento. Non è possibile usarlo per controllare un'operazione di trascinamento. È possibile automatizzare le operazioni di trascinamento inviando l'input del mouse a un controllo.
-   La proprietà [**IDragProvider:: grabbing**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) è obbligatoria.
-   Le proprietà [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) e [**IDragProvider::D ropeffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) sono necessarie per l'implementazione di uno stile di solo origine e non sono consentite per un'implementazione dello stile di origine/destinazione. In un'implementazione dello stile di origine/destinazione, è possibile eseguire una query sugli elementi drop-target per individuare gli effetti di rilascio.
-   La proprietà [**IDragProvider:: GrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) rappresenta il trascinamento di più elementi. Quando l'utente inizia l'operazione di trascinamento, è necessario creare un nuovo elemento di automazione interfaccia utente che funga da elemento di origine evento. Questo nuovo elemento genera tutti gli eventi che l'elemento di origine avrebbe generato nella modalità di origine/destinazione o solo origine, mentre nessuno degli elementi effettivamente trascinati genera eventi. Al termine dell'operazione di trascinamento, eliminare definitivamente l'elemento di origine dell'evento.
-   L'elemento deve generare eventi di modifica di proprietà per le proprietà **DropEffect** ([**\_ DragDropEffectPropertyId**](uiauto-control-pattern-propids.md)) e **DropEffects** ([**UIA \_ DragDropEffectsPropertyId**](uiauto-control-pattern-propids.md)) quando cambiano. Gli eventi di modifica delle proprietà per le altre proprietà sono consentiti, ma possono essere dedotti dagli eventi **DragStart** (DragStartEventId drag), **DragCancel** ([**UIA \_ drag \_ DragCancelEventId**](uiauto-event-ids.md)) **e DragComplete** ([**\_ \_**](uiauto-event-ids.md)[**\_ drag \_ DragCompleteEventId**](uiauto-event-ids.md)) necessari.
-   

## <a name="required-members-for-idragprovider"></a>Membri obbligatori per **IDragProvider**

Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**IDragProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider) .



| Membri obbligatori                                                                        | Tipo di membro | Note                                                                         |
|-----------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------|
| [**Con acquisizione**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed)                                     | Proprietà    | nessuno                                                                          |
| [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect)                                   | Proprietà    | Obbligatorio per un'implementazione dello stile di sola origine.                      |
| [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects)                                 | Proprietà    | Obbligatorio se è presente più di un possibile effetto di rilascio per l'elemento catturato. |
| [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems)                         | Metodo      | Obbligatorio per un'operazione di trascinamento di più elementi.                                  |
| [**\_Drag \_ DRAGSTARTEVENTID di UIA**](uiauto-event-ids.md)       | Evento       | nessuno                                                                          |
| [**\_Drag \_ DRAGCANCELEVENTID di UIA**](uiauto-event-ids.md)     | Evento       | nessuno                                                                          |
| [**\_Drag \_ DRAGCOMPLETEEVENTID di UIA**](uiauto-event-ids.md) | Evento       | nessuno                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Pattern di controllo DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> <dt>

[Supporto di automazione interfaccia utente per il trascinamento della selezione](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 