---
description: La tabella TextStyle elenca diversi stili di carattere usati nei controlli con testo.
ms.assetid: a351e67a-8f51-41bf-9202-56488b870fa7
title: Tabella TextStyle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9993362228e37f01c0e53683755f7bd1310eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966824"
---
# <a name="textstyle-table"></a>Tabella TextStyle

La tabella TextStyle elenca diversi stili di carattere usati nei controlli con testo.

La tabella TextStyle include le colonne seguenti.



| Colonna    | Tipo                               | Chiave | Nullable |
|-----------|------------------------------------|-----|----------|
| TextStyle | [Identificatore](identifier.md)       | S   | N        |
| Contemplato  | [Text](text.md)                   | N   | N        |
| Dimensione      | [Integer](integer.md)             | N   | N        |
| Colore     | [DoubleInteger](doubleinteger.md) | N   | S        |
| StyleBits | [Integer](integer.md)             | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>TextStyle
</dt> <dd>

Questa colonna è il nome dello stile del tipo di carattere. Questo nome può essere incorporato nella stringa di testo per indicare una modifica dello stile. Si noti che il nome dello stile del tipo di carattere usato in questo campo non deve terminare con i caratteri: \_ ul. Vedere [aggiunta di controlli e testo](adding-controls-and-text.md).

</dd> <dt>

<span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>Contemplato
</dt> <dd>

Stringa che indica il nome del tipo di carattere. La lunghezza della stringa non deve superare i 31 caratteri.

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>Dimensioni
</dt> <dd>

Dimensione del carattere misurata in punti. Deve essere un numero non negativo.

</dd> <dt>

<span id="Color"></span><span id="color"></span><span id="COLOR"></span>Colore
</dt> <dd>

In questa colonna viene specificato il colore del testo visualizzato da un [controllo di testo](text-control.md). Tutti gli altri tipi di controlli utilizzano sempre il colore predefinito del testo. Il valore inserito in questa colonna deve essere calcolato utilizzando la formula seguente: 65536 \* blu + 256 \* verde + rosso, dove rosso, verde e blu sono ciascuno nell'intervallo 0-255. Il valore non deve superare 16777215, ovvero il valore per il bianco. Il valore è 0 per il nero, 255 per il rosso, 65280 per il verde, 16711680 per il blu e 8421504 per il grigio. Se si lascia vuoto il campo, viene specificato il colore predefinito.

Non posizionare [controlli testo](text-control.md) trasparenti su bitmap colorate. Il testo potrebbe non essere visibile se l'utente modifica la combinazione di colori di visualizzazione. Ad esempio, il testo potrebbe diventare invisibile se l'utente imposta il parametro a contrasto elevato per l'accessibilità.

</dd> <dt>

<span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits
</dt> <dd>

Combinazione di bit che indica la formattazione del testo.

I singoli bit di stile hanno i valori seguenti.



| Costante                             | Valore esadecimale | Decimal | Stile      |
|--------------------------------------|-------------|---------|------------|
| **msidbTextStyleStyleBitsBold**      | 0x001       | 1       | Grassetto       |
| **msidbTextStyleStyleBitsItalic**    | 0x002       | 2       | Corsivo     |
| **msidbTextStyleStyleBitsUnderline** | 0x004       | 4       | Sottolineato  |
| **msidbTextStyleStyleBitsStrike**    | 0x008       | 8       | Sciopero |



 

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE31](ice31.md)  
[ICE45](ice45.md)  
</dl>

 

 



