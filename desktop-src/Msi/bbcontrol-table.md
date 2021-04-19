---
description: Nella tabella BBControl sono elencati i controlli da visualizzare in ogni Billboard.
ms.assetid: 2ab31a32-6d33-46b7-a295-199560efa7fb
title: Tabella BBControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfebbdbc474ef88cbf26f34555deb4874840d005
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311021"
---
# <a name="bbcontrol-table"></a>Tabella BBControl

Nella tabella BBControl sono elencati i controlli da visualizzare in ogni Billboard.

La tabella BBControl include le colonne seguenti.



| Colonna      | Tipo                               | Chiave | Nullable |
|-------------|------------------------------------|-----|----------|
| Billboard\_ | [Identificatore](identifier.md)       | S   | N        |
| BBControl   | [Identificatore](identifier.md)       | S   | N        |
| Tipo        | [Identificatore](identifier.md)       | N   | N        |
| X           | [Integer](integer.md)             | N   | N        |
| S           | [Integer](integer.md)             | N   | N        |
| Larghezza       | [Integer](integer.md)             | N   | N        |
| Altezza      | [Integer](integer.md)             | N   | N        |
| Attributi  | [DoubleInteger](doubleinteger.md) | N   | S        |
| Testo        | [Text](text.md)                   | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Billboard_"></span><span id="billboard_"></span><span id="BILLBOARD_"></span>Billboard\_
</dt> <dd>

Nome del tabellone.

Chiave esterna per la colonna uno della [tabella Billboard](billboard-table.md).

</dd> <dt>

<span id="BBControl"></span><span id="bbcontrol"></span><span id="BBCONTROL"></span>BBControl
</dt> <dd>

Nome del controllo. Questo nome deve essere univoco all'interno di un cartellone, ma può essere ripetuto in cartelloni diversi. Questa colonna combinata con la \_ colonna Billboard costituisce la chiave primaria della tabella.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo
</dt> <dd>

Tipo del controllo. Solo i controlli statici, ad esempio un [testo](text-control.md), una [bitmap](bitmap-control.md), un' [icona](icon-control.md)o un controllo personalizzato, possono essere inseriti in un tabellone. Per un elenco completo dei controlli, vedere la sezione [controlli](controls.md) .

</dd> <dt>

<span id="X"></span><span id="x"></span>X
</dt> <dd>

Coordinata orizzontale dell'angolo superiore sinistro del limite rettangolare del controllo. Le unità sono [unità del programma di installazione](installer-units.md). Questa coordinata viene misurata in relazione al controllo Billboard e non rispetto alla finestra di dialogo. Usare solo numeri non negativi.

</dd> <dt>

<span id="Y"></span><span id="y"></span>Y
</dt> <dd>

Coordinata verticale dell'angolo superiore sinistro del limite rettangolare del controllo. Le unità sono [unità del programma di installazione](installer-units.md). Questa coordinata viene misurata in relazione al controllo Billboard e non rispetto alla finestra di dialogo. Questo numero deve essere non negativo.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Larghezza
</dt> <dd>

Larghezza del limite rettangolare del controllo. Le unità sono [unità del programma di installazione](installer-units.md). Questo numero deve essere non negativo.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Altezza
</dt> <dd>

Altezza del limite rettangolare del controllo. Le unità sono [unità del programma di installazione](installer-units.md). Questo numero deve essere non negativo.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

Parola a 32 bit che specifica i flag di attributo da applicare a questo controllo. Questo numero deve essere non negativo e specificare un attributo per un controllo statico valido per la selezione host in un tabellone. Per informazioni sui valori numerici da immettere in questo campo, vedere l'attributo particolare sotto [gli attributi del controllo](control-attributes.md).

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Testo
</dt> <dd>

Questa colonna contiene una stringa localizzabile utilizzata per impostare il testo iniziale nel controllo se il controllo Visualizza il testo. La stringa viene troncata se il testo è troppo lungo per essere adattato al controllo. Questa colonna contiene una chiave nella [tabella binaria](binary-table.md) se il controllo è un pulsante di comando o una casella di controllo contenente un'icona o una bitmap. Non è possibile visualizzare sia il testo che un'immagine sullo stesso pulsante. Questa colonna può essere lasciata vuota.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori interi per x, y, larghezza e altezza si trovano nelle [unità del programma di installazione](installer-units.md), non nelle unità di dialogo. Un'unità del programma di installazione è uguale a un dodicesimo dell'altezza delle dimensioni del carattere MS Sans Serif a 10 punti. Le coordinate per i controlli sono relative al controllo Billboard non alla finestra di dialogo.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE95](ice95.md)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
</dt> </dl>

 

 



