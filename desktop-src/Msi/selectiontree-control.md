---
description: Questo controllo consente a un utente di modificare lo stato di selezione delle funzionalità elencate nella tabella Funzionalità.
ms.assetid: 0daf5b44-ba07-47f1-95d9-28c59f7cf985
title: Controllo SelectionTree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 894a7d90829172c29a6f1df1ffc4139cc0bf6c540bd49193c3cc2f3a396891ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040351"
---
# <a name="selectiontree-control"></a>Controllo SelectionTree

Questo controllo consente a un utente di modificare lo stato di selezione delle funzionalità elencate nella [tabella Funzionalità](feature-table.md). Il controllo è associato a una proprietà con valori stringa che l'utente può impostare tramite una [finestra di dialogo Sfoglia](browse-dialog.md). È possibile associare il controllo a una proprietà immettendo il nome della proprietà nella colonna Proprietà della [tabella Control](control-table.md).

Il controllo SelectionTree pubblica automaticamente gli eventi [di](control-events.md) controllo seguenti Windows xp o sistemi operativi precedenti. Il controllo SelectionTree pubblica questi eventi quando l'elemento selezionato viene modificato da un nodo a un altro. Se l'albero di selezione non ha nodi, il controllo pubblica questi eventi e cancella il contenuto dei controlli che sottoscriveno l'evento. Questi ControlEvent non devono essere elencati nella [tabella ControlEvent](controlevent-table.md).



| Evento di controllo                                                 | Descrizione                                                                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [SelectionAction](selectionaction-controlevent.md)           | Pubblica una stringa dalla tabella [UIText che descrive](uitext-table.md) l'elemento evidenziato.      |
| [SelectionBrowse](selectionbrowse-controlevent.md)           | Genera una finestra di dialogo Sfoglia utilizzata per modificare il percorso dell'elemento evidenziato.                     |
| [SelectionDescription](selectiondescription-controlevent.md) | Pubblica una stringa dalla tabella [Funzionalità che descrive](feature-table.md) l'elemento evidenziato.    |
| [SelectionNoItems](selectionnoitems-controlevent.md)         | Elimina il testo descrittivo o disabilita i pulsanti di un elemento obsoleto.                          |
| [SelectionPath](selectionpath-controlevent.md)               | Pubblica il percorso per l'elemento evidenziato.                                                       |
| [SelectionPathOn](selectionpathon-controlevent.md)           | Pubblica se è presente o meno un percorso di selezione associato alla funzionalità attualmente selezionata. |
| [SelectionSize](selectionsize-controlevent.md)               | Pubblica le dimensioni dell'elemento evidenziato.                                                        |



 

A partire da Windows Server 2003, i controlli SelectionTree pubblicano tutti gli eventi nella tabella precedente e pubblicano anche [un oggetto DoAction ControlEvent](doaction-controlevent.md) o [SetProperty ControlEvent](setproperty-controlevent.md). È necessario aggiungere record alla tabella [ControlEvent per](controlevent-table.md) pubblicare DoAction o SetProperty ControlEvents.



| Evento di controllo                               | Descrizione                                        |
|---------------------------------------------|----------------------------------------------------|
| [DoAction](doaction-controlevent.md)       | Notifica al programma di installazione di eseguire un'azione personalizzata. |
| [SetProperty](setproperty-controlevent.md) | Imposta una proprietà su un nuovo valore.                    |



 

A partire da Windows Installer versione 3.0, i controlli [](custom-actions.md) SelectionTree pubblicano un evento che esegue azioni personalizzate elencate nella [tabella ControlEvent](controlevent-table.md). Il controllo SelectionTree pubblica questo evento ogni volta che la selezione della funzionalità cambia nel controllo o quando viene scelto un diverso stato di selezione per la funzionalità corrente. Le azioni personalizzate vengono eseguite ogni volta che l'evento viene pubblicato. Il controllo SelectionTree invia informazioni all'azione personalizzata impostando i valori delle proprietà seguenti. Tutte queste proprietà vengono cancellate quando il controllo SelectionTree viene chiuso.

