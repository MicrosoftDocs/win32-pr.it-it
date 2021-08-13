---
description: La tabella Control definisce i controlli visualizzati in ogni finestra di dialogo.
ms.assetid: cbe7acd6-b916-45f3-b694-d2345c5a892a
title: Tabella dei controlli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e1832a2cb600e8d7a27b43bc28c94836396d74a50a90b44d0e5013bde973c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638533"
---
# <a name="control-table"></a>Tabella dei controlli

La tabella Control definisce i controlli visualizzati in ogni finestra di dialogo.

La tabella Control include le colonne seguenti.



| Colonna        | Tipo                               | Chiave | Nullable |
|---------------|------------------------------------|-----|----------|
| Finestra di dialogo\_      | [Identificatore](identifier.md)       | S   | N        |
| Control       | [Identificatore](identifier.md)       | S   | N        |
| Tipo          | [Identificatore](identifier.md)       | N   | N        |
| X             | [Integer](integer.md)             | N   | N        |
| S             | [Integer](integer.md)             | N   | N        |
| Larghezza         | [Integer](integer.md)             | N   | N        |
| Altezza        | [Integer](integer.md)             | N   | N        |
| Attributi    | [DoubleInteger](doubleinteger.md) | N   | S        |
| Proprietà      | [Identificatore](identifier.md)       | N   | S        |
| Testo          | [Formattato](formatted.md)         | N   | S        |
| Controllo \_ successivo | [Identificatore](identifier.md)       | N   | S        |
| Help          | [Text](text.md)                   | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogo\_
</dt> <dd>

Chiave esterna alla prima colonna della tabella [Dialog](dialog-table.md), il nome della finestra di dialogo.

</dd> <dt>

<span id="Control"></span><span id="control"></span><span id="CONTROL"></span>Controllo
</dt> <dd>

Nome del controllo. Questo nome deve essere univoco all'interno di una finestra di dialogo, ma può essere ripetuto in finestre di dialogo diverse. La colonna Control combinata con la colonna Dialog \_ forma la chiave primaria per questa tabella.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>digitare
</dt> <dd>

Tipo del controllo. Per un elenco dei tipi di controllo, vedere [Controlli](controls.md).

</dd> <dt>

<span id="X"></span><span id="x"></span>X
</dt> <dd>

Coordinata orizzontale dell'angolo superiore sinistro del limite rettangolare del controllo. Deve essere un numero non negativo. Vedere [Position Control Attribute](position-control-attribute.md).

</dd> <dt>

<span id="Y"></span><span id="y"></span>Y
</dt> <dd>

Coordinata verticale dell'angolo superiore sinistro del limite rettangolare del controllo. Deve essere un numero non negativo. Vedere [Position Control Attribute](position-control-attribute.md).

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Larghezza
</dt> <dd>

Larghezza del limite rettangolare del controllo. Deve essere un numero non negativo. Vedere [Position Control Attribute](position-control-attribute.md).

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Altezza
</dt> <dd>

Altezza del limite rettangolare del controllo. Deve essere un numero non negativo. Vedere [Position Control Attribute](position-control-attribute.md).

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

Parola a 32 bit che specifica i flag di bit da applicare a questo controllo. Deve essere un numero non negativo e i valori consentiti dipendono dal tipo di controllo. Per un elenco di tutti gli attributi del controllo e il valore da immettere in questo campo, vedere [Attributi di controllo.](control-attributes.md)

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà
</dt> <dd>

Nome di una proprietà definita da collegare a questo controllo. I valori dei pulsanti di opzione, delle caselle di riepilogo e delle caselle combinate sono collegati a un gruppo tramite il collegamento alla stessa proprietà. Questa colonna è obbligatoria per i controlli attivi.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Testo
</dt> <dd>

Stringa localizzabile utilizzata per impostare il testo iniziale contenuto in un controllo . La stringa può anche contenere proprietà incorporate. Per la sintassi di una stringa formattata contenente proprietà, vedere la [**funzione MsiFormatRecord.**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) Specificare le dimensioni, il tipo di carattere e il colore del testo antendo alla stringa di testo { style}, dove style è uno stile di testo creato nella colonna TextStyle della tabella \\ [TextStyle](textstyle-table.md). La stringa di testo viene troncata se è troppo lunga per adattarsi al controllo. La stringa di testo può essere vuota.

La creazione speciale [](formatted.md) della stringa di testo formattata in questo campo è [](text-control.md) necessaria se il testo deve essere visualizzato da un controllo Testo che si trova in una finestra di dialogo con l'attributo TrackDiskpace. Questo è il caso specificato dal bit di stile della finestra di [dialogo TrackDiskSpace](trackdiskspace-dialog-style-bit.md) visualizzato negli attributi della [tabella Dialog](dialog-table.md). In questo caso, se la stringa formattata nella colonna Text della tabella Control inizia con " " e termina con " ", è necessario aggiungere uno spazio alla fine \[ \] della stringa. Ad esempio, se DlgTextFont è una proprietà che verrà impostata su "{ DlgFontBold}" la stringa formattata \\ " \[ DlgTextFont \] MyText ProductName " richiede lo spazio alla fine dopo la parentesi di \[ \] chiusura. Questo spazio aggiuntivo è necessario al programma di installazione per visualizzare correttamente il testo nel controllo Text.

È possibile immettere una breve stringa di testo descrittiva per i controlli [VolumeCostList](volumecostlist-control.md), [ListView](listview-control.md), [DirectoryList](directorylist-control.md)e [SelectionTree](selectiontree-control.md). Questo testo non viene visualizzato dall'utente, ma può essere letto dalle utilità per la lettura dello schermo come descrizione del controllo.

Vedere anche [Accessibilità.](accessibility.md)

</dd> <dt>

<span id="Control_Next"></span><span id="control_next"></span><span id="CONTROL_NEXT"></span>Controllo \_ successivo
</dt> <dd>

Nome di un altro controllo nella stessa finestra di dialogo e di una chiave esterna per la seconda colonna della tabella Control. Se lo stato attivo nella finestra di dialogo è sul controllo nella colonna Controllo , premendo TAB lo stato attivo viene spostato sul controllo elencato nella colonna \_ Controllo successivo . Questa colonna viene pertanto utilizzata per specificare l'ordine di tabulazione dei controlli nella finestra di dialogo. I collegamenti tra i controlli devono formare un ciclo chiuso. Alcuni controlli, ad esempio i controlli di testo statico, possono essere lasciati fuori dal ciclo. In questo caso, questo campo può essere lasciato vuoto.

Vedere anche [Accessibilità.](accessibility.md)

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>Guida
</dt> <dd>

Stringhe di testo localizzabili facoltative usate con il pulsante ? . La stringa è divisa in due parti da un carattere separatore ( \| ). La prima parte della stringa viene usata come testo della descrizione comando. Questo testo viene usato dalle utilità per la lettura dello schermo per i controlli che contengono un'immagine. La seconda parte della stringa è riservata per un uso futuro. Il carattere separatore è obbligatorio anche se è presente solo uno dei due tipi di testo.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori interi per x, y, larghezza e altezza sono nelle unità del programma [di installazione,](installer-units.md)non nelle unità di dialogo. Un'unità di installazione equivale a un dodicesimo di altezza delle dimensioni del carattere MS Sans Serif a 10 punti. Le coordinate per i controlli sono relative alla griglia.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE23](ice23.md)  
[ICE31](ice31.md)  
[ICE32](ice32.md)  
[ICE34](ice34.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE95](ice95.md)  
</dl>

 

 



