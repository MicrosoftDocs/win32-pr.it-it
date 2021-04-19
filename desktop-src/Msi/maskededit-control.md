---
description: Il controllo MaskedEdit è un controllo di modifica campo che contiene una maschera nel campo di testo del controllo. È possibile associare il controllo a una proprietà di valore stringa immettendo il nome della proprietà nella colonna proprietà della tabella dei controlli.
ms.assetid: 8cc14683-3dbb-404f-87af-09a5f5b90b19
title: Controllo MaskedEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7568df9969ebabab6311e519d0a5a625feb8dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319967"
---
# <a name="maskededit-control"></a>Controllo MaskedEdit

Il controllo MaskedEdit è un controllo di modifica campo che contiene una maschera nel campo di testo del controllo. È possibile associare il controllo a una proprietà di valore stringa immettendo il nome della proprietà nella colonna proprietà della [tabella dei controlli](control-table.md).

È possibile utilizzare il controllo MaskedEdit per creare un modello per l'immissione di informazioni da parte dell'utente, ad esempio un numero di telefono o un codice ID prodotto. Ad esempio, la proprietà [**codice PIDKEY**](pidkey.md) può essere immessa dall'utente tramite un controllo MaskedEdit specificato impostando la proprietà [**PIDTemplate**](pidtemplate.md) su una stringa simile alla seguente:

12345<\#\#\# -%%%%%%%>@@@@@

La stringa definisce il modello di mascheramento per la voce della proprietà [**codice PIDKEY**](pidkey.md) da parte dell'utente. Il segmento visibile della stringa è racchiuso tra due caratteri di parentesi quadre (<>).

Nella tabella seguente è stata identificata la sintassi della maschera.



