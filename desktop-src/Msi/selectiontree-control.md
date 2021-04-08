---
description: Questo controllo consente a un utente di modificare lo stato di selezione delle funzionalità elencate nella tabella delle funzionalità.
ms.assetid: 0daf5b44-ba07-47f1-95d9-28c59f7cf985
title: Controllo SelectionTree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5287736c3293c736d6d392ce8532b76ee7b62ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885481"
---
# <a name="selectiontree-control"></a>Controllo SelectionTree

Questo controllo consente a un utente di modificare lo stato di selezione delle funzionalità elencate nella [tabella delle funzionalità](feature-table.md). Il controllo è associato a una proprietà con valori di stringa che l'utente può impostare tramite una [finestra di dialogo di esplorazione](browse-dialog.md). È possibile associare il controllo a una proprietà immettendo il nome della proprietà nella colonna proprietà della [tabella dei controlli](control-table.md).

Il controllo SelectionTree pubblica automaticamente gli eventi di [controllo](control-events.md) seguenti in Windows XP o nei sistemi operativi precedenti. Il controllo SelectionTree pubblica questi eventi quando l'elemento selezionato viene modificato da un nodo a un altro. Se l'albero di selezione non contiene nodi, il controllo pubblica questi eventi e cancella il contenuto dei controlli che sottoscrivono l'evento. Non è necessario che questi ControlEvents siano elencati nella [tabella ControlEvent](controlevent-table.md).



| Evento di controllo                                                 | Descrizione                                                                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [SelectionAction](selectionaction-controlevent.md)           | Pubblica una stringa dalla [tabella UIText](uitext-table.md) che descrive l'elemento evidenziato.      |
| [SelectionBrowse](selectionbrowse-controlevent.md)           | Genera una finestra di dialogo Sfoglia utilizzata per modificare il percorso dell'elemento evidenziato.                     |
| [SelectionDescription](selectiondescription-controlevent.md) | Pubblica una stringa dalla tabella delle [funzionalità](feature-table.md) che descrive l'elemento evidenziato.    |
| [SelectionNoItems](selectionnoitems-controlevent.md)         | Elimina il testo descrittivo o Disabilita i pulsanti di un elemento obsoleto.                          |
| [SelectionPath](selectionpath-controlevent.md)               | Pubblica il percorso per l'elemento evidenziato.                                                       |
| [SelectionPathOn](selectionpathon-controlevent.md)           | Pubblica se è presente o meno un percorso di selezione associato alla funzionalità attualmente selezionata. |
| [SelectionSize](selectionsize-controlevent.md)               | Pubblica la dimensione dell'elemento evidenziato.                                                        |



 

A partire dai sistemi Windows Server 2003, i controlli SelectionTree pubblicano tutti gli eventi nella tabella precedente e, inoltre, pubblicano un [DoAction ControlEvent](doaction-controlevent.md) o una [Proprietà ControlEvent](setproperty-controlevent.md). I record devono essere aggiunti alla [tabella ControlEvent](controlevent-table.md) per pubblicare DoAction o SetProperty ControlEvents.



| Evento di controllo                               | Descrizione                                        |
|---------------------------------------------|----------------------------------------------------|
| [DoAction](doaction-controlevent.md)       | Notifica al programma di installazione di eseguire un'azione personalizzata. |
| [SetProperty](setproperty-controlevent.md) | Imposta una proprietà su un nuovo valore.                    |



 

A partire da Windows Installer versione 3,0, i controlli SelectionTree pubblicano un evento che esegue [azioni personalizzate](custom-actions.md) elencate nella [tabella ControlEvent](controlevent-table.md). Il controllo SelectionTree pubblica questo evento ogni volta che la selezione delle caratteristiche cambia nel controllo o ogni volta che viene scelto uno stato di selezione diverso per la funzionalità corrente. Le azioni personalizzate vengono eseguite ogni volta che viene pubblicato l'evento. Il controllo SelectionTree invia informazioni all'azione personalizzata impostando i valori delle proprietà seguenti. Tutte queste proprietà vengono cancellate quando il controllo SelectionTree viene chiuso.

**Windows Installer 2,0:** Non supportato. Il controllo SelectionTree non pubblica l'evento e non imposta le proprietà seguenti.



