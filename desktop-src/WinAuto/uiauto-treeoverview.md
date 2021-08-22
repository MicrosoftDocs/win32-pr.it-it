---
title: Panoramica dell'albero di automazione dell'interfaccia utente
description: I prodotti di assistive technology e gli script di test esplorano l'albero di Microsoft Automazione interfaccia utente per raccogliere informazioni sull'interfaccia utente e sui relativi elementi.
ms.assetid: f3afe258-baa7-41b5-a27e-cdc94b467d73
keywords:
- Automazione interfaccia utente,panoramica dell'albero
- Automazione interfaccia utente,visualizzazione dell'albero
- Automazione interfaccia utente,visualizzazione non elaborata dell'albero
- Automazione interfaccia utente,controllare la visualizzazione dell'albero
- Automazione interfaccia utente,visualizzazione contenuto dell'albero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e1b8776f86931882acc85e2fb974ff5d1db0be266be94e391ce242ff2a497e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570402"
---
# <a name="ui-automation-tree-overview"></a>Panoramica dell'albero di automazione dell'interfaccia utente

I prodotti di assistive technology e gli script di test esplorano l'albero di Microsoft Automazione interfaccia utente per raccogliere informazioni sull'interfaccia utente e sui relativi elementi.

Nell'Automazione interfaccia utente albero è un elemento radice che rappresenta la finestra Windows desktop ("desktop") e i cui elementi figlio rappresentano le finestre dell'applicazione. Ognuno di questi elementi figlio può contenere elementi che rappresentano parti dell'interfaccia utente, ad esempio menu, pulsanti, barre degli strumenti e caselle di riepilogo. Questi elementi possono contenere elementi, ad esempio elementi di elenco.

L Automazione interfaccia utente albero non è una struttura fissa. Raramente è visibile nella sua totalità perché potrebbe contenere migliaia di elementi. Le parti dell Automazione interfaccia utente albero vengono compilate in base alle esigenze di un client e la struttura dell'albero cambia quando gli elementi vengono aggiunti, spostati o rimossi.

Automazione interfaccia utente provider di servizi supportano l'Automazione interfaccia utente struttura ad albero implementando lo spostamento tra gli elementi in un frammento. Un frammento è un sottoalbero completo di elementi di un particolare framework e ha un elemento radice (denominato radice del frammento *)* che in genere è ospitato in una finestra.

I provider non sono interessati alla navigazione da un controllo a un altro. Questa operazione viene gestita dal Automazione interfaccia utente core, che usa le informazioni dei provider di finestre predefiniti.

In questo argomento sono contenute le sezioni seguenti.

