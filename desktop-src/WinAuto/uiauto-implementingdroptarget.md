---
title: Pattern di controllo DropTarget
description: Fornisce linee guida e convenzioni per l'implementazione del pattern di controllo DropTarget usando IDropTargetProvider, incluse le informazioni su proprietà e metodi.
ms.assetid: DD5EE4A0-E6C0-4657-A60F-7F59FC569E04
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo DropTarget
- Automazione interfaccia utente, pattern di controllo DropTarget
- Automazione interfaccia utente, IDropTargetProvider
- IDropTargetProvider
- implementazione di pattern di controllo DropTarget di automazione interfaccia utente
- Pattern di controllo DropTarget
- pattern di controllo, IDropTargetProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente DropTarget
- pattern di controllo, DropTarget
- interfacce, IDropTargetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd03d219ce8b26a0ac01806ebab09892a027fbd1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338190"
---
# <a name="droptarget-control-pattern"></a>Pattern di controllo DropTarget

Fornisce linee guida e convenzioni per l'implementazione del pattern di controllo **DropTarget** usando [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider), incluse le informazioni su proprietà e metodi. Il pattern di controllo **DropTarget** viene usato per supportare i controlli che possono essere la destinazione di un'operazione di trascinamento della selezione.

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **DropTarget** , usare le linee guida e le convenzioni seguenti:

-   Il pattern **DropTarget** deve essere supportato mentre è in corso un'operazione di trascinamento. Può essere supportata anche quando non è in corso un'operazione di trascinamento.
-   La proprietà [**IDropTargetProvider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) è obbligatoria.
-   La proprietà [**IDropTargetProvider::D roptargeteffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) è obbligatoria quando è disponibile più di un effetto di rilascio per la destinazione.
-   L'elemento deve generare eventi di modifica di proprietà per le proprietà **DropTargetEffect** ([**UIA \_ DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) e **DropTargetEffects** ([**UIA \_ DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) quando cambiano.

## <a name="required-members-for-idroptargetprovider"></a>Membri obbligatori per **IDropTargetProvider**

Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) .



| Membri obbligatori                                                                              | Tipo di membro | Note                                                                    |
|-----------------------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------|
| [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)                       | Proprietà    | nessuno                                                                     |
| [**DropTargetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects)                     | Proprietà    | Obbligatorio se la destinazione di rilascio supporta più di un possibile effetto di rilascio. |
| [**\_DragEnterEventId DropTarget di UIA \_**](uiauto-event-ids.md) | Evento       | nessuno                                                                     |
| [**\_DragLeaveEventId DropTarget di UIA \_**](uiauto-event-ids.md) | Evento       | nessuno                                                                     |
| [**\_DroppedEventId DropTarget di UIA \_**](uiauto-event-ids.md)     | Evento       | nessuno                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Trascinare il pattern di controllo](/windows/desktop/WinAuto/uiauto-implementingdrag)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> <dt>

[Supporto di automazione interfaccia utente per il trascinamento della selezione](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 