| Carattere | Significato                                                                                                                                                                                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <      | Estremità sinistra del segmento visibile del modello. Questo carattere e tutti gli elementi a sinistra sono nascosti nell'interfaccia utente. Nel modello non deve essere presente più di un'istanza di questo carattere.                                                                               |
| >      | Estremità destra del segmento visibile del modello. Questo carattere e tutto il suo diritto sono nascosti nell'interfaccia utente. Questo carattere viene sostituito da un trattino durante la convalida. Se è presente un segmento visibile che inizia con <, deve terminare con un > corrispondente. |
| \#        | Questo carattere può essere una cifra (numero).                                                                                                                                                                                                                                                    |
| %         | Questo carattere può essere una cifra alternativa (numero) che consente alla maschera di controllare il modo in cui un'azione personalizzata differenzia i campi.                                                                                                                                                          |
| @         | Questo carattere può essere una cifra casuale (numero). Questo carattere non deve essere visualizzato nella parte visibile del modello.                                                                                                                                                                       |
| &         | Questo carattere può essere qualsiasi carattere.                                                                                                                                                                                                                                                        |
| ^         | Questo carattere può essere un carattere alternativo che consente alla maschera di controllare il modo in cui un'azione personalizzata differenzia i campi.                                                                                                                                                                |
| ?         | Questo carattere può essere un carattere alternativo che consente alla maschera di controllare il modo in cui un'azione personalizzata differenzia i campi.                                                                                                                                                                |
| \`        | I contrassegni accentati gravi \` (valore ASCII 96) possono rappresentare un carattere alternativo che consente alla maschera di controllare il modo in cui un'azione personalizzata differenzia i campi.                                                                                                                                 |
| \_        | Questo carattere è un carattere di sottolineatura letterale.                                                                                                                                                                                                                                           |
| =         | Questo carattere è il carattere di terminazione del campo. Deve seguire un valore \# ,%, ^ o \` . In questo modo viene creata una posizione di input dello stesso tipo delle posizioni precedenti e il campo viene terminato con un separatore '-'.                                                                                 |



 

Qualsiasi altro carattere viene considerato come una costante letterale.

Per i caratteri che possono essere modificati, il controllo crea finestre di modifica separate con una finestra per ogni blocco di caratteri contigui dello stesso tipo.

## <a name="control-attributes"></a>Attributi del controllo

Per modificare il valore di un attributo che utilizza un evento, sottoscrivere il controllo a un evento del controllo nella [tabella EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna attributo. Immettere l'identificatore dell'evento di controllo nella colonna evento. Con il controllo MaskedEdit è possibile usare gli attributi seguenti.



| Attributo                                                          | Bit esadecimale                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Si tratta del nome di una proprietà indiretta associata al controllo. Se viene impostato il bit di attributo indiretto, il controllo Visualizza o modifica il valore della proprietà con questo nome. Se viene impostato il bit di attributo indiretto, questo nome è anche il valore della proprietà elencata nella colonna proprietà della tabella dei [controlli](control-table.md).                                                                                                                                   |
| [Position](position-control-attribute.md)                         |                                  | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate del controllo dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della tabella del [controllo](control-table.md). Usare le [unità del programma di installazione](installer-units.md) per lunghezza e distanza.<br/>                                                                                                                                                                                                            |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Si tratta del nome della proprietà associata a questo controllo. Se il bit di attributo indiretto non è impostato, il controllo Visualizza o modifica il valore della proprietà con questo nome. Questo attributo viene specificato nella colonna proprietà della tabella dei [controlli](control-table.md).                                                                                                                                                                                                           |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valore corrente della proprietà visualizzata o modificata da questo controllo. Se il bit di attributo indiretto non è impostato, questo è il valore di PropertyName. Se viene impostato il bit di attributo indiretto, questo è il valore di IndirectPropertyName. Se l'attributo viene modificato, il controllo riflette il nuovo valore.                                                                                                                                                                                                |
| [Text](text-control-attribute.md)                                 |                                  | Per impostare il tipo di carattere e lo stile del carattere di una stringa di testo, anteporre alla stringa dei caratteri visualizzati lo stile { \\ Style} o {&Style}. Dove Style è un identificatore elencato nella colonna Style della [tabella TextStyle](textstyle-table.md). Se nessuna di queste è presente, ma la proprietà [**DefaultUIFont**](defaultuifont.md) è definita come uno stile di testo valido, viene usato il tipo di carattere. La stringa che specifica il modello di maschera segue questo prefisso e usa la sintassi descritta in precedenza in questo argomento. |
| [Visible](visible-control-attribute.md)                           | 0x00000001 0x00000000<br/> | Controllo nascosto. Controllo visibile.<br/> Includere questo bit nella parola bit della colonna attributi nella [tabella dei controlli](control-table.md) per rendere il controllo visibile o nascosto quando viene creato.<br/> È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                 |
| [Enabled](enabled-control-attribute.md)                           | 0x00000002 0x00000000<br/> | Controllo in uno stato disabilitato. Controllo in uno stato abilitato.<br/> Includere questo bit nella parola bit nella colonna attributi della [tabella dei controlli](control-table.md) per abilitare il controllo al momento della creazione.<br/> È anche possibile abilitare o disabilitare un controllo tramite la [tabella ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                          |
| [Sunken](sunken-control-attribute.md)                             | 0x00000004 0x00000000<br/> | Visualizza lo stile di visualizzazione predefinito. Visualizza il controllo con un aspetto incassato, 3D.<br/> Includere questi bit nella parola bit nella colonna attributi della [tabella dei controlli](control-table.md).<br/>                                                                                                                                                                                                                                                                                          |
| [Indiretto](indirect-control-attribute.md)                         | 0x00000008 0x00000000<br/> | Il controllo Visualizza o modifica il valore della proprietà nella colonna proprietà della [tabella dei controlli](control-table.md). Il controllo Visualizza o modifica il valore della proprietà con l'identificatore elencato nella colonna proprietà della [tabella dei controlli](control-table.md).<br/> Determina se viene fatto riferimento indirettamente alla proprietà associata a questo controllo.<br/>                                                                                                 |



 

## <a name="remarks"></a>Commenti

Il controllo MaskedEdit crea una finestra padre della classe **Button** con gli stili **BS \_ OWNERDRAW** e **WS \_ ex \_ CONTROLPARENT** . Crea diverse finestre figlio in questa finestra.

-   Per le parti di testo costanti, vengono create finestre statiche con gli stili **SS \_ Left** e **WS \_ child** .
-   Per i campi modificabili, viene creata una finestra di modifica con gli stili **WS \_ child**, **WS \_ Border** e **WS \_ TABSTOP** .
-   Per i campi numerici, la finestra ha anche lo stile del **\_ numero es** .

I campi numero alternativo,% e caratteri alfanumerici alternativi, ^,? e \` consentono azioni personalizzate per distinguere i campi in modo che possano essere controllati dalla maschera. ad esempio, ^ può essere usato per i campi che devono essere maiuscoli.

 

 




