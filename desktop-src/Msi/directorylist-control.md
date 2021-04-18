---
description: Un controllo di elenco di directory Visualizza una parte del percorso attualmente visualizzato nel controllo PathEdit. Il controllo Directory Visualizza le cartelle sotto la directory attualmente visualizzata dal controllo DirectoryCombo.
ms.assetid: 05e70381-28c0-4568-808e-ff2dee8ff790
title: Controllo Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6a1e48a25ae057c836c7b815dae18e7dcf5c3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314275"
---
# <a name="directorylist-control"></a>Controllo Directory

Un controllo di elenco di directory Visualizza una parte del percorso attualmente visualizzato nel [controllo PathEdit](pathedit-control.md). Il controllo Directory Visualizza le cartelle sotto la directory attualmente visualizzata dal [controllo DirectoryCombo](directorycombo-control.md).

I controlli PathEdit, DirectoryCombo e directory sono associati alla stessa proprietà con valori di stringa. Tale proprietà è il percorso selezionato dall'utente. Immettere il nome della proprietà nella colonna proprietà della tabella dei [controlli](control-table.md). Questa proprietà deve avere un valore iniziale contenente almeno un volume e un sottolivello. Specificare il valore iniziale per la proprietà nella colonna valore della tabella delle [Proprietà](property-table.md).

Questo controllo è destinato a essere utilizzato in una [finestra di dialogo di esplorazione](browse-dialog.md) insieme al controllo [PathEdit](pathedit-control.md) e directory.

Il controllo directory pubblica i ControlEvents seguenti.



| ControlEvent                                            | Descrizione                                                       |
|---------------------------------------------------------|-------------------------------------------------------------------|
| [DirectoryListNew](directorylistnew-controlevent.md)   | Crea una nuova cartella e seleziona il campo nome per la modifica.      |
| [IgnoreChange](ignorechange-controlevent.md)           | Evidenzia, ma non apre, una cartella nella directory corrente. |
| [DirectoryListUp](directorylistup-controlevent.md)     | Seleziona l'elemento padre della directory corrente.                      |
| [DirectoryListOpen](directorylistopen-controlevent.md) | Seleziona ed evidenzia una directory.                               |



 

Il contenuto del campo di testo della [tabella dei controlli](control-table.md) non viene mai visualizzato dal controllo Directory. Questo campo specifica invece lo stile di testo che deve essere visualizzato dal controllo e contiene una descrizione del controllo usato dalle utilità di revisione dello schermo. Per impostare il tipo di carattere e lo stile del carattere di una stringa di testo, anteporre alla stringa dei caratteri visualizzati lo stile { \\ Style} o {&*Style*}. Dove Style è un identificatore elencato nella colonna TextStyle della [tabella TextStyle](textstyle-table.md). Se nessuna di queste è presente, ma la proprietà [**DefaultUIFont**](defaultuifont.md) è definita come uno stile di testo valido, verrà usato tale tipo di carattere. Le informazioni riportate di seguito vengono lette dalle utilità di revisione dello schermo come descrizione del controllo. Vedere [accessibilità](accessibility.md).

## <a name="control-attributes"></a>Attributi del controllo

