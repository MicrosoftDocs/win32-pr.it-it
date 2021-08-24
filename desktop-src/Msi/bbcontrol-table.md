---
description: La tabella BBControl elenca i controlli da visualizzare in ogni manifesto.
ms.assetid: 2ab31a32-6d33-46b7-a295-199560efa7fb
title: Tabella BBControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70198167c866195204ec6cbcf644b92f3489a4ff44e14e719efbf5c6647e30c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754371"
---
# <a name="bbcontrol-table"></a>Tabella BBControl

La tabella BBControl elenca i controlli da visualizzare in ogni manifesto.

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

Nome del manifesto.

Chiave esterna alla colonna uno della [tabella Disasserta](billboard-table.md).

</dd> <dt>

<span id="BBControl"></span><span id="bbcontrol"></span><span id="BBCONTROL"></span>BBControl
</dt> <dd>

Nome del controllo. Questo nome deve essere univoco all'interno di un manifesto pubblicitario, ma può essere ripetuto in diversi manifesti. Questa colonna in combinazione con la colonna Manifesto \_ costituisce la chiave primaria della tabella.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>digitare
</dt> <dd>

Tipo del controllo. Solo i controlli statici, ad esempio [un controllo Text,](text-control.md) [Bitmap,](bitmap-control.md) [Icon](icon-control.md)o custom control, possono essere posizionati in un manifesto. Per un elenco completo dei controlli, vedere la [sezione](controls.md) Controlli.

</dd> <dt>

<span id="X"></span><span id="x"></span>X
</dt> <dd>

Coordinata orizzontale dell'angolo superiore sinistro del limite rettangolare del controllo. Le unità sono unità [del programma di installazione.](installer-units.md) Questa coordinata viene misurata in relazione al controllo e non al dialogo. Usare solo numeri non negativi.

</dd> <dt>

<span id="Y"></span><span id="y"></span>Y
</dt> <dd>

Coordinata verticale dell'angolo superiore sinistro del limite rettangolare del controllo. Le unità sono unità [del programma di installazione.](installer-units.md) Questa coordinata viene misurata in relazione al controllo e non al dialogo. Questo numero deve essere non negativo.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Larghezza
</dt> <dd>

Larghezza del limite rettangolare del controllo. Le unità sono unità [del programma di installazione.](installer-units.md) Questo numero deve essere non negativo.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Altezza
</dt> <dd>

Altezza del limite rettangolare del controllo. Le unità sono unità [del programma di installazione.](installer-units.md) Questo numero deve essere non negativo.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

Parola a 32 bit che specifica i flag di attributo da applicare a questo controllo. Questo numero deve essere non negativo e specificare un attributo per un controllo statico valido per il posizionamento in un oggetto . Per informazioni sui valori numerici da immettere in questo campo, vedere l'attributo specifico in [Attributi di controllo](control-attributes.md).

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Testo
</dt> <dd>

Questa colonna contiene una stringa localizzabile utilizzata per impostare il testo iniziale nel controllo se il controllo visualizza testo. La stringa viene troncata se il testo è troppo lungo per adattarsi al controllo. Questa colonna contiene una chiave nella tabella [Binary](binary-table.md) se il controllo è un pulsante di push o una casella di controllo contenente un'icona o una bitmap. Non è possibile visualizzare sia testo che un'immagine sullo stesso pulsante. Questa colonna può essere lasciata vuota.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori interi per x, y, width e height sono nelle unità [del programma di installazione,](installer-units.md)non nelle unità di dialogo. Un'unità di installazione equivale a un dodicesimo dell'altezza della dimensione del carattere MS Sans Serif a 10 punti. Le coordinate per i controlli sono relative al controllo barrato e non alla finestra di dialogo.

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

 

 