| Proprietà                                | Descrizione                                                                                                                                                      |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MsiSelectionTreeSelectedFeature         | Nome della funzionalità selezionata nel campo funzionalità della [tabella delle funzionalità](feature-table.md).                                                                      |
| MsiSelectionTreeSelectedAction          | Stato dell'azione di installazione della funzionalità selezionata. Il valore può essere INSTALLSTATE \_ assente, InstallState \_ locale, InstallState \_ origine o InstallState \_ annunciata. |
| MsiSelectonTreeChildrenCount            | Numero di nodi figlio diretti.                                                                                                                                    |
| MsiSelectionTreeInstallingChildrenCount | Numero di nodi figlio diretti INSTALLSTATE \_ locale, \_ origine INSTALLSTATE o InstallState \_ annunciati.                                                    |
| MsiSelectionTreeSelectedCost            | Costo dell'installazione della funzionalità selezionata in unità di 512 byte.                                                                                                   |
| MsiSelectionTreeChildrenCost            | Costo dell'installazione di tutte le funzionalità figlio in unità di 512 byte.                                                                                              |
| MsiSelectionTreeSelectedPath            | Percorso in cui viene installata la funzionalità selezionata. Definito solo se la funzionalità viene installata come INSTALLSTATE \_ locale.                                       |



 

> [!Note]
>
> Il contenuto del campo di testo della [tabella dei controlli](control-table.md) non viene mai visualizzato dal controllo SelectionTree. Questo campo specifica invece lo stile di testo che deve essere visualizzato dal controllo e contiene una descrizione del controllo usato dalle utilità di revisione dello schermo. Per impostare il tipo di carattere e lo stile del carattere di una stringa di testo, anteporre alla stringa dei caratteri visualizzati lo stile { \\ Style} o {&*Style*}. Dove Style è un identificatore elencato nella colonna TextStyle della [tabella TextStyle](textstyle-table.md). Se nessuna di queste è presente, ma la proprietà [**DefaultUIFont**](defaultuifont.md) è definita come uno stile di testo valido, viene usato il tipo di carattere. Le informazioni riportate di seguito vengono lette dalle utilità di revisione dello schermo come descrizione del controllo. Vedere [accessibilità](accessibility.md).

 

## <a name="control-attributes"></a>Attributi del controllo

Con questo controllo è possibile usare gli attributi seguenti. Per modificare il valore di un attributo utilizzando un evento, sottoscrivere il controllo in un ControlEvent nella [tabella EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna attributo. Immettere l'identificatore del ControlEvent nella colonna evento.



| Identificatore di attributo                                               | Bit esadecimale                  | Descrizione                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Nome di una proprietà indiretta associata al controllo. Se viene impostato il bit di attributo indiretto, il controllo Visualizza o modifica il valore della proprietà con questo nome. Se viene impostato il bit di attributo indiretto, questo nome è anche il valore della proprietà elencata nella colonna proprietà della [tabella dei controlli](control-table.md).                                    |
| [Position](position-control-attribute.md)                         |                                  | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate del controllo dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella del controllo](control-table.md). Usare le [unità del programma di installazione](installer-units.md) per lunghezza e distanza.<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Nome della proprietà associata a questo controllo. Se il bit di attributo indiretto non è impostato, il controllo Visualizza o modifica il valore della proprietà con questo nome. Questo attributo viene specificato nella colonna proprietà della tabella dei [controlli](control-table.md).                                                                                                    |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valore corrente della proprietà visualizzata o modificata da questo controllo. Se il bit di attributo indiretto non è impostato, questo è il valore di PropertyName. Se viene impostato il bit di attributo indiretto, questo è il valore di IndirectPropertyName. Se l'attributo viene modificato, il controllo riflette il nuovo valore.                                                                           |
| [Text](text-control-attribute.md)                                 |                                  | Visualizza il testo in utilità in base al testo immesso nella colonna di testo della [tabella dei controlli](control-table.md). Vedere [accessibilità](accessibility.md).                                                                                                                                                                                                          |
| [Visible](visible-control-attribute.md)                           | 0x00000001 0x00000000<br/> | Controllo nascosto. Controllo visibile.<br/> Includere questo bit nella parola bit della colonna attributi nella [tabella dei controlli](control-table.md) per rendere il controllo visibile o nascosto alla sua creazione.<br/> È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/>                                     |
| [Enabled](enabled-control-attribute.md)                           | 0x00000002 0x00000000<br/> | Controllo in uno stato disabilitato. Controllo in uno stato abilitato.<br/> Includere questo bit nella parola bit nella colonna attributi del [controllo](control-table.md) per abilitare il controllo alla creazione.<br/> È anche possibile abilitare o disabilitare un controllo tramite la [tabella ControlCondition](controlcondition-table.md).<br/>                                   |
| [Sunken](sunken-control-attribute.md)                             | 0x00000004 0x00000000<br/> | Visualizza lo stile di visualizzazione predefinito. Visualizza il controllo con un aspetto incassato, 3D.<br/> Includere questi bit nella parola bit nella colonna attributi della [tabella dei controlli](control-table.md).<br/>                                                                                                                                                             |
| [Indiretto](indirect-control-attribute.md)                         | 0x00000008 0x00000000<br/> | Il controllo Visualizza o modifica il valore della proprietà nella colonna proprietà della [tabella dei controlli](control-table.md). Il controllo Visualizza o modifica il valore della proprietà con l'identificatore elencato nella colonna proprietà della tabella dei controlli.<br/> Determina se viene fatto riferimento indirettamente alla proprietà associata a questo controllo.<br/> |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000020 0x00000000<br/> | Il testo nel controllo viene visualizzato nell'ordine di lettura da sinistra a destra. Il testo nel controllo viene visualizzato in ordine di lettura da destra a sinistra.<br/>                                                                                                                                                                                                                              |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000040 0x00000000<br/> | Il testo nel controllo è allineato a sinistra. Il testo nel controllo è allineato a destra.<br/>                                                                                                                                                                                                                                                                       |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000080 0x00000000<br/> | La barra di scorrimento si trova sul lato destro del controllo. La barra di scorrimento si trova sul lato sinistro del controllo.<br/>                                                                                                                                                                                                                                         |
| [BiDi](bidi-control-attribute.md)                                 | 0x000000E0                       | Impostare questo valore per una combinazione degli attributi [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)e [LeftScroll](leftscroll-control-attribute.md) .                                                                                                                                                                          |



 

