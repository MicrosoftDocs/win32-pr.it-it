---
title: Panoramica dell'albero di automazione dell'interfaccia utente
description: I prodotti di Assistive Technology e gli script di test esplorano l'albero di automazione interfaccia utente Microsoft per raccogliere informazioni sull'interfaccia utente e i relativi elementi.
ms.assetid: f3afe258-baa7-41b5-a27e-cdc94b467d73
keywords:
- Automazione interfaccia utente, panoramica dell'albero
- Automazione interfaccia utente, visualizzazione dell'albero
- Automazione interfaccia utente, visualizzazione non elaborata dell'albero
- Automazione interfaccia utente, visualizzazione controlli dell'albero
- Automazione interfaccia utente, visualizzazione contenuto dell'albero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76bc9aa6568a3f4d63194d35ff0c7d8f59510c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855938"
---
# <a name="ui-automation-tree-overview"></a>Panoramica dell'albero di automazione dell'interfaccia utente

I prodotti di Assistive Technology e gli script di test esplorano l'albero di automazione interfaccia utente Microsoft per raccogliere informazioni sull'interfaccia utente e i relativi elementi.

Nell'albero di automazione interfaccia utente è un elemento radice che rappresenta la finestra del desktop di Windows ("desktop") e i cui elementi figlio rappresentano le finestre dell'applicazione. Ognuno di questi elementi figlio può contenere elementi che rappresentano parti dell'interfaccia utente, ad esempio menu, pulsanti, barre degli strumenti e caselle di riepilogo. Questi elementi possono contenere elementi, ad esempio elementi elenco.

La struttura ad albero di automazione interfaccia utente non è fissa. Viene raramente visualizzato nella sua totale, perché potrebbe contenere migliaia di elementi. Le parti della struttura ad albero di automazione interfaccia utente sono compilate come un client necessario e la struttura dell'albero cambia quando gli elementi vengono aggiunti, spostati o rimossi.

I provider di automazione interfaccia utente supportano l'albero di automazione interfaccia utente implementando la navigazione tra gli elementi di un frammento. Un frammento è un sottoalbero completo di elementi di un particolare Framework e dispone di un elemento radice (denominato *radice del frammento*) che in genere è ospitato in una finestra.

I provider non sono interessati alla navigazione da un controllo a un altro. Questo è gestito dal core di automazione interfaccia utente, che usa le informazioni dei provider di finestra predefiniti.

In questo argomento sono contenute le sezioni seguenti.

