---
title: Ottenere elementi di automazione interfaccia utente
description: Questo argomento descrive i vari modi per ottenere le interfacce IUIAutomationElement per gli elementi dell'interfaccia utente.
ms.assetid: 8675851a-4a72-4cbe-ab71-ed6fc891be17
keywords:
- client, acquisizione di elementi di automazione interfaccia utente
- client, elementi di automazione interfaccia utente
- client, elementi radice
- client, ambito di ricerca
- Automazione interfaccia utente, recupero di elementi
- Automazione interfaccia utente, elementi
- Automazione interfaccia utente, elementi radice
- Automazione interfaccia utente, condizioni
- Automazione interfaccia utente, ambito di ricerca
- recupero di elementi di automazione interfaccia utente
- elementi radice
- ambito di ricerca
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: a1adbcea5cea81f97350ef15c491b289e07d3ee6
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323877"
---
# <a name="obtaining-ui-automation-elements"></a>Ottenere elementi di automazione interfaccia utente

Questo argomento descrive i vari modi per ottenere le interfacce [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per gli elementi dell'interfaccia utente.

**IUIAutomationElement** viene usato nell' [app di esempio client di contenuto del documento di automazione interfaccia utente](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient).

## <a name="root-element"></a>Elemento radice

Sebbene gli elementi possano essere recuperati direttamente usando metodi, ad esempio [**IUIAutomation:: GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), alcune applicazioni client richiedono una visualizzazione della struttura gerarchica degli elementi, nota come albero di automazione interfaccia utente. L'elemento radice di questa gerarchia è il desktop. È possibile ottenere questo elemento usando il metodo [**IUIAutomation:: getRootElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelement) o [**IUIAutomation:: GetRootElementBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelementbuildcache) . Entrambi questi metodi recuperano un puntatore di interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) . È possibile cercare elementi discendenti usando metodi, ad esempio [**IUIAutomationElement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) e [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall).

> [!Note]  
> In generale, è consigliabile provare a ottenere solo gli elementi figlio diretti dell'elemento radice. Una ricerca di discendenti può scorrere centinaia o migliaia di elementi. Per ottenere un elemento specifico a un livello inferiore, è consigliabile avviare la ricerca dalla finestra dell'applicazione o da un contenitore a un livello inferiore.

 

## <a name="conditions"></a>Condizioni

Per la maggior parte delle tecniche usate per recuperare gli elementi di automazione interfaccia utente, è necessario specificare una condizione. Una condizione è un set di criteri che definisce gli elementi che si desidera recuperare. Una condizione è rappresentata dall'interfaccia [**IUIAutomationCondition**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition) .

La condizione più semplice è la condizione vera, ovvero un oggetto predefinito che specifica che devono essere restituiti tutti gli elementi nell'ambito di ricerca. La condizione falsa è l'inverso della condizione vera ed è meno utile, perché impedirebbe la rilevanza di qualsiasi elemento. È possibile ottenere un'interfaccia per la condizione true usando [**IUIAutomation:: CreateTrueCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtruecondition).

Altre tre condizioni predefinite, disponibili come proprietà per l'oggetto [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) , possono essere usate singolarmente o in combinazione con altre condizioni: [**IUIAutomation:: ContentViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewcondition), [**ControlViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewcondition)e [**RawViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewcondition). **RawViewCondition**, usato da solo, equivale alla condizione true, perché non filtra gli elementi in base alle proprietà [**IUIAutomationElement:: CurrentIsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) o [**CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) .

Altre condizioni sono compilate da oggetti Condition, ognuno dei quali specifica un valore della proprietà. Una condizione di proprietà, ad esempio, potrebbe specificare che l'elemento è abilitato o che supporta un determinato pattern di controllo.

Le condizioni che usano la logica booleana possono essere combinate chiamando [**IUIAutomation:: CreateAndCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createandcondition), [**CreateOrCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createorcondition), [**CreateNotCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createnotcondition)e i metodi correlati.

## <a name="search-scope"></a>Ambito di ricerca

Le ricerche eseguite con [**IUIAutomationElement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) o [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) devono avere un ambito e una posizione iniziale.

> [!Note]  
> Eventuali commenti su questi due metodi si applicano anche a [**IUIAutomationElement:: FindFirstBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache) e [**FindAllBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findallbuildcache).

 

L'ambito definisce lo spazio intorno al punto di inizio in cui eseguire la ricerca. Ciò può includere l'elemento stesso, i relativi elementi di pari livello, il padre, i relativi elementi figlio immediati e i relativi discendenti. Tenere presente che i metodi **Find** non supportano la ricerca nell'albero di automazione interfaccia utente Microsoft; ovvero la ricerca di elementi predecessori non è supportata.

L'ambito di una ricerca viene definito da una combinazione bit per bit dei valori del tipo enumerato [**TreeScope**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope) .

## <a name="finding-a-known-element"></a>Ricerca di un elemento noto

Per trovare un elemento noto identificato dal nome, dall'ID di automazione o da altre proprietà o combinazioni di proprietà, è più semplice usare il metodo [**IUIAutomationElement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) . Se l'elemento cercato è una finestra dell'applicazione, il punto iniziale della ricerca può essere l'elemento radice.

Questo modo per trovare gli elementi di automazione interfaccia utente è particolarmente utile negli scenari di test automatizzati.

Per un esempio di codice in cui viene illustrato come trovare un elemento know, vedere [ricerca di un elemento in base al nome](uiauto-howto-find-ui-elements.md).

## <a name="finding-elements-in-a-subtree"></a>Ricerca di elementi in un sottoalbero

Per trovare tutti gli elementi che soddisfano criteri specifici e sono correlati a un elemento noto, è possibile chiamare [**IUIAutomationElement:: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) sull'elemento noto. Usare, ad esempio, questo metodo per recuperare elementi elenco o voci di menu da un elenco o menu o per identificare tutti i controlli in una finestra di dialogo.

Per un esempio di codice che illustra come trovare elementi in un sottoalbero, vedere [ricerca di elementi correlati](uiauto-howto-find-ui-elements.md).

## <a name="walking-a-subtree"></a>Esplorazione di un sottoalbero

Se non si ha alcuna conoscenza precedente delle applicazioni con cui il client può essere usato, è possibile costruire un sottoalbero di tutti gli elementi di interesse usando [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker). Il client può eseguire questa operazione, ad esempio, in risposta a un evento di modifica dello stato attivo; ovvero, quando un'applicazione o un controllo riceve lo stato attivo per l'input, il client di automazione interfaccia utente esamina gli elementi figlio ed eventualmente tutti i discendenti dell'elemento con lo stato attivo.

Tenere presente che la struttura ad albero di automazione interfaccia utente richiede un utilizzo intensivo delle risorse. Esaminare l'albero solo quando non è possibile usare i metodi [**IUIAutomationElement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst), [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)o [**BuildUpdatedCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache) .

È possibile definire il proprio camminatore di albero passando una condizione personalizzata a [**IUIAutomation:: CreateTreeWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtreewalker)oppure è possibile usare uno degli oggetti predefiniti seguenti che vengono definiti come proprietà del [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)di base.



| Oggetto                                                              | Scopo                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) | Trova solo gli elementi la cui proprietà [**IUIAutomationElement:: CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) è **true**. |
| [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) | Trova solo gli elementi la cui proprietà [**IUIAutomationElement:: CurrentIsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) è **true**. |
| [**RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker)         | Trova tutti gli elementi.                                                                                                                                          |



 

