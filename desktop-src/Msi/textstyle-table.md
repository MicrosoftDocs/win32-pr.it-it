---
description: La tabella TextStyle elenca diversi stili di carattere usati nei controlli con testo.
ms.assetid: a351e67a-8f51-41bf-9202-56488b870fa7
title: Tabella TextStyle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f8a5b3141314722bc5b92e34ea214fa8e1505babfbc8b7f942899e6c6779c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623489"
---
# <a name="textstyle-table"></a>Tabella TextStyle

La tabella TextStyle elenca diversi stili di carattere usati nei controlli con testo.

La tabella TextStyle include le colonne seguenti.



| Colonna    | Tipo                               | Chiave | Nullable |
|-----------|------------------------------------|-----|----------|
| TextStyle | [Identificatore](identifier.md)       | S   | N        |
| FaceName  | [Text](text.md)                   | N   | N        |
| Dimensione      | [Integer](integer.md)             | N   | N        |
| Color     | [DoubleInteger](doubleinteger.md) | N   | S        |
| StyleBits | [Integer](integer.md)             | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>TextStyle
</dt> <dd>

Questa colonna è il nome dello stile del carattere. Questo nome può essere incorporato nella stringa di testo per indicare una modifica dello stile. Si noti che il nome dello stile del carattere usato in questo campo non deve terminare con i caratteri \_ UL. Vedere [Aggiunta di controlli e testo](adding-controls-and-text.md).

</dd> <dt>

<span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>FaceName
</dt> <dd>

Stringa che indica il nome del tipo di carattere. La stringa non deve contenere più di 31 caratteri.

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>Dimensione
</dt> <dd>

Dimensione del carattere misurata in punti. Deve essere un numero non negativo.

</dd> <dt>

<span id="Color"></span><span id="color"></span><span id="COLOR"></span>Colore
</dt> <dd>

Questa colonna specifica il colore del testo visualizzato da un [controllo Text](text-control.md). Tutti gli altri tipi di controlli usano sempre il colore del testo predefinito. Il valore inserito in questa colonna deve essere calcolato usando la formula seguente: 65536 blu + 256 verde + rosso, dove rosso, verde e blu sono ognuno nell'intervallo compreso tra \* \* 0 e 255. Il valore non deve superare 16777215, ovvero il valore per il bianco. Il valore è 0 per il nero, 255 per il rosso, 65280 per il verde, 16711680 per il blu e 8421504 per il grigio. Lasciando vuoto il campo, viene specificato il colore predefinito.

Non posizionare i controlli [Text trasparenti](text-control.md) sopra le bitmap colorate. Il testo potrebbe non essere visibile se l'utente modifica la combinazione di colori di visualizzazione. Ad esempio, il testo può diventare invisibile se l'utente imposta il parametro di contrasto elevato per l'accessibilità.

</dd> <dt>

<span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits
</dt> <dd>

Combinazione di bit che indica la formattazione del testo.

I singoli bit di stile hanno i valori seguenti.



| Costante                             | Valore esadecimale | Decimal | Stile      |
|--------------------------------------|-------------|---------|------------|
| **msidbTextStyleStyleBitsBold**      | 0x001       | 1       | Bold       |
| **msidbTextStyleStyleBitsItalic**    | 0x002       | 2       | Corsivo     |
| **msidbTextStyleStyleBitsUnderline** | 0x004       | 4       | Sottolineato  |
| **msidbTextStyleStyleBitsStrike**    | 0x008       | 8       | Strike out |



 

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE31](ice31.md)  
[ICE45](ice45.md)  
</dl>

 

 



