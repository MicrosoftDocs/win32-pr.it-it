---
description: Un controllo DirectoryList visualizza una parte del percorso attualmente visualizzata nel controllo PathEdit. Il controllo DirectoryList visualizza le cartelle sotto la directory attualmente visualizzata dal controllo DirectoryCombo.
ms.assetid: 05e70381-28c0-4568-808e-ff2dee8ff790
title: Controllo DirectoryList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce0cf409f4ca7335bd032f1fc63831db88ace14424ef7a73cd3853c9ff3e2de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086191"
---
# <a name="directorylist-control"></a>Controllo DirectoryList

Un controllo DirectoryList visualizza una parte del percorso attualmente visualizzata nel [controllo PathEdit](pathedit-control.md). Il controllo DirectoryList visualizza le cartelle sotto la directory attualmente visualizzata dal [controllo DirectoryCombo](directorycombo-control.md).

I controlli PathEdit, DirectoryCombo e DirectoryList sono associati alla stessa proprietà con valori stringa. Questa proprietà è il percorso selezionato dall'utente. Immettere il nome della proprietà nella colonna Proprietà della [tabella Control](control-table.md). Questa proprietà deve avere un valore iniziale contenente almeno un volume e un sottolivello. Specificare il valore iniziale per la proprietà nella colonna Valore della [tabella Proprietà](property-table.md).

Questo controllo deve essere usato in una [finestra di dialogo sfoglia](browse-dialog.md) insieme al controllo [PathEdit](pathedit-control.md) e DirectoryList.

Il controllo DirectoryList pubblica gli eventi ControlEvents seguenti.



| ControlEvent                                            | Descrizione                                                       |
|---------------------------------------------------------|-------------------------------------------------------------------|
| [DirectoryListNew](directorylistnew-controlevent.md)   | Crea una nuova cartella e seleziona il campo del nome per la modifica.      |
| [IgnoreChange](ignorechange-controlevent.md)           | Evidenzia, ma non apre, una cartella nella directory corrente. |
| [DirectoryListUp](directorylistup-controlevent.md)     | Seleziona l'elemento padre della directory corrente.                      |
| [DirectoryListOpen](directorylistopen-controlevent.md) | Seleziona ed evidenzia una directory.                               |



 

Il contenuto del campo Text della [tabella Control non](control-table.md) viene mai visualizzato dal controllo DirectoryList. Questo campo specifica invece lo stile del testo che deve essere visualizzato dal controllo e contiene una descrizione del controllo utilizzato dalle utilità di revisione dello schermo. Per impostare il tipo di carattere e lo stile del carattere di una stringa di testo, antessare alla stringa di caratteri visualizzati { style} o \\ {&*style*}. Dove style è un identificatore elencato nella colonna TextStyle della [tabella TextStyle](textstyle-table.md). Se nessuna di queste proprietà è presente, ma la [**proprietà DefaultUIFont**](defaultuifont.md) è definita come stile di testo valido, verrà usato tale tipo di carattere. Le informazioni seguenti vengono lette dalle utilità di revisione dello schermo come descrizione del controllo. Vedere [Accessibilità](accessibility.md).

## <a name="control-attributes"></a>Attributi del controllo

