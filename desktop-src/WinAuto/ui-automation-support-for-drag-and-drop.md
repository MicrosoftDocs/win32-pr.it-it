---
title: Supporto di automazione interfaccia utente per il trascinamento della selezione
description: Questo argomento descrive i pattern di controllo che espongono informazioni sulla funzionalità di trascinamento della selezione di un elemento.
ms.assetid: FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE
keywords:
- Automazione interfaccia utente, supporto del trascinamento della selezione
- Automazione interfaccia utente, panoramica del modello di trascinamento
- Automazione interfaccia utente, panoramica del modello DropTarget
- Automazione interfaccia utente, panoramica del trascinamento della selezione
- modelli di trascinamento della selezione, informazioni
- Trascinare il pattern di controllo
- Pattern di controllo DropTarget
- pattern di controllo, trascinamento
- pattern di controllo, DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4194613d15aadac4a925303ef2322d4cf53c341c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300061"
---
# <a name="ui-automation-support-for-drag-and-drop"></a>Supporto di automazione interfaccia utente per il trascinamento della selezione

Automazione interfaccia utente Microsoft definisce due pattern di controllo per supportare gli scenari di trascinamento della selezione, il pattern di controllo di [trascinamento](/windows/desktop/WinAuto/uiauto-implementingdrag) e il pattern di controllo [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) . Si implementa il pattern di controllo di trascinamento per un elemento che può essere trascinato e il pattern di controllo DropTarget per un elemento che può ricevere un elemento trascinato; ovvero una destinazione di rilascio. I due pattern di controllo espongono informazioni che possono essere usate da una tecnologia per l'accessibilità per consentire a un utente di accessibilità di completare un'operazione di trascinamento della selezione.