Dopo aver ottenuto un [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker), chiamare i metodi **IUIAutomationTreeWalker:: GetXxx** per spostarsi tra gli elementi del sottoalbero, passando l'elemento da cui iniziare a camminare.

Il metodo [**IUIAutomationTreeWalker:: Normalize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-normalizeelement) può essere usato per passare a un elemento nel sottoalbero da un altro elemento che non fa parte della visualizzazione. Si supponga, ad esempio, di creare una vista di un sottoalbero usando [**IUIAutomation:: ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker). L'applicazione riceve la notifica che una barra di scorrimento ha ricevuto lo stato attivo per l'input. Poiché una barra di scorrimento non è un elemento con contenuto, non è presente nella visualizzazione del sottoalbero. Tuttavia, è possibile passare il [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) che rappresenta la barra di scorrimento a **IUIAutomationTreeWalker:: Normalize** e recuperare il predecessore più vicino nella visualizzazione contenuto.

Per esempi di codice che illustrano come usare l'interfaccia [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) , vedere [come esaminare l'albero di automazione interfaccia utente](uiauto-howto-walk-uiautomation-tree.md).

## <a name="other-ways-to-retrieve-an-element"></a>Altri modi per recuperare un elemento

Oltre alle ricerche e alla navigazione, è possibile recuperare un [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) nei modi seguenti.

### <a name="from-an-event"></a>Da un evento

Quando l'applicazione riceve un evento di automazione interfaccia utente, l'oggetto di origine passato al gestore eventi è rappresentato da un [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement). Se ad esempio si effettua la sottoscrizione agli eventi di modifica dello stato attivo, l'origine passata a [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) è l'elemento che ha ricevuto lo stato attivo. Per altre informazioni, vedere [sottoscrizione di eventi di automazione interfaccia utente](uiauto-eventsforclients.md).

### <a name="from-a-point"></a>Da un punto

Per recuperare un [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) dalle coordinate dello schermo, ad esempio una posizione del cursore, usare il metodo [**IUIAutomation:: ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) .

### <a name="from-a-window-handle"></a>Da un handle di finestra

Per recuperare un [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) da un **HWND**, usare il metodo [**IUIAutomation:: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle) .

### <a name="from-the-focused-control"></a>Dal controllo con lo stato attivo

Per recuperare un [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) che rappresenta il controllo con stato attivo, usare il metodo [**IUIAutomation:: GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement) .

## <a name="related-topics"></a>Argomenti correlati

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)

[App di esempio client di contenuto del documento di automazione interfaccia utente](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient)