Con questo controllo è possibile usare gli attributi seguenti. Per modificare il valore di un attributo usando un evento , sottoscrivere il controllo a un oggetto ControlEvent nella tabella [EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna Attribute . Immettere l'identificatore di ControlEvent nella colonna Event .



| Identificatore dell'attributo                                               | Bit esadecimale                  | Descrizione                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Nome di una proprietà indiretta associata al controllo. Se il bit dell'attributo indiretto è impostato, il controllo visualizza o modifica il valore della proprietà con questo nome. Se il bit dell'attributo indiretto è impostato, questo nome è anche il valore della proprietà elencata nella colonna Proprietà della [tabella Control](control-table.md).                        |
| [Position](position-control-attribute.md)                         |                                  | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella Control](control-table.md). Usare le [unità del programma](installer-units.md) di installazione per lunghezza e distanza.<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Nome della proprietà associata a questo controllo. Se il bit dell'attributo indiretto non è impostato, il controllo visualizza o modifica il valore della proprietà con questo nome. Questo attributo viene specificato nella colonna Proprietà della [tabella Control](control-table.md).                                                                                        |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valore corrente della proprietà visualizzata o modificata da questo controllo. Se il bit dell'attributo indiretto non è impostato, questo è il valore di PropertyName. Se il bit dell'attributo indiretto è impostato, questo è il valore di IndirectPropertyName. Se l'attributo viene modificato, il controllo riflette il nuovo valore.                                                                           |
| [Text](text-control-attribute.md)                                 |                                  | Per visualizzare il testo nelle utilità per la lettura dello schermo, immettere il testo nella colonna Testo della [tabella Controllo](control-table.md). Vedere [Accessibilità](accessibility.md).                                                                                                                                                                                                                 |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Controllo nascosto. Controllo visibile.<br/> Includere questo bit nella parola di bit della colonna Attributes nella tabella [Control](control-table.md)per rendere il controllo visibile o nascosto al momento della creazione.<br/> È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/>                                     |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Controllo in uno stato disabilitato. Controllo in uno stato abilitato.<br/> Includere questo bit nella parola di bit nella colonna Attributi del [controllo](control-table.md) per abilitare il controllo al momento della creazione.<br/> È anche possibile abilitare o disabilitare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/>                                   |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Visualizza lo stile di visualizzazione predefinito. Visualizza il controllo con un aspetto incassato, 3D.<br/> Includere questi bit nella parola di bit nella colonna Attributi della [tabella Control](control-table.md).<br/>                                                                                                                                                             |
| [Indiretto](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | Il controllo visualizza o modifica il valore della proprietà nella colonna Proprietà della [tabella Control](control-table.md). Il controllo visualizza o modifica il valore della proprietà con l'identificatore elencato nella colonna Proprietà della tabella Control.<br/> Determina se alla proprietà associata a questo controllo viene fatto riferimento indirettamente.<br/> |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | Il testo nel controllo viene visualizzato in ordine di lettura da sinistra a destra. Il testo nel controllo viene visualizzato in ordine di lettura da destra a sinistra.<br/>                                                                                                                                                                                                                              |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | Il testo nel controllo è allineato a sinistra. Il testo nel controllo è allineato a destra.<br/>                                                                                                                                                                                                                                                                       |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | La barra di scorrimento si trova sul lato destro del controllo . La barra di scorrimento si trova sul lato sinistro del controllo .<br/>                                                                                                                                                                                                                                         |
| [Controllo BiDi](bidi-control-attribute.md)                         | 0x000000E0                       | Impostare questo valore per una combinazione degli [attributi RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md) [e LeftScroll.](leftscroll-control-attribute.md)                                                                                                                                                                          |



 

## <a name="remarks"></a>Commenti

Questo controllo può essere creato dalla classe LISTVIEW WC \_ usando la [**funzione CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Include gli stili **LVS \_ LIST,** **LVS \_ EDITLABELS,** **WS \_ VSCROLL,** **LVS \_ SHAREIMAGELISTS,** **LVS \_ AUTOARRANGE,** **LVS \_ SINGLESEL,** **WS \_ BORDER,** **LVS \_ SORTASCENDING,** **WS \_ CHILD,** **WS \_ GROUP** e **WS \_ TABSTOP.**

Questo controllo consente all'utente di selezionare una sottocartella della selezione corrente. Con pulsanti aggiuntivi consente anche all'utente di selezionare una nuova cartella nella selezione corrente o di un livello superiore nel percorso. Se l'utente  sceglie il pulsante Crea nuova cartella in una cartella in cui esiste già una nuova cartella, non viene creata una seconda nuova cartella e il nome della nuova cartella esistente viene selezionato per la modifica.

 

