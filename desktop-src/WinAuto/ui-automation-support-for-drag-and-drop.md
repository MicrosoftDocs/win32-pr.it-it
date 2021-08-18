---
title: Automazione interfaccia utente supporto per il trascinamento della selezione
description: In questo argomento vengono descritti i pattern di controllo che espongono informazioni sulla funzionalità di trascinamento della selezione di un elemento.
ms.assetid: FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE
keywords:
- Automazione interfaccia utente, supporto del trascinamento della selezione
- Automazione interfaccia utente,Panoramica del modello di trascinamento
- Automazione interfaccia utente,Panoramica del modello DropTarget
- Automazione interfaccia utente, panoramica del trascinamento della selezione
- modelli di trascinamento della selezione, informazioni
- Trascinare il pattern di controllo
- Pattern di controllo DropTarget
- pattern di controllo, trascinamento
- pattern di controllo, DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eab48f4319c51a5ccbbaadae22f1ae337740df5b6d0fdf325a01ba1323f8630
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133564"
---
# <a name="ui-automation-support-for-drag-and-drop"></a>Automazione interfaccia utente supporto per il trascinamento della selezione

Microsoft Automazione interfaccia utente definisce due pattern di controllo per supportare scenari di trascinamento della selezione, il pattern di controllo [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) e [il pattern di controllo DropTarget.](/windows/desktop/WinAuto/uiauto-implementingdroptarget) Puoi implementare il pattern di controllo Drag per un elemento che può essere trascinato e il pattern di controllo DropTarget per un elemento che può ricevere un elemento trascinato; ad esempio un obiettivo di rilascio. I due pattern di controllo espongono informazioni che un assistive technology può usare per consentire a un utente di accessibilità di completare un'operazione di trascinamento della selezione.