-   [Visualizzazioni dell'albero di automazione interfaccia utente](#views-of-the-ui-automation-tree)
    -   [Visualizzazione non elaborata](#raw-view)
    -   [Visualizzazione controlli](#control-view)
    -   [Visualizzazione contenuto](#content-view)
-   [Argomenti correlati](#related-topics)

## <a name="views-of-the-ui-automation-tree"></a>Visualizzazioni dell'albero di automazione interfaccia utente

L'albero di automazione interfaccia utente può essere filtrato per creare visualizzazioni che contengono solo gli elementi di automazione interfaccia utente pertinenti per un determinato client. Questo approccio consente ai client di personalizzare la struttura presentata tramite automazione interfaccia utente in base alle esigenze specifiche.

Il client può personalizzare la visualizzazione in base all'ambito e filtrando. L'ambito definisce l'ambito della visualizzazione, a partire da un elemento di base. Ad esempio, l'applicazione potrebbe voler trovare solo gli elementi figlio diretti del desktop o tutti i discendenti di una finestra dell'applicazione. Il filtro definisce i tipi di elementi inclusi nella visualizzazione.

I provider di automazione interfaccia utente supportano il filtraggio definendo proprietà sugli elementi, incluse le proprietà [**IUIAutomationElement::**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) [**IUIAutomationElement:: dataconteelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) .

Automazione interfaccia utente offre tre visualizzazioni predefinite: visualizzazione non elaborata, visualizzazione controlli e visualizzazione contenuto. Queste viste sono definite dal tipo di filtro eseguito. L'ambito di qualsiasi visualizzazione è definito dall'applicazione. L'applicazione può applicare altri filtri sulle proprietà; ad esempio, per includere solo i controlli abilitati in una visualizzazione controlli.

### <a name="raw-view"></a>Visualizzazione non elaborata

La visualizzazione non elaborata dell'albero di automazione interfaccia utente è la struttura completa degli elementi di automazione per i quali il desktop è la radice. La visualizzazione non elaborata segue strettamente la struttura nativa a livello di codice di un'applicazione ed è la visualizzazione più dettagliata disponibile. Costituisce inoltre la base sulla quale vengono compilate le altre visualizzazioni dell'albero. Poiché questa vista dipende dal framework dell'interfaccia utente sottostante, la visualizzazione non elaborata di un pulsante Windows Presentation Foundation (WPF) ha una visualizzazione non elaborata diversa da quella di un pulsante di Microsoft Win32.

La visualizzazione non elaborata viene ottenuta cercando elementi senza specificare proprietà o usando [**IUIAutomation:: RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker) per ottenere un'interfaccia [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) per spostarsi nell'albero.

### <a name="control-view"></a>Visualizzazione controlli

La visualizzazione controlli è un sottoinsieme della visualizzazione non elaborata. Include solo gli elementi dell'interfaccia utente la cui proprietà [**IUIAutomationElement::**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) IsSynchronized è impostata su **true**.

La visualizzazione controlli include gli elementi dell'interfaccia utente che forniscono informazioni all'utente o consentono all'utente di eseguire un'azione. Si tratta degli elementi dell'interfaccia utente più interessanti per le applicazioni di test automatizzato.

La visualizzazione controlli include anche elementi dell'interfaccia utente non interattivi che contribuiscono alla struttura logica dell'interfaccia utente. Sono inclusi i contenitori di elementi, ad esempio le intestazioni di visualizzazione elenco, le barre degli strumenti, i menu e la barra di stato. Gli altri elementi non interattivi visualizzati nella visualizzazione controlli sono grafici con informazioni e testo statico in una finestra di dialogo.

Gli elementi non interattivi utilizzati solo a scopo di layout o decorativo, ad esempio i pannelli utilizzati per disporre i controlli in una finestra di dialogo, non vengono visualizzati nella visualizzazione controlli.

La visualizzazione controlli dell'albero di automazione interfaccia utente è strettamente mappata alla struttura dell'interfaccia utente percepita da un utente finale. Questo rende più semplice per il prodotto Assistive Technology descrivere l'interfaccia utente per l'utente finale e consentire all'utente finale di interagire con l'applicazione.

La visualizzazione controlli viene ottenuta cercando gli elementi la cui proprietà [**IUIAutomationElement::**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) ControlViewWalker è impostata su true oppure usando [](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) per ottenere un'interfaccia [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) per spostarsi nell'albero.

### <a name="content-view"></a>Visualizzazione contenuto

La visualizzazione contenuto dell'albero di automazione interfaccia utente è un subset della visualizzazione controlli. Include solo gli elementi dell'interfaccia utente con la proprietà [**IUIAutomationElement::**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) IUIAutomationElement:: IsSynchronized e la proprietà [**::**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) IsSynchronized impostata su **true**.

La visualizzazione contenuto contiene elementi dell'interfaccia utente che contengono le informazioni effettive in un'interfaccia utente, inclusi gli elementi dell'interfaccia utente che possono ricevere lo stato attivo e il testo che non è un'etichetta di un elemento dell'interfaccia utente. Si tratta degli elementi dell'interfaccia utente più interessanti per un'applicazione per la lettura dello schermo. Ad esempio, i valori in una casella combinata a discesa vengono visualizzati nella visualizzazione contenuto perché i valori rappresentano le informazioni utilizzate da un utente finale.

Nella visualizzazione contenuto, una casella combinata e una casella di riepilogo sono entrambe rappresentate come una raccolta di elementi dell'interfaccia utente in cui è possibile selezionare uno o più elementi. Il fatto che un elemento sia sempre aperto e che un elemento possa espandersi e comprimere è irrilevante nella visualizzazione contenuto perché è progettato per mostrare i dati, o il contenuto, che vengono presentati all'utente.

La visualizzazione del contenuto viene ottenuta cercando gli elementi che hanno sia [**l'oggetto e la**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) proprietà [**CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) impostati su **true** oppure [**IUIAutomation:: ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) per ottenere un'interfaccia [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) per spostarsi nell'albero.

Le immagini seguenti mostrano le differenze tra la visualizzazione controlli e la visualizzazione contenuto. La prima immagine mostra una casella combinata semplice con tre elementi nell'elenco a discesa. La seconda immagine mostra come vengono visualizzati gli elementi dell'interfaccia utente della casella combinata nelle visualizzazioni controllo e contenuto dell'applicazione UISpy.exe.

![Screenshot di una casella combinata semplice con tre elementi a discesa](images/combobox.png)

![screenshot dell'applicazione UISpy con visualizzazioni del contenuto e del controllo degli elementi della casella combinata](images/treeviews.jpg)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Creazione dell'oggetto CUIAutomation](uiauto-creatingcuiautomation.md)
</dt> <dt>

[Ottenere elementi di automazione interfaccia utente](uiauto-obtainingelements.md)
</dt> <dt>

[Nozioni fondamentali sull'automazione interfaccia utente](entry-uiautocore-overview.md)
</dt> </dl>

 

 




