---
description: Il formato di trama DXT1 è per le trame opache o con un solo colore trasparente.
ms.assetid: a890ed0a-1f68-45b8-93cb-b621d1908d9f
title: Trame alfa opache e a 1 bit (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f629eff594d28d9a807021c0b9df0bd05ea66c3
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104567420"
---
# <a name="opaque-and-1-bit-alpha-textures-direct3d-9"></a>Trame alfa opache e a 1 bit (Direct3D 9)

Il formato di trama DXT1 è per le trame opache o con un solo colore trasparente.

Per ogni blocco alfa opaco o a 1 bit, vengono archiviati i valori a 2 16 bit (formato RGB 5:6:5) e una bitmap 4x4 con 2 bit per pixel. Questo totale 64 bit per 16 Texel o quattro bit per Texel. Nella bitmap a blocchi sono disponibili 2 bit per Texel per la selezione tra i quattro colori, due dei quali sono archiviati nei dati codificati. Gli altri due colori sono derivati da questi colori archiviati dall'interpolazione lineare. Questo layout è illustrato nel diagramma seguente.

![diagramma del layout bitmap](images/colors1.png)

Il formato Alpha a 1 bit si distingue dal formato opaco confrontando i valori dei colori a 2 16 bit archiviati nel blocco. Vengono considerati come interi senza segno. Se il primo colore è maggiore del secondo, significa che sono definiti solo Texel opachi. Ciò significa che per rappresentare i Texel vengono utilizzati quattro colori. Nella codifica a quattro colori sono presenti due colori derivati e tutti e quattro i colori vengono distribuiti equamente nello spazio colore RGB. Questo formato è analogo al formato RGB 5:6:5. In caso contrario, per la trasparenza alpha a 1 bit vengono utilizzati tre colori e il quarto è riservato per rappresentare i Texel trasparenti.

Nella codifica a tre colori è presente un colore derivato e il quarto codice a 2 bit è riservato per indicare un Texel trasparente (informazioni Alpha). Questo formato è analogo a RGBA 5:5:5:1, in cui viene usato il bit finale per la codifica della maschera alfa.

Nell'esempio di codice seguente viene illustrato l'algoritmo per decidere se è selezionata la codifica a tre o quattro colori:


```
if (color_0 > color_1) 
{
    // Four-color block: derive the other two colors.    
    // 00 = color_0, 01 = color_1, 10 = color_2, 11 = color_3
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block.
    color_2 = (2 * color_0 + color_1 + 1) / 3;
    color_3 = (color_0 + 2 * color_1 + 1) / 3;
}    
else
{ 
    // Three-color block: derive the other color.
    // 00 = color_0,  01 = color_1,  10 = color_2,  
    // 11 = transparent.
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block. 
    color_2 = (color_0 + color_1) / 2;    
    color_3 = transparent;    

}
```



Prima di eseguire la fusione è consigliabile impostare su zero i componenti RGBA del pixel di trasparenza.

Nelle tabelle seguenti viene illustrato il layout di memoria per il blocco a 8 byte. Si presuppone che il primo indice corrisponda alla coordinata y e il secondo corrisponda alla coordinata x. Ad esempio, Texel \[ 1 \] \[ 2 \] fa riferimento al pixel della mappa di trama in corrispondenza di (x, y) = (2, 1).

Questa tabella contiene il layout di memoria per il blocco a 8 byte (64 bit).



| Indirizzo di Word | Word a 16 bit    |
|--------------|----------------|
| 0            | Colore \_ 0       |
| 1            | Colore \_ 1       |
| 2            | Bitmap Word \_ 0 |
| 3            | Bitmap Word \_ 1 |



 

\_Il colore 0 e \_ il colore 1, i colori dei due estremi sono disposti come segue:



| BITS        | Colore                 |
|-------------|-----------------------|
| 4:0 (LSB \* ) | Componente colore blu  |
| 10:5        | Componente colore verde |
| 15:11       | Componente colore rosso   |



 

\*bit meno significativo

La bitmap Word \_ 0 è configurata come segue:



| BITS          | Texel           |
|---------------|-----------------|
| 1:0 (LSB)     | Texel \[ 0 \] \[ 0\] |
| 3:2           | Texel \[ 0 \] \[ 1\] |
| 5:4           | Texel \[ 0 \] \[ 2\] |
| 7:6           | Texel \[ 0 \] \[ 3\] |
| 9:8           | Texel \[ 1 \] \[ 0\] |
| 11:10         | Texel \[ 1 \] \[ 1\] |
| 13:12         | Texel \[ 1 \] \[ 2\] |
| 15:14 (MSB \* ) | Texel \[ 1 \] \[ 3\] |



 

\*bit più significativo (MSB)

La bitmap Word \_ 1 è configurata come segue:



| BITS        | Texel           |
|-------------|-----------------|
| 1:0 (LSB)   | Texel \[ 2 \] \[ 0\] |
| 3:2         | Texel \[ 2 \] \[ 1\] |
| 5:4         | Texel \[ 2 \] \[ 2\] |
| 7:6         | Texel \[ 2 \] \[ 3\] |
| 9:8         | Texel \[ 3 \] \[ 0\] |
| 11:10       | Texel \[ 3 \] \[ 1\] |
| 13:12       | Texel \[ 3 \] \[ 2\] |
| 15:14 (MSB) | Texel \[ 3 \] \[ 3\] |



 

## <a name="example-of-opaque-color-encoding"></a>Esempio di codifica dei colori opaca

Come esempio di codifica opaca, si supponga che i colori rosso e nero siano estremi. Il colore rosso è \_ 0 e il nero è il colore \_ 1. Sono disponibili quattro colori interpolati che formano la sfumatura distribuita in modo uniforme tra di essi. Per determinare i valori per la bitmap 4x4, vengono usati i calcoli seguenti:


```
00 ? color_0
01 ? color_1
10 ? 2/3 color_0 + 1/3 color_1
11 ? 1/3 color_0 + 2/3 color_1
```



La bitmap sarà quindi simile al diagramma seguente.

![Diagramma che mostra il layout della bitmap espansa.](images/colors2.png)

Questo aspetto è simile alla serie di colori illustrata di seguito.

> [!Note]  
> In un'immagine, pixel (0, 0) viene visualizzato in alto a sinistra.

 

![illustrazione di una sfumatura con codifica opaca](images/redsquares.png)

## <a name="example-of-1-bit-alpha-encoding"></a>Esempio di codifica Alpha a 1 bit

Questo formato è selezionato quando l'intero senza segno a 16 bit, colore \_ 0, è minore dell'intero senza segno a 16 bit, colore \_ 1. Un esempio di in cui è possibile usare questo formato è il lascia su un albero, visualizzato su un cielo blu. Alcuni Texel possono essere contrassegnati come trasparenti mentre tre tonalità di verde sono ancora disponibili per le foglie. Due colori correggono gli estremi e il terzo è un colore interpolato.

Nell'illustrazione seguente viene illustrato un esempio di tale immagine.

![illustrazione della codifica Alpha a 1 bit](images/greenthing.png)

Si noti che, in cui l'immagine viene visualizzata come bianca, il Texel viene codificato come trasparente. Si noti inoltre che i componenti RGBA dei Texel trasparenti devono essere impostati su zero prima della fusione.

La codifica bitmap per i colori e la trasparenza viene determinata utilizzando i calcoli seguenti.


```
00 ? color_0
01 ? color_1
10 ? 1/2 color_0 + 1/2 color_1
11   ?   Transparent
```



La bitmap sarà quindi simile al diagramma seguente.

![diagramma del layout di bitmap espanso](images/colors3.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse di trama compresse](compressed-texture-resources.md)
</dt> </dl>

 

 