-   [Visualizzazioni dell'albero Automazione interfaccia utente dati](#views-of-the-ui-automation-tree)
    -   [Visualizzazione non elaborata](#raw-view)
    -   [Visualizzazione controlli](#control-view)
    -   [Visualizzazione contenuto](#content-view)
-   [Argomenti correlati](#related-topics)

## <a name="views-of-the-ui-automation-tree"></a>Visualizzazioni dell'albero Automazione interfaccia utente dati

La Automazione interfaccia utente albero può essere filtrata per creare viste che contengono solo Automazione interfaccia utente elementi rilevanti per un client specifico. Questo approccio consente ai client di personalizzare la struttura presentata tramite Automazione interfaccia utente in base alle esigenze specifiche.

Il client può personalizzare la visualizzazione con l'ambito e filtrando. L'ambito è la definizione dell'estensione della vista, a partire da un elemento di base. Ad esempio, l'applicazione potrebbe voler trovare solo gli elementi figlio diretti del desktop o tutti i discendenti di una finestra dell'applicazione. Il filtro definisce i tipi di elementi inclusi nella visualizzazione.

Automazione interfaccia utente provider supportano il filtro definendo proprietà sugli elementi, incluse le proprietà [**IUIAutomationElement::IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) e [**IUIAutomationElement::IsContentElement.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement)

Automazione interfaccia utente fornisce tre visualizzazioni predefinite: visualizzazione non elaborata, visualizzazione controllo e visualizzazione contenuto. Queste viste sono definite dal tipo di filtro eseguito. L'ambito di qualsiasi vista è definito dall'applicazione. L'applicazione può applicare altri filtri alle proprietà. ad esempio per includere solo i controlli abilitati in una visualizzazione controlli.

### <a name="raw-view"></a>Visualizzazione non elaborata

La visualizzazione non elaborata dell'Automazione interfaccia utente albero è l'albero completo degli elementi di automazione per cui il desktop è la radice. La visualizzazione non elaborata segue da vicino la struttura programmatica nativa di un'applicazione ed è la visualizzazione più dettagliata disponibile. Costituisce inoltre la base sulla quale vengono compilate le altre visualizzazioni dell'albero. Poiché questa visualizzazione dipende dal framework dell'interfaccia utente sottostante, la visualizzazione non elaborata di un pulsante Windows Presentation Foundation (WPF) ha una visualizzazione non elaborata diversa da un pulsante Microsoft Win32.

La visualizzazione non elaborata viene ottenuta cercando elementi senza specificare proprietà o usando [**IUIAutomation::RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker) per ottenere [**un'interfaccia IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) per lo spostamento nell'albero.

### <a name="control-view"></a>Visualizzazione controlli

La visualizzazione controlli è un sottoinsieme della visualizzazione non elaborata. Include solo gli elementi dell'interfaccia utente la cui proprietà [**IUIAutomationElement::IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) è impostata su **TRUE.**

La visualizzazione controllo include gli elementi dell'interfaccia utente che forniscono informazioni all'utente o consentono all'utente di eseguire un'azione. Si tratta degli elementi dell'interfaccia utente più interessanti per le applicazioni di test automatizzate.

La visualizzazione controlli include anche elementi dell'interfaccia utente non interattivi che contribuiscono alla struttura logica dell'interfaccia utente. Sono inclusi contenitori di elementi, ad esempio intestazioni di visualizzazione elenco, barre degli strumenti, menu e barra di stato. Altri elementi non interattivi visualizzati nella visualizzazione controlli sono elementi grafici con informazioni e testo statico in una finestra di dialogo.

Gli elementi non interattivi usati solo per scopi di layout o decorativi, ad esempio i pannelli usati per il layout dei controlli in una finestra di dialogo, non vengono visualizzati nella visualizzazione controlli.

La visualizzazione di controllo della struttura Automazione interfaccia utente mappa strettamente alla struttura dell'interfaccia utente percepita da un utente finale. Ciò rende più semplice per il assistive technology prodotto descrivere l'interfaccia utente all'utente finale e consentire all'utente finale di interagire con l'applicazione.

La visualizzazione controlli viene ottenuta cercando gli elementi la cui proprietà [**IUIAutomationElement::IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) è impostata su true oppure usando [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) per ottenere un'interfaccia [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) per l'esplorazione della struttura ad albero.

### <a name="content-view"></a>Visualizzazione contenuto

La visualizzazione contenuto dell'albero Automazione interfaccia utente è un subset della visualizzazione controlli. Include solo gli elementi dell'interfaccia utente con la proprietà [**IUIAutomationElement::IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) e [**la proprietà IUIAutomationElement::IsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) impostata su **TRUE.**

La visualizzazione contenuto contiene elementi dell'interfaccia utente che comunicano le informazioni effettive in un'interfaccia utente, inclusi gli elementi dell'interfaccia utente che possono ricevere lo stato attivo della tastiera e un testo che non è un'etichetta in un elemento dell'interfaccia utente. Si tratta degli elementi dell'interfaccia utente più interessanti per un'applicazione di lettura dello schermo. Ad esempio, i valori in una casella combinata a discesa vengono visualizzati nella visualizzazione contenuto perché rappresentano le informazioni usate da un utente finale.

Nella visualizzazione contenuto, una casella combinata e una casella di riepilogo sono entrambe rappresentate come una raccolta di elementi dell'interfaccia utente in cui è possibile selezionare uno o più elementi. Il fatto che un elemento sia sempre aperto e che un elemento possa espandersi e comprimere è irrilevante nella visualizzazione contenuto perché è progettato per visualizzare i dati, o il contenuto, presentati all'utente.

La visualizzazione contenuto viene ottenuta cercando elementi con la proprietà [**IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) e [**CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) impostata su **TRUE** oppure [**usando IUIAutomation::ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) per ottenere un'interfaccia [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) per l'esplorazione della struttura ad albero.

Le immagini seguenti illustrano le differenze tra la visualizzazione controlli e la visualizzazione contenuto. La prima immagine mostra una semplice casella combinata con tre elementi nell'elenco a discesa. La seconda immagine mostra come vengono visualizzati gli elementi dell'interfaccia utente della casella combinata nelle visualizzazioni controllo e contenuto dellUISpy.exe app.

![Screenshot di una casella combinata semplice con tre elementi a discesa](images/combobox.png)

![Screenshot dell'applicazione uispy con le visualizzazioni controllo e contenuto degli elementi della casella combinata](images/treeviews.jpg)

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

 

 