Con questo controllo è possibile usare gli attributi seguenti. Per modificare il valore di un attributo utilizzando un evento, sottoscrivere il controllo in un ControlEvent nella [tabella EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna attributo. Immettere l'identificatore del ControlEvent nella colonna evento.



| Identificatore di attributo                                               | Bit esadecimale                  | Descrizione                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Si tratta del nome di una proprietà indiretta associata al controllo. Se viene impostato il bit di attributo indiretto, il controllo Visualizza o modifica il valore della proprietà con questo nome. Se viene impostato il bit di attributo indiretto, questo nome è anche il valore della proprietà elencata nella colonna proprietà della [tabella dei controlli](control-table.md).                        |
| [Position](position-control-attribute.md)                         |                                  | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate del controllo dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella del controllo](control-table.md). Usare le [unità del programma di installazione](installer-units.md) per lunghezza e distanza.<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Si tratta del nome della proprietà associata a questo controllo. Se il bit di attributo indiretto non è impostato, il controllo Visualizza o modifica il valore della proprietà con questo nome. Questo attributo viene specificato nella colonna proprietà della tabella dei [controlli](control-table.md).                                                                                        |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valore corrente della proprietà visualizzata o modificata da questo controllo. Se il bit di attributo indiretto non è impostato, questo è il valore di PropertyName. Se viene impostato il bit di attributo indiretto, questo è il valore di IndirectPropertyName. Se l'attributo viene modificato, il controllo riflette il nuovo valore.                                                                           |
| [Text](text-control-attribute.md)                                 |                                  | Per visualizzare il testo nelle utilità per la lettura dello schermo, immettere il testo nella colonna di testo della [tabella dei controlli](control-table.md). Vedere [accessibilità](accessibility.md).                                                                                                                                                                                                                 |
| [Visible](visible-control-attribute.md)                           | 0x00000001 0x00000000<br/> | Controllo nascosto. Controllo visibile.<br/> Includere questo bit nella parola bit della colonna attributi nella [tabella dei controlli](control-table.md). per rendere il controllo visibile o nascosto alla sua creazione.<br/> È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/>                                     |
| [Enabled](enabled-control-attribute.md)                           | 0x00000002 0x00000000<br/> | Controllo in uno stato disabilitato. Controllo in uno stato abilitato.<br/> Includere questo bit nella parola bit nella colonna attributi del [controllo](control-table.md) per abilitare il controllo alla creazione.<br/> È anche possibile abilitare o disabilitare un controllo tramite la [tabella ControlCondition](controlcondition-table.md).<br/>                                   |
| [Sunken](sunken-control-attribute.md)                             | 0x00000004 0x00000000<br/> | Visualizza lo stile di visualizzazione predefinito. Visualizza il controllo con un aspetto incassato, 3D.<br/> Includere questi bit nella parola bit nella colonna attributi della [tabella dei controlli](control-table.md).<br/>                                                                                                                                                             |
| [Indiretto](indirect-control-attribute.md)                         | 0x00000008 0x00000000<br/> | Il controllo Visualizza o modifica il valore della proprietà nella colonna proprietà della [tabella dei controlli](control-table.md). Il controllo Visualizza o modifica il valore della proprietà con l'identificatore elencato nella colonna proprietà della tabella dei controlli.<br/> Determina se viene fatto riferimento indirettamente alla proprietà associata a questo controllo.<br/> |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000020 0x00000000<br/> | Il testo nel controllo viene visualizzato nell'ordine di lettura da sinistra a destra. Il testo nel controllo viene visualizzato in ordine di lettura da destra a sinistra.<br/>                                                                                                                                                                                                                              |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000040 0x00000000<br/> | Il testo nel controllo è allineato a sinistra. Il testo nel controllo è allineato a destra.<br/>                                                                                                                                                                                                                                                                       |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000080 0x00000000<br/> | La barra di scorrimento si trova sul lato destro del controllo. La barra di scorrimento si trova sul lato sinistro del controllo.<br/>                                                                                                                                                                                                                                         |
| [BiDi (controllo)](bidi-control-attribute.md)                         | 0x000000E0                       | Impostare questo valore per una combinazione degli attributi [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)e [LeftScroll](leftscroll-control-attribute.md) .                                                                                                                                                                          |



 

## <a name="remarks"></a>Commenti

Questo controllo può essere creato dalla \_ classe ListView di WC usando la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Include gli stili **LVS \_ List**, **LVS \_ EDITLABELS**, **WS \_ VSCROLL**, **LVS \_ SHAREIMAGELISTS**, **LVS \_ AutoArrange**, **LVS \_ SINGLESEL**, **WS \_ Border**, **LVS \_ SORTASCENDING**, **WS \_ child**, **WS \_ Group** e **WS \_ TABSTOP** .

Questo controllo consente all'utente di selezionare una sottocartella della selezione corrente. Con pulsanti aggiuntivi consente inoltre all'utente di selezionare una nuova cartella nella selezione corrente o di eseguire un passaggio verso l'alto di un livello nel percorso. Se l'utente sceglie il pulsante **Crea nuova cartella** in una cartella in cui è già presente una nuova cartella, non viene creata una seconda nuova cartella e il nome della nuova cartella esistente è selezionato per la modifica.

 