## <a name="remarks"></a>Commenti

Questo controllo può essere creato dalla \_ classe TreeView di WC tramite la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Dispone degli stili **WS \_ Border**, **TV \_ HASLINES**, **TV \_ HASBUTTONS**, **TV \_ LINESATROOT**, **TV \_ DISABLEDRAGDROP**, **TV \_ SHOWSELALWAYS**, **WS \_ child**, **WS \_ TABSTOP** e **WS \_ Group** .

La struttura ad albero di selezione viene popolata solo se sono state chiamate l'azione [CostInitialize](costinitialize-action.md) e l' [azione CostFinalize secondo](costfinalize-action.md) .

La stringa seguente nella [tabella UIText](uitext-table.md) è correlata a questo controllo.



| Termine                                                                                                         | Descrizione                                                    |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="AbsentPath"></span><span id="absentpath"></span><span id="ABSENTPATH"></span>AbsentPath<br/> | Percorso visualizzato per un elemento nello stato assente.<br/> |



 

Per visualizzare il numero di elementi figlio selezionati e le dimensioni associate all'elemento evidenziato, vengono utilizzate le sei stringhe seguenti:

-   SelChildCostPos
-   SelChildCostNeg
-   SelParentCostPosPos
-   SelParentCostPosNeg
-   SelParentCostNegPos
-   SelParentCostNegNeg

Per visualizzare le opzioni di selezione disponibili per un elemento in un menu popup, vengono utilizzate le stringhe seguenti:

-   MenuAbsent
-   MenuLocal
-   MenuCD
-   MenuNetwork
-   MenuAllLocal
-   MenuAllCD
-   MenuAllNetwork

Le stringhe seguenti vengono usate per spiegare la selezione presente in [SelectionDescription](selectiondescription-controlevent.md) ControlEvent.

-   SelAbsentAbsent
-   SelAbsentLocal
-   SelAbsentCD
-   SelAbsentNetwork
-   SelLocalAbsent
-   SelLocalLocal
-   SelLocalCD
-   SelLocalNetwork
-   SelCDAbsent
-   SelNetworkAbsent
-   SelCDLocal
-   SelNetworkLocal
-   SelCDCD
-   SelNetworkNetwork

Per la formattazione delle dimensioni di un file vengono usate le quattro stringhe localizzate seguenti:

-   Byte
-   KB
-   MB
-   GB

 

 