**Windows Installer 2.0:** Non supportato. Il controllo SelectionTree non pubblica l'evento e non imposta le proprietà seguenti.



| Proprietà                                | Descrizione                                                                                                                                                      |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MsiSelectionTreeSelectedFeature         | Nome della funzionalità selezionata nel campo Funzionalità della [tabella Funzionalità](feature-table.md).                                                                      |
| MsiSelectionTreeSelectedAction          | Stato dell'azione di installazione della funzionalità selezionata. Il valore può essere INSTALLSTATE \_ ABSENT, INSTALLSTATE \_ LOCAL, INSTALLSTATE \_ SOURCE o INSTALLSTATE \_ ADVERTISED. |
| MsiSelectonTreeChildrenCount            | Numero di nodi figlio diretti.                                                                                                                                    |
| MsiSelectionTreeInstallingChildrenCount | Numero di nodi figlio diretti che sono INSTALLSTATE \_ LOCAL, INSTALLSTATE \_ SOURCE o INSTALLSTATE \_ ADVERTISED.                                                    |
| MsiSelectionTreeSelectedCost            | Costo dell'installazione della funzionalità selezionata in unità di 512 byte.                                                                                                   |
| MsiSelectionTreeChildrenCost            | Costo dell'installazione di tutte le funzionalità figlio in unità di 512 byte.                                                                                              |
| MsiSelectionTreeSelectedPath            | Percorso in cui viene installata la funzionalità selezionata. Definito solo se la funzionalità viene installata come INSTALLSTATE \_ LOCAL.                                       |



 

> [!Note]
>
> Il contenuto del campo Text della [tabella Control non](control-table.md) viene mai visualizzato dal controllo SelectionTree. Questo campo specifica invece lo stile del testo che deve essere visualizzato dal controllo e contiene una descrizione del controllo utilizzato dalle utilità di revisione dello schermo. Per impostare il tipo di carattere e lo stile del carattere di una stringa di testo, antessare alla stringa di caratteri visualizzati { style} o \\ {&*style*}. Dove style è un identificatore elencato nella colonna TextStyle della [tabella TextStyle](textstyle-table.md). Se nessuna di queste proprietà è presente, ma la [**proprietà DefaultUIFont**](defaultuifont.md) è definita come stile di testo valido, viene usato tale tipo di carattere. Le informazioni seguenti vengono lette dalle utilità di revisione dello schermo come descrizione del controllo. Vedere [Accessibilità](accessibility.md).

 

## <a name="control-attributes"></a>Attributi del controllo