-   [Stili di trascinamento](#dragging-styles)
    -   [Stile di origine/destinazione](#sourcetarget-style)
    -   [Stile di solo origine](#source-only-style)
-   [Trascinamento di più elementi](#dragging-multiple-items)
-   [Interfacce client per il trascinamento della selezione](#client-interfaces-for-drag-and-drop)

## <a name="dragging-styles"></a>Stili di trascinamento

Quando si implementa il pattern [di controllo di trascinamento](/windows/desktop/WinAuto/uiauto-implementingdrag) per un elemento trascinabile, è necessario decidere se implementare lo stile di trascinamento di *origine/destinazione* oppure lo stile di trascinamento *solo di origine* .

### <a name="sourcetarget-style"></a>Stile di origine/destinazione

Nello stile di origine/destinazione del trascinamento della selezione, l'elemento trascinato ("origine") e l'elemento di destinazione finale ("destinazione") sono distinti e ognuno di essi genera un set di eventi distinto. Ecco il ciclo di vita di un'operazione di trascinamento che usa lo stile di origine/destinazione: <dl> Quando l'utente avvia un'operazione di trascinamento:

-   L'origine genera l'evento DragStart [**( \_ \_ DragStartEventId drag**](uiauto-event-ids.md)).
-   Il codice sorgente imposta la proprietà [**IDragProvider:: grabbing**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) su **true**.
-   Le destinazioni aggiornano le proprietà [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) .

  
Quando l'operazione di trascinamento entra in un'area di destinazione:

-   La destinazione genera l'evento DragEnter ([**UIA \_ DropTarget \_ DragEnterEventId**](uiauto-event-ids.md)).

  
Quando l'operazione di trascinamento esce da un'area di destinazione:

-   La destinazione genera l'evento DragLeave [**( \_ DropTarget \_ DragLeaveEventId**](uiauto-event-ids.md)).

  
Quando l'utente rilascia l'elemento trascinato su un non target:

-   L'origine genera l'evento DragCancel [**( \_ \_ DragCancelEventId drag**](uiauto-event-ids.md)).
-   L'origine imposta la proprietà [**IDragProvider:: ungrabbing**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) su **false**.

  
Quando l'utente rilascia l'elemento trascinato su una destinazione:

-   L'origine genera l'evento DragComplete [**( \_ \_ DragCompleteEventId drag**](uiauto-event-ids.md)).
-   L'origine imposta la proprietà [**IDragProvider:: ungrabbing**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) su **false**.
-   La destinazione imposta la proprietà [**IDropTargetProvider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) per indicare l'effetto che si è verificato.
-   La destinazione genera l'evento [**\_ DropTarget \_ DroppedEventId**](uiauto-event-ids.md)eliminato.

  
</dl>

Gli eventi degli oggetti di origine e di destinazione sono strettamente correlati, ma distinti. I dati relativi a ciò che viene trascinato provengono dall'origine, mentre i dati relativi a "cosa può accadere" e "cosa è accaduto" provengono dalla destinazione.

Quando è in corso un'operazione di trascinamento, l'elemento trascinato può essere trascinato all'interno e all'esterno delle aree di destinazione un numero qualsiasi di volte prima del completamento dell'operazione.

Qualsiasi destinazione di rilascio che deve aggiornare la relativa proprietà [**IDropTargetProvider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) in tempo reale deve generare un evento di modifica proprietà aggiuntivo sulla proprietà.

### <a name="source-only-style"></a>Stile di solo origine

Lo stile di trascinamento solo origine consente a un provider di evitare di implementare destinazioni di rilascio. La mancata implementazione degli obiettivi di rilascio contribuisce a ridurre il costo di implementazione, ma non fornisce alle applicazioni client di accessibilità informazioni sull'oggetto che ha ricevuto l'eliminazione. Ecco il ciclo di vita di un'operazione di trascinamento che usa lo stile di sola origine: <dl> Quando l'utente avvia un'operazione di trascinamento:

-   L'origine genera l'evento DragStart [**( \_ \_ DragStartEventId drag**](uiauto-event-ids.md)).
-   Il codice sorgente imposta la proprietà [**IDragProvider:: grabbing**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) su **true**.

  
Quando l'operazione di trascinamento entra in un'area di destinazione:

-   L'origine imposta la proprietà [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) sul valore appropriato.

  
Quando l'operazione di trascinamento esce da un'area di destinazione:

-   L'origine imposta la proprietà [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) sul valore appropriato.

  
Quando l'utente rilascia l'elemento trascinato su un non target:

-   L'origine genera l'evento DragCancel [**( \_ \_ DragCancelEventId drag**](uiauto-event-ids.md)).
-   L'origine imposta la proprietà [**IDragProvider:: ungrabbing**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) su **false**.

  
Quando l'utente rilascia l'elemento trascinato su una destinazione:

-   L'origine genera l'evento DragComplete [**( \_ \_ DragCompleteEventId drag**](uiauto-event-ids.md)).
-   L'origine imposta la proprietà [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) per indicare l'effetto che si è verificato quando l'elemento è stato eliminato.

  
</dl>

## <a name="dragging-multiple-items"></a>Trascinamento di più elementi

Se un provider implementa operazioni di trascinamento della selezione in cui l'utente può trascinare contemporaneamente più oggetti, il provider utilizza gli stili di origine/destinazione o solo origine, come descritto nella sezione precedente, ma con una piccola differenza. Quando l'utente inizia l'operazione di trascinamento, il provider crea un elemento di origine master che rappresenta il set completo di elementi trascinati. L'elemento di origine master genera tutti gli eventi per conto del set di elementi trascinati; gli elementi non generano alcun evento autonomo.<dl> Quando l'utente avvia un'operazione di trascinamento:

-   Il provider crea l'elemento di origine master.
-   L'elemento di origine master genera l'evento DragStart ([**\_ \_ DragStartEventId drag**](uiauto-event-ids.md)).
-   L'elemento di origine master imposta la proprietà [**IDragProvider:: ungrabbing**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) su **true**.
-   L'elemento di origine master aggiorna l'elenco di elementi catturati per includere tutti gli elementi trascinati in modo che il metodo [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) possa recuperare l'elenco.

  
</dl>

Per questo punto, l'elemento di origine master esegue lo stesso ruolo dell'elemento di origine, come descritto nella sezione precedente.

## <a name="client-interfaces-for-drag-and-drop"></a>Interfacce client per il trascinamento della selezione

Le applicazioni client di automazione interfaccia utente usano le interfacce [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) e [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) per accedere alle informazioni relative al trascinamento della selezione dagli elementi dell'interfaccia utente.

 

 