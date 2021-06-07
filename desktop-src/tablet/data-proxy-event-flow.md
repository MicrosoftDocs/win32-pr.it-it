---
description: Questo argomento illustra i dettagli dell'evento quando si usano le funzionalità proxy dei dati di analisi input penna.
ms.assetid: 837867a4-7cda-41b0-b20d-eec9a3a7fb86
title: Flusso di eventi del proxy dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b88fbb43e54b19486a6413bc44319fa2dd737486
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432543"
---
# <a name="data-proxy-event-flow"></a>Flusso di eventi del proxy dati

Questo argomento illustra i dettagli dell'evento quando si usano le funzionalità proxy dei dati di analisi input penna.

## <a name="data-proxy-event-flow-overview"></a>Panoramica del flusso di eventi del proxy dati

Nell'utilizzo del proxy dei dati di [**InkAnalyzer**](inkanalyzer.md)si presuppone che l'applicazione che integra InkAnalyzer abbia già un modello di documento esistente a cui desiderano proxyare i risultati dell'analisi. Si presuppone inoltre che l'applicazione abbia i risultati di qualsiasi operazione di analisi precedente che desidera creare in base all'archiviazione nel modello di documento. Potrebbe anche essere presente un contesto non input penna che può essere aggiunto a **InkAnalyzer** sotto forma di **ImageNode** o **TextWordNode**[**ContextNode**](icontextnode.md) per essere potenzialmente annotato con l'input penna.

La chiave per il sistema proxy di dati è che l'applicazione contrassegni [**ContextNode**](icontextnode.md) come "parzialmente popolato" usando [**PartiallyPopulated.**](icontextnode-setpartiallypopulated.md) Quando questo flag è [**true, InkAnalyzer**](inkanalyzer.md) presuppone che siano disponibili tre elementi relativi a **Tale ContextNode:**

-   La posizione di [**ContextNode**](icontextnode.md) è corretta.
-   Il tipo di [**ContextNode**](icontextnode.md) è corretto.
-   Tutte le altre informazioni su [**tale ContextNode**](icontextnode.md) vengono archiviate altrove.

In base a queste tre regole, se e quando [**InkAnalyzer**](inkanalyzer.md) necessita di informazioni aggiuntive su [**un ContextNode,**](icontextnode.md) genererà l'evento [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) e farà riferimento a **ContextNode** in questione. In questo modo l'applicazione può impostare tutte le informazioni note su **tale ContextNode** prima che **InkAnalyzer** la animi in modo più dettagliato. Dopo la gestione di un evento **PopulateContextNode,** **l'oggetto ContextNode** in questione deve avere una proprietà location valida, il numero corretto di sottonodi impostati se si tratta di un contenitore **ContextNode** o se sono impostati i tratti corretti, usando [**SetStrokes**](icontextnode-setstrokes.md), se si tratta di un **contextNode** foglia input penna. Se non si imposta correttamente questa posizione e le informazioni sul sottonodo o sul tratto, verrà generata **un'eccezione InvalidOperation.** I sottonodi per un **contenitore ContextNode** possono essere impostati come parzialmente popolati, nel qual caso verranno generati più eventi **PopulateContextNode** se **InkAnalyzer** determina che saranno necessari per l'operazione di analisi corrente.

Le tabelle seguenti descrivono quando verrà generato l'evento [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) durante l'utilizzo di [**InkAnalyzer.**](inkanalyzer.md)

Dopo che [**InkAnalyzer**](inkanalyzer.md) ha calcolato alcuni aggiornamenti, verrà nuovamente visualizzato l'applicazione per aggiornare i risultati. Il primo evento generato è [**l'evento InkAnalyzerStateChanging.**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Questo evento indica semplicemente all'applicazione che lo stato dell'albero dell'oggetto **InkAnalyzer** sta per cambiare. In questo modo le applicazioni possono impostare il flag [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) su true in tutti [**i ContextNode con**](icontextnodes.md) stato archiviato altrove. **InkAnalyzer** genererà quindi una serie di [**eventi PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) per determinare lo stato corrente dei dati. Una volta che ciò è possibile, un'operazione di riconciliazione viene espulsa per determinare quali risultati in background possono ancora essere applicati.

Per applicare i risultati a [**InkAnalyzer, viene**](inkanalyzer.md) generata una serie di eventi di modifica dell'albero. Gli eventi di modifica dell'albero descrivono, passo per passo, tutte le modifiche necessarie per aggiornare i risultati. Questi eventi devono essere gestiti in modalità di sucessione senza interuption o annullamento. Se l'operazione di analisi viene annullata (tramite il metodo [**Abort)**](iinkanalyzer-abort.md) durante l'elaborazione degli eventi di modifica dell'albero, lo stato di **InkAnalyzer** non sarà valido e potrebbe essere necessario analizzare nuovamente l'intero documento.

