---
description: Il controllo MaskedEdit è un controllo campo di modifica che contiene una maschera nel campo di testo del controllo. È possibile associare il controllo a una proprietà di valore stringa immettendo il nome della proprietà nella colonna Proprietà della tabella di controllo.
ms.assetid: 8cc14683-3dbb-404f-87af-09a5f5b90b19
title: Controllo MaskedEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30a6490cf2eb05d001d00a1cd8b5b3d33520ea735ebe0d05f064d4053847b691
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805106"
---
# <a name="maskededit-control"></a>Controllo MaskedEdit

Il controllo MaskedEdit è un controllo campo di modifica che contiene una maschera nel campo di testo del controllo. È possibile associare il controllo a una proprietà di valore stringa immettendo il nome della proprietà nella colonna Proprietà della [tabella di controllo](control-table.md).

È possibile usare il controllo MaskedEdit per creare un modello per l'immissione da parte dell'utente di informazioni quali un numero di telefono o un codice ID prodotto. Ad esempio, la [**proprietà PIDKEY**](pidkey.md) può essere immessa dall'utente tramite un controllo MaskedEdit specificato impostando la [**proprietà PIDTemplate**](pidtemplate.md) su una stringa simile alla seguente:

12345<\#\#\# -%%%%%%%>@@@@@

La stringa definisce il modello di maschera per l'immissione della [**proprietà PIDKEY**](pidkey.md) da parte dell'utente. Il segmento visibile della stringa è racchiuso da una coppia di caratteri di parentesi quadre (<>).

Nella tabella seguente è stata identificata la sintassi della maschera.



