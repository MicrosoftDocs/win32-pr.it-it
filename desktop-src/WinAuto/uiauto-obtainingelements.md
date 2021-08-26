---
title: Ottenere elementi di automazione interfaccia utente
description: Questo argomento descrive diversi modi per ottenere le interfacce IUIAutomationElement per gli elementi dell'interfaccia utente.
ms.assetid: 8675851a-4a72-4cbe-ab71-ed6fc891be17
keywords:
- client, recupero Automazione interfaccia utente elementi
- client, Automazione interfaccia utente elementi
- client, elementi radice
- client, ambito di ricerca
- Automazione interfaccia utente,recupero di elementi
- Automazione interfaccia utente,elements
- Automazione interfaccia utente,elementi radice
- Automazione interfaccia utente,conditions
- Automazione interfaccia utente,ambito di ricerca
- recupero di Automazione interfaccia utente elementi
- elementi radice
- ambito di ricerca
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: f2ecf8a30f468e7a7ca4df60465993fa7acdc1e8eef1c8537d8c3d796132cb82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997741"
---
# <a name="obtaining-ui-automation-elements"></a>Ottenere elementi di automazione interfaccia utente

Questo argomento descrive diversi modi per ottenere le interfacce [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per gli elementi dell'interfaccia utente.

**IUIAutomationElement** viene usato nell'app di Automazione interfaccia utente [di esempio del contenuto del documento.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient)

## <a name="root-element"></a>Elemento radice

Anche se gli elementi possono essere recuperati direttamente usando metodi, ad esempio [**IUIAutomation::GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), alcune applicazioni client richiedono una visualizzazione della struttura gerarchica degli elementi, nota come albero Automazione interfaccia utente. L'elemento radice di questa gerarchia è il desktop. È possibile ottenere questo elemento usando il metodo [**IUIAutomation::GetRootElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelement) o [**il metodo IUIAutomation::GetRootElementBuildCache.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelementbuildcache) Entrambi questi metodi recuperano un [**puntatore a interfaccia IUIAutomationElement.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) È possibile cercare elementi discendenti usando metodi come [**IUIAutomationElement::FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) [**e FindAll.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)

> [!Note]  
> In generale, è consigliabile provare a ottenere solo gli elementi figlio diretti dell'elemento radice. Una ricerca di discendenti può scorrere centinaia o migliaia di elementi. Per ottenere un elemento specifico a un livello inferiore, è consigliabile avviare la ricerca dalla finestra dell'applicazione o da un contenitore a un livello inferiore.

 

## <a name="conditions"></a>Condizioni

Per la maggior parte delle tecniche usate per recuperare Automazione interfaccia utente, è necessario specificare una condizione. Una condizione è un set di criteri che definisce gli elementi da recuperare. Una condizione è rappresentata [**dall'interfaccia IUIAutomationCondition.**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)

La condizione più semplice è la condizione true, ovvero un oggetto predefinito che specifica che devono essere restituiti tutti gli elementi nell'ambito di ricerca. La condizione false è l'inverso della condizione true ed è meno utile, perché impedirebbe la ricerca di elementi. È possibile ottenere un'interfaccia per la condizione true usando [**IUIAutomation::CreateTrueCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtruecondition).

Altre tre condizioni predefinite, disponibili come proprietà nell'oggetto [**IUIAutomation,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) possono essere usate da sole o in combinazione con altre condizioni: [**IUIAutomation::ContentViewCondition,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewcondition) [**ControlViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewcondition)e [**RawViewCondition.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewcondition) **RawViewCondition,** usato da solo, equivale alla condizione true, perché non filtra gli elementi in base alle proprietà [**IUIAutomationElement::CurrentIsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) o [**CurrentIsContentElement.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement)

Altre condizioni vengono compilate da oggetti condizione, ognuno dei quali specifica un valore di proprietà. Ad esempio, una condizione di proprietà può specificare che l'elemento è abilitato o che supporta un determinato pattern di controllo.

Le condizioni che usano la logica booleana possono essere combinate chiamando [**IUIAutomation::CreateAndCondition,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createandcondition) [**CreateOrCondition,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createorcondition) [**CreateNotCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createnotcondition)e i metodi correlati.

## <a name="search-scope"></a>Ambito di ricerca

Le ricerche eseguite usando [**IUIAutomationElement::FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) o [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) devono avere un ambito e una posizione iniziale.

> [!Note]  
> Qualsiasi commento su questi due metodi si applica anche a [**IUIAutomationElement::FindFirstBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache) e [**FindAllBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findallbuildcache).

 

L'ambito definisce lo spazio intorno al punto iniziale in cui eseguire la ricerca. Può includere l'elemento stesso, i relativi elementi di pari livello, l'elemento padre, gli elementi figlio immediati e i relativi discendenti. Tenere presente che i **metodi Find** non supportano la ricerca nell'albero Automazione interfaccia utente Microsoft. ciò significa che la ricerca di elementi predecessori non è supportata.

L'ambito di una ricerca è definito da una combinazione bit per bit di valori del [**tipo enumerato TreeScope.**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)

## <a name="finding-a-known-element"></a>Ricerca di un elemento noto

Per trovare un elemento noto identificato dal nome, dall'ID di automazione o da un'altra proprietà o combinazione di proprietà, è più semplice usare il metodo [**IUIAutomationElement::FindFirst.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) Se l'elemento cercato è una finestra dell'applicazione, il punto iniziale della ricerca può essere l'elemento radice.

Questo modo di trovare Automazione interfaccia utente elementi è particolarmente utile negli scenari di test automatizzati.

Per un esempio di codice che illustra come trovare un elemento know, vedere [Ricerca di un elemento in base al nome.](uiauto-howto-find-ui-elements.md)

## <a name="finding-elements-in-a-subtree"></a>Ricerca di elementi in un sottoalbero

Per trovare tutti gli elementi che soddisfano criteri specifici e sono correlati a un elemento noto, è possibile chiamare [**IUIAutomationElement::FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) sull'elemento noto. Ad esempio, usare questo metodo per recuperare voci di elenco o di menu da un elenco o un menu o per identificare tutti i controlli in una finestra di dialogo.

Per un esempio di codice che illustra come trovare elementi in un sottoalbero, vedere [Ricerca di elementi correlati.](uiauto-howto-find-ui-elements.md)

## <a name="walking-a-subtree"></a>Esplorazione di un sottoalbero

Se non si ha alcuna conoscenza delle applicazioni con cui il client può essere usato, è possibile costruire un sottoalbero di tutti gli elementi di interesse usando [**IUIAutomationTreeWalker.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) Il client potrebbe eseguire questa operazione, ad esempio, in risposta a un evento di modifica dello stato attivo. quando un'applicazione o un controllo riceve lo stato attivo per l'input, il client Automazione interfaccia utente esamina gli elementi figlio e forse tutti i discendenti dell'elemento con lo stato attivo.

Tenere presente che l'albero Automazione interfaccia utente è a elevato utilizzo di risorse. Visualizzare l'albero solo quando non è possibile usare i metodi [**IUIAutomationElement::FindFirst,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)o [**BuildUpdatedCache.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache)

È possibile definire il proprio albero di passaggio di una condizione personalizzata a [**IUIAutomation::CreateTreeWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtreewalker)oppure è possibile usare uno degli oggetti predefiniti seguenti definiti come proprietà dell'interfaccia [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)di base.



| Oggetto                                                              | Scopo                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) | Trova solo gli elementi la [**cui proprietà IUIAutomationElement::CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) è **TRUE.** |
| [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) | Trova solo gli elementi la [**cui proprietà IUIAutomationElement::CurrentIsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) è **TRUE.** |
| [**RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker)         | Trova tutti gli elementi.                                                                                                                                          |



 

Dopo aver ottenuto [**un oggetto IUIAutomationTreeWalker,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)chiamare i metodi **IUIAutomationTreeWalker::GetXxx** per spostarsi tra gli elementi del sottoalbero, passando l'elemento da cui iniziare a spostarsi.

Il [**metodo IUIAutomationTreeWalker::Normalize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-normalizeelement) può essere usato per passare a un elemento nel sottoalbero da un altro elemento che non fa parte della visualizzazione. Si supponga, ad esempio, di creare una visualizzazione di un sottoalbero usando [**IUIAutomation::ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker). L'applicazione riceve una notifica che indica che una barra di scorrimento ha ricevuto lo stato attivo per l'input. Poiché una barra di scorrimento non è un elemento con contenuto, non è presente nella visualizzazione del sottoalbero. È tuttavia possibile passare [**l'oggetto IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) che rappresenta la barra di scorrimento a **IUIAutomationTreeWalker::Normalize** e recuperare il predecessore più vicino presente nella visualizzazione contenuto.

Per esempi di codice che illustrano come usare [**l'interfaccia IUIAutomationTreeWalker,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) vedere [How to Walk the Automazione interfaccia utente Tree](uiauto-howto-walk-uiautomation-tree.md).

## <a name="other-ways-to-retrieve-an-element"></a>Altri modi per recuperare un elemento

Oltre alle ricerche e alla navigazione, è possibile recuperare un [**oggetto IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) nei modi seguenti.

### <a name="from-an-event"></a>Da un evento

Quando l'applicazione riceve un evento Automazione interfaccia utente, l'oggetto di origine passato al gestore eventi è rappresentato da [**un oggetto IUIAutomationElement.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) Ad esempio, se si sottoscriveno eventi di modifica dello stato attivo, l'origine passata a [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) è l'elemento che ha ricevuto lo stato attivo. Per altre informazioni, vedere Sottoscrizione di [Automazione interfaccia utente eventi](uiauto-eventsforclients.md).

### <a name="from-a-point"></a>Da un punto

Per recuperare un [**oggetto IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) dalle coordinate dello schermo, ad esempio la posizione del cursore, usare il [**metodo IUIAutomation::ElementFromPoint.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)

### <a name="from-a-window-handle"></a>Da un handle di finestra

Per recuperare un [**oggetto IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) da **un oggetto HWND,** usare il [**metodo IUIAutomation::ElementFromHandle.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle)

### <a name="from-the-focused-control"></a>Dal controllo con lo stato attivo

Per recuperare un [**oggetto IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) che rappresenta il controllo con lo stato attivo, usare il [**metodo IUIAutomation::GetFocusedElement.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)

## <a name="related-topics"></a>Argomenti correlati

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)

[Automazione interfaccia utente'app di esempio del client del contenuto del documento](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient)