Con questo controllo è possibile usare gli attributi seguenti. Per modificare il valore di un attributo usando un evento , sottoscrivere il controllo a un oggetto ControlEvent nella tabella [EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna Attribute . Immettere l'identificatore di ControlEvent nella colonna Event .



| Identificatore dell'attributo                                               | Bit esadecimale                  | Descrizione                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Nome di una proprietà indiretta associata al controllo. Se il bit dell'attributo indiretto è impostato, il controllo visualizza o modifica il valore della proprietà con questo nome. Se il bit dell'attributo indiretto è impostato, questo nome è anche il valore della proprietà elencata nella colonna Proprietà della [tabella Control](control-table.md).                                    |
| [Position](position-control-attribute.md)                         |                                  | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella Control](control-table.md). Usare le [unità del programma](installer-units.md) di installazione per lunghezza e distanza.<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Nome della proprietà associata a questo controllo. Se il bit dell'attributo indiretto non è impostato, il controllo visualizza o modifica il valore della proprietà con questo nome. Questo attributo viene specificato nella colonna Proprietà della [tabella Control](control-table.md).                                                                                                    |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valore corrente della proprietà visualizzata o modificata da questo controllo. Se il bit dell'attributo indiretto non è impostato, questo è il valore di PropertyName. Se il bit dell'attributo indiretto è impostato, questo è il valore di IndirectPropertyName. Se l'attributo viene modificato, il controllo riflette il nuovo valore.                                                                           |
| [Text](text-control-attribute.md)                                 |                                  | Visualizza il testo nelle utilità per la lettura dello schermo in base al testo immesso nella colonna Text della [tabella Control](control-table.md). Vedere [Accessibilità](accessibility.md).                                                                                                                                                                                                          |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Controllo nascosto. Controllo visibile.<br/> Includere questo bit nella parola di bit della colonna Attributes nella tabella [Control](control-table.md) per rendere il controllo visibile o nascosto al momento della creazione.<br/> È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/>                                     |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Controllo in uno stato disabilitato. Controllo in uno stato abilitato.<br/> Includere questo bit nella parola di bit nella colonna Attributi del [controllo per](control-table.md) abilitare il controllo durante la creazione.<br/> È anche possibile abilitare o disabilitare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/>                                   |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Visualizza lo stile di visualizzazione predefinito. Visualizza il controllo con un aspetto 3D incassato.<br/> Includere questi bit nella parola di bit nella colonna Attributi della [tabella Control](control-table.md).<br/>                                                                                                                                                             |
| [Indiretto](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | Il controllo visualizza o modifica il valore della proprietà nella colonna Proprietà della [tabella Control](control-table.md). Il controllo visualizza o modifica il valore della proprietà con l'identificatore elencato nella colonna Proprietà della tabella Control.<br/> Determina se alla proprietà associata a questo controllo viene fatto riferimento indirettamente.<br/> |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | Il testo nel controllo viene visualizzato in ordine di lettura da sinistra a destra. Il testo nel controllo viene visualizzato in ordine di lettura da destra a sinistra.<br/>                                                                                                                                                                                                                              |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | Il testo nel controllo è allineato a sinistra. Il testo nel controllo è allineato a destra.<br/>                                                                                                                                                                                                                                                                       |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | La barra di scorrimento si trova sul lato destro del controllo . La barra di scorrimento si trova sul lato sinistro del controllo .<br/>                                                                                                                                                                                                                                         |
| [Bidi](bidi-control-attribute.md)                                 | 0x000000E0                       | Impostare questo valore per una combinazione degli [attributi RTLRO,](rtlro-control-attribute.md) [RightAligned](rightaligned-control-attribute.md) [e LeftScroll.](leftscroll-control-attribute.md)                                                                                                                                                                          |



 

## <a name="remarks"></a>Commenti

Questo controllo può essere creato dalla classe TREEVIEW WC \_ usando la [**funzione CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Ha GLI STILI **WS \_ BORDER,** **TVS \_ HASLINES,** **TVS \_ HASBUTTONS,** **TVS \_ LINESATROOT,** **TVS \_ DISABLEDRAGDROP,** **TVS \_ SHOWSELALWAYS,** **WS \_ CHILD,** **WS \_ TABSTOP** e **WS \_ GROUP.**

L'albero di selezione viene popolato solo se sono state chiamate [l'azione CostInitialize](costinitialize-action.md) [e l'azione CostFinalize.](costfinalize-action.md)

La stringa seguente nella [tabella UIText](uitext-table.md) è correlata a questo controllo.



| Termine                                                                                                         | Descrizione                                                    |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="AbsentPath"></span><span id="absentpath"></span><span id="ABSENTPATH"></span>AbsentPath<br/> | Percorso visualizzato per un elemento nello stato assente.<br/> |



 

Le sei stringhe seguenti vengono usate per visualizzare il numero di elementi figlio selezionati e le dimensioni associate all'elemento evidenziato:

-   SelChildCostPos
-   SelChildCostNeg
-   SelParentCostPosPos
-   SelParentCostPosNeg
-   SelParentCostNegPos
-   SelParentCostNegNeg

Le stringhe seguenti vengono usate per visualizzare le opzioni di selezione disponibili per un elemento in un menu popup:

-   MenuAbsent
-   MenuLocal
-   MenuCD
-   MenuNetwork
-   MenuAllLocal
-   MenuAllCD
-   MenuAllNetwork

Le stringhe seguenti vengono usate per spiegare la selezione corrente in [SelectionDescription](selectiondescription-controlevent.md) ControlEvent.

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

Le quattro stringhe localizzate seguenti vengono usate per formattare le dimensioni di un file:

-   Byte
-   KB
-   MB
-   GB

 

 