| Carattere | Significato                                                                                                                                                                                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <      | Estremità sinistra del segmento visibile del modello. Questo carattere e tutti gli elementi a sinistra sono nascosti nell'interfaccia utente. Non deve essere presente più di un'istanza di questo carattere nel modello.                                                                               |
| >      | Estremità destra del segmento visibile del modello. Questo carattere e tutti gli elementi a destra sono nascosti nell'interfaccia utente. Questo carattere viene sostituito da un trattino durante la convalida. Se un segmento visibile inizia con <, deve essere terminato con un >. |
| \#        | Questo carattere può essere una cifra (numero).                                                                                                                                                                                                                                                    |
| %         | Questo carattere può essere una cifra alternativa (numerale) che consente alla maschera di controllare il modo in cui un'azione personalizzata differenzia i campi.                                                                                                                                                          |
| @         | Questo carattere può essere una cifra casuale (numero). Questo carattere non deve essere visualizzato nella parte visibile del modello.                                                                                                                                                                       |
| &         | Questo carattere può essere qualsiasi carattere.                                                                                                                                                                                                                                                        |
| ^         | Questo carattere può essere un carattere alternativo che consente alla maschera di controllare il modo in cui un'azione personalizzata differenzia i campi.                                                                                                                                                                |
| ?         | Questo carattere può essere un carattere alternativo che consente alla maschera di controllare il modo in cui un'azione personalizzata differenzia i campi.                                                                                                                                                                |
| \`        | I segni di accento grave (valore ASCII 96) possono rappresentare un carattere alternativo che consente alla maschera di controllare il modo in cui \` un'azione personalizzata differenzia i campi.                                                                                                                                 |
| \_        | Questo carattere è un carattere di sottolineatura letterale.                                                                                                                                                                                                                                           |
| =         | Questo carattere è il carattere di terminazione del campo. Deve seguire , \# %, ^, o \` . Verrà creata un'altra posizione di input dello stesso tipo delle posizioni precedenti e il campo verrà terminato con un separatore '-'.                                                                                 |



 

Qualsiasi altro carattere viene considerato come una costante letterale.

Per i caratteri che possono essere modificati, il controllo crea finestre di modifica separate con una finestra per ogni blocco di caratteri contigui dello stesso tipo.

## <a name="control-attributes"></a>Attributi del controllo

Per modificare il valore di un attributo che usa un evento, sottoscrivere il controllo a un evento Control nella [tabella EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna Attribute. Immettere l'identificatore dell'evento Control nella colonna Event (Evento). È possibile usare gli attributi seguenti con il controllo MaskedEdit.



| Attributo                                                          | Bit esadecimale                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Si tratta del nome di una proprietà indiretta associata al controllo . Se il bit dell'attributo indiretto è impostato, il controllo visualizza o modifica il valore della proprietà con questo nome. Se il bit dell'attributo indiretto è impostato, questo nome è anche il valore della proprietà elencata nella colonna Proprietà della [tabella di controllo](control-table.md).                                                                                                                                   |
| [Position](position-control-attribute.md)                         |                                  | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate del controllo nell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella di controllo](control-table.md). Usare [unità di installazione](installer-units.md) per lunghezza e distanza.<br/>                                                                                                                                                                                                            |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Nome della proprietà associata a questo controllo. Se il bit dell'attributo indiretto non è impostato, il controllo visualizza o modifica il valore della proprietà con questo nome. Questo attributo viene specificato nella colonna Proprietà della tabella [di controllo](control-table.md).                                                                                                                                                                                                           |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valore corrente della proprietà visualizzata o modificata da questo controllo. Se il bit dell'attributo indiretto non è impostato, questo è il valore di PropertyName. Se il bit dell'attributo indiretto è impostato, questo è il valore di IndirectPropertyName. Se l'attributo viene modificato, il controllo riflette il nuovo valore.                                                                                                                                                                                                |
| [Text](text-control-attribute.md)                                 |                                  | Per impostare il tipo di carattere e lo stile del carattere di una stringa di testo, antessare alla stringa di caratteri visualizzati { style} o \\ {&style}. Dove style è un identificatore elencato nella colonna Style della [tabella TextStyle](textstyle-table.md). Se nessuna di queste proprietà è presente, ma la [**proprietà DefaultUIFont**](defaultuifont.md) è definita come stile di testo valido, viene usato tale tipo di carattere. La stringa che specifica il modello di maschera segue questo prefisso e usa la sintassi descritta in precedenza in questo argomento. |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Controllo nascosto. Controllo visibile.<br/> Includere questo bit nella parola di bit della colonna Attributi nella [tabella](control-table.md) di controllo per rendere il controllo visibile o nascosto al momento della creazione.<br/> È anche possibile nascondere o visualizzare un controllo usando [la tabella ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                 |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Controllo in uno stato disabilitato. Controllo in uno stato abilitato.<br/> Includere questo bit nella parola di bit nella colonna Attributi della tabella [di](control-table.md) controllo per abilitare il controllo al momento della creazione.<br/> È anche possibile abilitare o disabilitare un controllo usando [la tabella ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                          |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Visualizza lo stile di visualizzazione predefinito. Visualizza il controllo con un aspetto 3D incassato.<br/> Includere questi bit nella parola di bit nella colonna Attributi della [tabella di controllo](control-table.md).<br/>                                                                                                                                                                                                                                                                                          |
| [Indiretto](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | Il controllo visualizza o modifica il valore della proprietà nella colonna Proprietà della [tabella di controllo](control-table.md). Il controllo visualizza o modifica il valore della proprietà con l'identificatore elencato nella colonna Proprietà della [tabella di controllo](control-table.md).<br/> Determina se alla proprietà associata a questo controllo viene fatto riferimento indirettamente.<br/>                                                                                                 |



 

## <a name="remarks"></a>Commenti

Il controllo MaskedEdit crea una finestra padre della **classe BUTTON** con gli stili **BS \_ OWNERDRAW** e **WS EX \_ \_ CONTROLPARENT.** Crea diverse finestre figlio in questa finestra.

-   Per le parti di testo costanti, crea finestre STATICHE con gli stili **\_ SS LEFT** e **WS \_ CHILD.**
-   Per i campi modificabili, crea una finestra EDIT con gli stili **WS \_ CHILD,** **WS \_ BORDER** e **WS \_ TABSTOP.**
-   Per i campi numerici, la finestra ha anche lo **stile ES \_ NUMBER.**

La cifra alternativa % e i caratteri alfanumerici alternativi , ^, ?, e consentono alle azioni personalizzate di distinguere i campi in modo che possano essere controllati dalla maschera, ad esempio ^ può essere usato per i campi che devono essere in \` maiuscolo.

 

 




