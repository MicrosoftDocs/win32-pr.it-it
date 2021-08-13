---
description: I pulsanti di opzione non vengono considerati come singoli controlli, ma fanno parte di un gruppo di pulsanti di opzione che funziona come un controllo RadioButtonGroup. La tabella RadioButton elenca i pulsanti per tutti i gruppi.
ms.assetid: 7f8f278a-a737-4116-9938-2850dbb611fa
title: Tabella RadioButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ffc91ece6b5c71cd6ba46143f33e49b90b0278139d194a218a2fddb797bb55a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381051"
---
# <a name="radiobutton-table"></a>Tabella RadioButton

I pulsanti di opzione non vengono considerati come singoli controlli, ma fanno parte di un gruppo di pulsanti di opzione che funziona come [un controllo RadioButtonGroup](radiobuttongroup-control.md). La tabella RadioButton elenca i pulsanti per tutti i gruppi.

La tabella RadioButton contiene le colonne seguenti.



| Colonna   | Tipo                         | Chiave | Nullable |
|----------|------------------------------|-----|----------|
| Proprietà | [Identificatore](identifier.md) | S   | N        |
| JSON    | [Integer](integer.md)       | S   | N        |
| Valore    | [Formattato](formatted.md)   | N   | N        |
| X        | [Integer](integer.md)       | N   | N        |
| S        | [Integer](integer.md)       | N   | N        |
| Larghezza    | [Integer](integer.md)       | N   | N        |
| Altezza   | [Integer](integer.md)       | N   | N        |
| Testo     | [Formattato](formatted.md)   | N   | S        |
| Help     | [Text](text.md)             | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà
</dt> <dd>

Proprietà denominata da aggiungere a questo pulsante di opzione. Tutti i pulsanti associati alla stessa proprietà diventano parte dello stesso gruppo.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordine
</dt> <dd>

Intero positivo utilizzato per determinare l'ordinamento degli elementi all'interno di un elenco. Non è necessario che i numeri interi siano consecutivi.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Stringa del valore associata a questo pulsante. Selezionando il pulsante, la proprietà associata viene impostata su questo valore.

</dd> <dt>

<span id="X"></span><span id="x"></span>X
</dt> <dd>

Coordinata orizzontale all'interno del gruppo dell'angolo superiore sinistro del rettangolo di delimitazione del pulsante di opzione. Deve essere un numero non negativo.

</dd> <dt>

<span id="Y"></span><span id="y"></span>Y
</dt> <dd>

Coordinata verticale all'interno del gruppo dell'angolo superiore sinistro del rettangolo di delimitazione del pulsante di opzione. Deve essere un numero non negativo.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Larghezza
</dt> <dd>

La larghezza del pulsante. Deve essere un numero non negativo.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Altezza
</dt> <dd>

Altezza del pulsante. Deve essere un numero non negativo.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Testo
</dt> <dd>

Titolo visibile localizzabile da assegnare al pulsante di opzione. Se il testo è troppo lungo per essere contenuto nel controllo, viene troncato. Se il pulsante visualizza un'icona o una bitmap, questa colonna contiene il nome dell'immagine, ovvero una chiave nella [tabella binaria](binary-table.md). Non è possibile visualizzare sia un'immagine che il testo in un pulsante.

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>Guida
</dt> <dd>

Stringhe della Guida usate con il pulsante. Il testo è facoltativo ed è localizzabile. La stringa è divisa in due parti separate da un carattere ( \| ). La prima parte della stringa viene usata come testo della descrizione comando. Questo testo viene visualizzato dalle utilità per la lettura dello schermo per i controlli che contengono un'immagine. La seconda parte viene usata per la Guida sensibile al contesto, anche se la Guida sensibile al contesto non è ancora stata implementata. Il carattere separatore è obbligatorio anche se è presente solo uno dei due tipi di testo.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori interi per x, y, larghezza e altezza sono nelle unità del programma [di installazione,](installer-units.md)non nelle unità di dialogo. Un'unità di installazione equivale a un dodicesimo di altezza delle dimensioni del carattere MS Sans Serif a 10 punti. Le coordinate per i controlli sono relative alla griglia.

Le coordinate dei pulsanti vengono fornite in relazione al gruppo. Se le coordinate del gruppo vengono modificate, i pulsanti all'interno del gruppo rimangono nella stessa posizione relativa tra loro.

Il contenuto dei campi Value e Text viene formattato dalla funzione [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando viene creato il controllo, pertanto può contenere qualsiasi espressione che la **funzione MsiFormatRecord** è in grado di interpretare. La formattazione si verifica solo quando viene creato il controllo e non viene aggiornata se una proprietà coinvolta nell'espressione viene modificata durante il ciclo di vita del controllo.

Ogni controllo RadioButtonGroup è associato a una proprietà. Il valore predefinito per questa proprietà deve essere inizializzato nella [tabella Property](property-table.md). All'interno di ogni radioButtonGroup specificato nella tabella RadioButton, può essere presente un pulsante di opzione con un valore nel campo Valore che corrisponde al valore predefinito per questa proprietà. Questo è il pulsante predefinito per il controllo RadioButtonGroup. Il pulsante predefinito viene inizialmente visualizzato come selezionato nel controllo .

Si noti che l'utente non può modificare lo stato attivo in una finestra di dialogo premendo TAB in un controllo RadioButtonGroup fino a quando non viene selezionato uno dei pulsanti del gruppo. Per spostare lo stato attivo su questo gruppo di pulsanti premendo TAB, specificare uno dei pulsanti come pulsante predefinito per il gruppo.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE34](ice34.md)  
[ICE46](ice46.md)  
</dl>

 

 



