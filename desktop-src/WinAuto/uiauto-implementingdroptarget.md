---
title: Pattern di controllo DropTarget
description: Fornisce linee guida e convenzioni per l'implementazione del pattern di controllo DropTarget usando IDropTargetProvider, incluse informazioni su proprietà e metodi.
ms.assetid: DD5EE4A0-E6C0-4657-A60F-7F59FC569E04
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo DropTarget
- Automazione interfaccia utente, pattern di controllo DropTarget
- Automazione interfaccia utente,IDropTargetProvider
- IDropTargetProvider
- Implementazione Automazione interfaccia utente pattern di controllo DropTarget
- Pattern di controllo DropTarget
- pattern di controllo, IDropTargetProvider
- pattern di controllo, implementazione Automazione interfaccia utente DropTarget
- pattern di controllo, DropTarget
- interfacce, IDropTargetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03cc425c9d41a70150eba2431c6fd317f2f8c23f878f7a0615025aec25b85b68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098311"
---
# <a name="droptarget-control-pattern"></a>Pattern di controllo DropTarget

Fornisce linee guida e convenzioni per l'implementazione del pattern di **controllo DropTarget** usando [**IDropTargetProvider,**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider)incluse informazioni su proprietà e metodi. Il **pattern di controllo DropTarget** viene usato per supportare i controlli che possono essere la destinazione di un'operazione di trascinamento della selezione.

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern **di controllo DropTarget,** usare le linee guida e le convenzioni seguenti:

-   Il **modello DropTarget** deve essere supportato mentre è in corso un'operazione di trascinamento. Può essere supportato anche quando non è in corso un'operazione di trascinamento.
-   La [**proprietà IDropTargetProvider::D targetEffect è**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) obbligatoria.
-   La [**proprietà IDropTargetProvider::D targetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) è obbligatoria quando è presente più di un possibile effetto di rilascio per la destinazione.
-   L'elemento deve generare eventi di modifica delle proprietà per le proprietà **DropTargetEffect** ([**UIA \_ DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) e **DropTargetEffects** ([**UIA \_ DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) quando cambiano.

## <a name="required-members-for-idroptargetprovider"></a>Membri obbligatori per **IDropTargetProvider**

Per implementare l'interfaccia [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) sono necessari i metodi e le proprietà seguenti.



| Membri obbligatori                                                                              | Tipo di membro | Note                                                                    |
|-----------------------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------|
| [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)                       | Proprietà    | Nessuno                                                                     |
| [**DropTargetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects)                     | Proprietà    | Obbligatorio se l'obiettivo di rilascio supporta più di un possibile effetto di rilascio. |
| [**UIA \_ DropTarget \_ DragEnterEventId**](uiauto-event-ids.md) | Event       | Nessuno                                                                     |
| [**UIA \_ DropTarget \_ DragLeaveEventId**](uiauto-event-ids.md) | Event       | Nessuno                                                                     |
| [**DropTarget \_ DroppedEventId dell'interfaccia \_ utente**](uiauto-event-ids.md)     | Event       | Nessuno                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Trascinare il pattern di controllo](/windows/desktop/WinAuto/uiauto-implementingdrag)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> <dt>

[Automazione interfaccia utente supporto per il trascinamento della selezione](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 