Le tabelle seguenti descrivono quando gli eventi di modifica dell'albero vengono generati durante l'utilizzo di InkAnalyzer. Le tabelle fanno riferimento ai timestamp illustrati nel diagramma di flusso degli eventi seguente.

![Immagine che mostra il flusso tra l'interfaccia utente dell'applicazione e l'analizzatore in background](images/7a0a54af-889e-43ed-8689-7f2d685567bf.jpg)

### <a name="adding-a-stroke"></a>Aggiunta di un tratto



| Timestamp | Tipo o scopo dell'evento | Evento generato | Commento                          |
|--------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T1, T5 e T9<br/> | \[All'interno della chiamata a AddStroke() \] \[ Tree Exploration Event\]<br/> | [**Evento PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) generato<br/> | Potrebbero essere presenti n eventi [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) generati a seconda del numero di [**ContextNode non**](icontextnodes.md) classificati esistenti con un valore [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) impostato su true.<br/> |
| T1, T5 e T9<br/> | \[Evento di modifica dell'albero\]<br/>                                  | [**Evento ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) generato<br/>   | Verrà generato un solo [**evento ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) in seguito alla chiamata del [**metodo AddStroke.**](iinkanalyzer-addstroke.md) Tutti i tratti vengono aggiunti allo stesso ContextNode non [**classificato.**](icontextnode.md)<br/>                      |



 

### <a name="deleting-a-stroke"></a>Eliminazione di un tratto



| Timestamp | Tipo o scopo dell'evento | Evento generato | Commento                          |
|---------------------------|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T2, T6 e T10<br/> | \[All'interno della chiamata a [**RemoveStroke**](iinkanalyzer-removestroke.md)() \] \[ Tree exploration Event\]<br/> | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Evento generato<br/> | È possibile che vengano generati diversi eventi [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) a seconda del numero di [**ContextNode**](icontextnodes.md) correlati ai tratti eliminati con valore [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) impostato su true.<br/> |
| T2, T6 e T10<br/> | \[Evento di modifica dell'albero\]<br/>                                                                          | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Evento generato<br/> | Potrebbe essere generato un numero qualsiasi di [**eventi ContextNodeDeleting,**](-ianalysisproxyevents-contextnodedeleting.md) a seconda del contenuto dell'input penna da eliminare e della struttura di analisi corrente.<br/>                                                                                                       |



 

### <a name="calling-the-backgroundanalyze-method"></a>Chiamata del metodo BackgroundAnalyze



| Timestamp | Tipo o scopo dell'evento | Evento generato | Commento                          |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T3<br/>         | \[All'interno della chiamata a [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)() \] \[ Tree Exploration Event\]<br/> | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Evento generato<br/> | Potrebbe essere generato un numero n di eventi [**PopulateContextNode,**](-ianalysisproxyevents-populatecontextnode.md) a seconda del numero di [**ContextNode nell'albero**](icontextnodes.md) con valore [**PartiallyPopulated**](icontextnode-createpartiallypopulatedsubnode.md) true (un evento per [**ContextNode**](icontextnode.md) necessario nell'operazione di analisi corrente).<br/> |



 

### <a name="after-the-call-to-backgroundanalyze-returns"></a>Dopo la fine della chiamata a BackgroundAnalyze()



| Timestamp | Tipo o scopo dell'evento | Evento generato | Commento                          |
|-----------------------|---------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------|
| Da T3 a T7<br/>   | \[Eventi generati dal thread BG\]<br/> | Activity Event Raised<br/> | Durante questo periodo di analisi in background verranno generati diversi eventi activity.<br/> |



 

### <a name="when-intermediateresults-are-ready"></a>Quando IntermediateResults è pronto



| Timestamp | Tipo o scopo dell'evento | Evento generato | Commento                          |
|-----------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Da T7 a T8<br/>   | \[Eventi generati dal thread BG, che indica l'inizio della prima operazione di riconciliazione\]<br/> | [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Evento generato<br/>         | Viene generato [**un solo evento InkAnalyzerStateChanging.**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Questo evento viene generato prima di controllare lo stato di [**InkAnalyzer,**](inkanalyzer.md)offrendo all'applicazione la possibilità di impostare il valore [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) in qualsiasi nodo o di eseguire il blocco dei documenti locale necessario.<br/> |
| Da T7 a T8<br/>   | \[Evento di esplorazione dell'albero\]<br/>                                                              | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Evento generato<br/>                   | Potrebbe essere presente un numero n di [**eventi PopulateContextNode generati,**](-ianalysisproxyevents-populatecontextnode.md) a seconda del contenuto dell'input penna.<br/>                                                                                                                                                                                                                                               |
| Da T7 a T8<br/>   | \[Evento di modifica dell'albero\]<br/>                                                             | [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) Evento generato<br/>                     | Potrebbero essere generati n eventi [**ContextNodeCreated,**](-ianalysisproxyevents-contextnodecreated.md) a seconda del contenuto dell'input penna.<br/>                                                                                                                                                                                                                                                 |
| Da T7 a T8<br/>   | \[Evento di modifica dell'albero\]<br/>                                                             | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Evento generato<br/>                   | Potrebbe essere presente un numero n di [**eventi ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) generati, a seconda del contenuto dell'input penna.<br/>                                                                                                                                                                                                                                               |
| Da T7 a T8<br/>   | \[Evento di modifica dell'albero\]<br/>                                                             | [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)<br/>                | Potrebbero essere generati n eventi [**ContextNodeMovingToPosition,**](-ianalysisproxyevents-contextnodemovingtoposition.md) a seconda del contenuto dell'input penna.<br/>                                                                                                                                                                                                                               |
| Da T7 a T8<br/>   | \[Evento di modifica dell'albero\]<br/>                                                             | [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)<br/>                          | Potrebbero essere generati n eventi [**ContextNodeReparenting,**](-ianalysisproxyevents-contextnodereparenting.md) a seconda del contenuto dell'input penna.<br/>                                                                                                                                                                                                                                         |
| Da T7 a T8<br/>   | \[Evento di modifica dell'albero\]<br/>                                                             | [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)<br/>                                      | Potrebbero essere generati n eventi [**StrokeReparented,**](-ianalysisproxyevents-strokereparented.md) a seconda del contenuto dell'input penna.<br/>                                                                                                                                                                                                                                                     |
| Da T7 a T8<br/>   | \[Evento di modifica dell'albero\]<br/>                                                             | [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)<br/>                            | Potrebbero essere generati n eventi [**ContextNodeLinkAdding,**](-ianalysisproxyevents-contextnodelinkadding.md) a seconda del contenuto dell'input penna.<br/>                                                                                                                                                                                                                                           |
| Da T7 a T8<br/>   | \[Evento di modifica dell'albero\]<br/>                                                             | [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)<br/>                        | Potrebbero essere generati n eventi [**ContextNodeLinkDeleting,**](-ianalysisproxyevents-contextnodelinkdeleting.md) a seconda del contenuto dell'input penna.<br/>                                                                                                                                                                                                                                       |
| Da T7 a T8<br/>   | \[Evento di modifica dell'albero\]<br/>                                                             | [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) Evento generato<br/> | Potrebbero essere generati n eventi [**ContextNodePropertiesUpdated,**](-ianalysisproxyevents-contextnodepropertiesupdated.md) a seconda del contenuto dell'input penna. **ContextNodePropertiesUpdated è** pianificato per essere generato dopo che tutti gli altri eventi di modifica [**contextNode**](icontextnode.md) vengono generati durante questo periodo [**di riconciliazione.**](iinkanalyzer-reconcile.md)<br/>              |
| Da T7 a T8<br/>   | \[L'evento indica la fine della prima operazione di riconciliazione\]<br/>                            | [**IntermediateResults**](-ianalysisevents-intermediateresults.md) Evento generato<br/>                        | Verrà generato [**un solo evento IntermediateResults**](-ianalysisevents-intermediateresults.md) per ogni operazione di analisi.<br/>                                                                                                                                                                                                                                                                  |



 

### <a name="after-intermediateresults-have-been-handled"></a>Dopo la gestione di IntermediateResults



| Timestamp | Tipo di evento o scopo | Evento generato | Commento                          |
|-----------------------|---------------------------------------------|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Da T8 a T11<br/>  | \[Eventi generati dal thread BG\]<br/> | [**Attività**](-ianalysisevents-activity.md) Evento generato<br/> | Durante [**questo periodo**](-ianalysisevents-activity.md) di analisi in background verranno generati diversi eventi activity.<br/> |



 

### <a name="when-final-results-are-ready"></a>Quando i risultati finali sono pronti



| Timestamp | Tipo di evento o scopo | Evento generato | Commento                          |
|-----------------------|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Da T11 a T12<br/> | \[Eventi generati dal thread BG, che indica l'inizio della seconda operazione di riconciliazione\]<br/> | [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Evento generato<br/>         | Viene generato [**un solo evento InkAnalyzerStateChanging.**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Questo evento viene generato prima di controllare lo stato di [**InkAnalyzer,**](inkanalyzer.md)offrendo all'applicazione la possibilità di impostare il valore [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) in qualsiasi nodo o di eseguire il blocco dei documenti locale necessario.<br/> |
| Da T11 a T12<br/> | \[Evento di esplorazione albero\]<br/>                                                               | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Evento generato<br/>                   | Potrebbe essere generato un numero qualsiasi di [**eventi PopulateContextNode,**](-ianalysisproxyevents-populatecontextnode.md) a seconda del contenuto dell'input penna.<br/>                                                                                                                                                                                                                                             |
| Da T11 a T12<br/> | \[Evento di modifica dell'albero\]<br/>                                                              | [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) Evento generato<br/>                     | Potrebbe essere generato un numero qualsiasi di [**eventi ContextNodeCreated,**](-ianalysisproxyevents-contextnodecreated.md) a seconda del contenuto dell'input penna.<br/>                                                                                                                                                                                                                                               |
| Da T11 a T12<br/> | \[Evento di modifica dell'albero\]<br/>                                                              | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Evento generato<br/>                   | Potrebbe essere generato un numero qualsiasi di [**eventi ContextNodeDeleting,**](-ianalysisproxyevents-contextnodedeleting.md) a seconda del contenuto dell'input penna.<br/>                                                                                                                                                                                                                                             |
| Da T11 a T12<br/> | \[Evento di modifica dell'albero\]<br/>                                                              | [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)<br/>                | Potrebbe essere generato un numero qualsiasi di [**eventi ContextNodeMovingToPosition,**](-ianalysisproxyevents-contextnodemovingtoposition.md) a seconda del contenuto dell'input penna.<br/>                                                                                                                                                                                                                             |
| Da T11 a T12<br/> | \[Evento di modifica dell'albero\]<br/>                                                              | [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)<br/>                          | Potrebbe essere generato un numero qualsiasi di [**eventi ContextNodeReparenting,**](-ianalysisproxyevents-contextnodereparenting.md) a seconda del contenuto dell'input penna.<br/>                                                                                                                                                                                                                                       |
| Da T11 a T12<br/> | \[Evento di modifica dell'albero\]<br/>                                                              | [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)<br/>                                      | Potrebbe essere generato un numero qualsiasi di [**eventi StrokeReparented,**](-ianalysisproxyevents-strokereparented.md) a seconda del contenuto dell'input penna.<br/>                                                                                                                                                                                                                                                   |
| Da T11 a T12<br/> | \[Evento di modifica dell'albero\]<br/>                                                              | [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)<br/>                            | Potrebbe essere generato un numero qualsiasi di [**eventi ContextNodeLinkAdding,**](-ianalysisproxyevents-contextnodelinkadding.md) a seconda del contenuto dell'input penna.<br/>                                                                                                                                                                                                                                         |
| Da T11 a T12<br/> | \[Evento di modifica dell'albero\]<br/>                                                              | [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)<br/>                        | Potrebbe essere generato un numero qualsiasi di [**eventi ContextNodeLinkDeleting,**](-ianalysisproxyevents-contextnodelinkdeleting.md) a seconda del contenuto dell'input penna.<br/>                                                                                                                                                                                                                                     |
| Da T11 a T12<br/> | \[Evento di modifica dell'albero\]<br/>                                                              | [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) Evento generato<br/> | Potrebbe essere generato un numero qualsiasi di [**eventi ContextNodePropertiesUpdated,**](-ianalysisproxyevents-contextnodepropertiesupdated.md) a seconda del contenuto dell'input penna. **ContextNodePropertiesUpdated è** pianificato per essere generato dopo che tutti gli altri eventi di modifica [**contextNode**](icontextnode.md) vengono generati durante questo periodo [**di riconciliazione.**](iinkanalyzer-reconcile.md)<br/>            |
| Da T11 a T12<br/> | \[L'evento indica la fine della seconda operazione di riconciliazione\]<br/>                            | [**Risultati**](-ianalysisevents-results.md) Evento generato<br/>                                                | Verrà generato [**un solo**](-ianalysisevents-results.md) evento Results per ogni operazione di analisi.<br/>                                                                                                                                                                                                                                                                                          |



 

 

 