-   [Trascinamento degli stili](#dragging-styles)
    -   [Stile di origine/destinazione](#sourcetarget-style)
    -   [Stile solo origine](#source-only-style)
-   [Trascinamento di più elementi](#dragging-multiple-items)
-   [Interfacce client per il trascinamento della selezione](#client-interfaces-for-drag-and-drop)

## <a name="dragging-styles"></a>Trascinamento degli stili

Quando si [](/windows/desktop/WinAuto/uiauto-implementingdrag) implementa il pattern di controllo Drag per un elemento trascinabile, è necessario decidere se implementare lo stile di trascinamento di *origine/destinazione* o lo stile di trascinamento solo *origine.*

### <a name="sourcetarget-style"></a>Stile di origine/destinazione

Nello stile di origine/destinazione del trascinamento della selezione, l'elemento trascinato (l'"origine") e l'elemento di destinazione di rilascio (la "destinazione") sono distinti e ognuno genera un set distinto di eventi. Ecco il ciclo di vita per un'operazione di trascinamento che usa lo stile di origine/destinazione: <dl> Quando l'utente avvia un'operazione di trascinamento:

-   L'origine genera l'evento DragStart ([**UIA \_ \_ DragStartEventId**](uiauto-event-ids.md)).
-   L'origine imposta [**la proprietà IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) su **TRUE.**
-   Le destinazioni aggiornano [**le proprietà DropTargetEffect.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)

  
Quando l'operazione di trascinamento entra in un'area di destinazione:

-   La destinazione genera l'evento DragEnter ([**UIA \_ DropTarget \_ DragEnterEventId**](uiauto-event-ids.md)).

  
Quando l'operazione di trascinamento esce da un'area di destinazione:

-   La destinazione genera l'evento DragLeave [**(UIA \_ DropTarget \_ DragLeaveEventId).**](uiauto-event-ids.md)

  
Quando l'utente rilascia l'elemento trascinato su un oggetto non di destinazione:

-   L'origine genera l'evento DragCancel ([**UIA \_ \_ DragCancelEventId**](uiauto-event-ids.md)).
-   L'origine imposta [**la proprietà IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) su **FALSE.**

  
Quando l'utente rilascia l'elemento trascinato su una destinazione:

-   L'origine genera l'evento DragComplete ([**UIA \_ \_ DragCompleteEventId**](uiauto-event-ids.md)).
-   L'origine imposta [**la proprietà IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) su **FALSE.**
-   La destinazione imposta la [**proprietà IDropTargetProvider::D targetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) per indicare l'effetto che si è verificato.
-   La destinazione genera l'evento Dropped ([**UIA \_ DropTarget \_ DroppedEventId).**](uiauto-event-ids.md)

  
</dl>

Gli eventi degli oggetti di origine e di destinazione sono strettamente correlati, ma distinti. I dati su ciò che viene trascinato provengono dall'origine, mentre i dati su "cosa potrebbe accadere" e "cosa è successo" provengono dalla destinazione.

Quando è in corso un'operazione di trascinamento, l'elemento trascinato può essere trascinato all'inizio e all'uscita delle aree di destinazione un numero qualsiasi di volte prima del completamento dell'operazione.

Qualsiasi obiettivo di rilascio che deve aggiornare la proprietà [**IDropTargetProvider::D targetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) in tempo reale deve generare un evento aggiuntivo di modifica della proprietà per tale proprietà.

### <a name="source-only-style"></a>Stile solo origine

Lo stile di trascinamento solo origine consente a un provider di evitare di implementare destinazioni di rilascio. La non implementazione di destinazioni di rilascio consente di ridurre il costo di implementazione, ma non fornisce alle applicazioni client di accessibilità informazioni sull'oggetto che ha ricevuto l'eliminazione. Ecco il ciclo di vita per un'operazione di trascinamento che usa lo stile solo di origine: <dl> Quando l'utente avvia un'operazione di trascinamento:

-   L'origine genera l'evento DragStart ([**UIA \_ \_ DragStartEventId**](uiauto-event-ids.md)).
-   L'origine imposta [**la proprietà IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) su **TRUE.**

  
Quando l'operazione di trascinamento entra in un'area di destinazione:

-   L'origine imposta [**la proprietà IDragProvider::D effect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) sul valore appropriato.

  
Quando l'operazione di trascinamento esce da un'area di destinazione:

-   L'origine imposta [**la proprietà IDragProvider::D effect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) sul valore appropriato.

  
Quando l'utente rilascia l'elemento trascinato su un oggetto non di destinazione:

-   L'origine genera l'evento DragCancel ([**UIA \_ \_ DragCancelEventId**](uiauto-event-ids.md)).
-   L'origine imposta [**la proprietà IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) su **FALSE.**

  
Quando l'utente rilascia l'elemento trascinato su una destinazione:

-   L'origine genera l'evento DragComplete ([**UIA \_ \_ DragCompleteEventId**](uiauto-event-ids.md)).
-   L'origine imposta [**la proprietà IDragProvider::D effect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) per indicare l'effetto che ha avuto luogo quando l'elemento è stato eliminato.

  
</dl>

## <a name="dragging-multiple-items"></a>Trascinamento di più elementi

Se un provider implementa operazioni di trascinamento della selezione in cui l'utente può trascinare più oggetti contemporaneamente, il provider usa gli stili di origine/destinazione o solo di origine, come descritto nella sezione precedente, ma con una piccola differenza. Quando l'utente inizia l'operazione di trascinamento, il provider crea un elemento di origine master che rappresenta il set completo di elementi trascinati. L'elemento di origine master genera tutti gli eventi per conto del set di elementi trascinati. Gli elementi non generano eventi propri.<dl> Quando l'utente avvia un'operazione di trascinamento:

-   Il provider crea l'elemento di origine master.
-   L'elemento di origine master genera l'evento DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).
-   L'elemento di origine master [**imposta la proprietà IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) su **TRUE.**
-   L'elemento di origine master aggiorna l'elenco di elementi afferrati per includere tutti gli elementi trascinati in modo che il [**metodo GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) possa recuperare l'elenco.

  
</dl>

A tale punto, l'elemento di origine master svolge lo stesso ruolo dell'elemento di origine, come descritto nella sezione precedente.

## <a name="client-interfaces-for-drag-and-drop"></a>Interfacce client per il trascinamento della selezione

Automazione interfaccia utente applicazioni client usano le interfacce [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) e [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) per accedere alle informazioni di trascinamento della selezione dagli elementi dell'interfaccia utente.

 

 