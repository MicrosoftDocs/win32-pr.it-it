---
description: Il formato trama DXT1 è per le trame opache o con un singolo colore trasparente.
ms.assetid: a890ed0a-1f68-45b8-93cb-b621d1908d9f
title: Trame alfa opache e a 1 bit (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda620810e48cba519322f3f2426555443fb696f524f4fbe7752a8c7aaedba73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728186"
---
# <a name="opaque-and-1-bit-alpha-textures-direct3d-9"></a>Trame alfa opache e a 1 bit (Direct3D 9)

Il formato trama DXT1 è per le trame opache o con un singolo colore trasparente.

Per ogni blocco alfa opaco o a 1 bit, vengono archiviati due valori a 16 bit (formato RGB 5:6:5) e una bitmap 4x4 con 2 bit per pixel. In questo modo vengono totali 64 bit per 16 texel o quattro bit per texel. Nella bitmap a blocchi sono presenti 2 bit per texel per selezionare tra i quattro colori, due dei quali vengono archiviati nei dati codificati. Gli altri due colori derivano da questi colori archiviati tramite interpolazione lineare. Questo layout è illustrato nel diagramma seguente.

![Diagramma del layout bitmap](images/colors1.png)

Il formato alfa a 1 bit si distingue dal formato opaco confrontando i due valori di colore a 16 bit archiviati nel blocco . Vengono considerati come interi senza segno. Se il primo colore è maggiore del secondo, implica che vengono definiti solo texel opachi. Ciò significa che vengono usati quattro colori per rappresentare i texel. Nella codifica a quattro colori sono presenti due colori derivati e tutti e quattro i colori sono distribuiti equamente nello spazio colore RGB. Questo formato è analogo al formato RGB 5:6:5. In caso contrario, per la trasparenza alfa a 1 bit vengono usati tre colori e il quarto è riservato per rappresentare texel trasparenti.

Nella codifica a tre colori è presente un colore derivato e il quarto codice a 2 bit è riservato per indicare un texel trasparente (informazioni alfa). Questo formato è analogo a RGBA 5:5:5:1, in cui il bit finale viene usato per codificare la maschera alfa.

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



È consigliabile impostare i componenti RGBA del pixel di trasparenza su zero prima della fusione.

Le tabelle seguenti illustrano il layout di memoria per il blocco di 8 byte. Si presuppone che il primo indice corrisponda alla coordinata y e il secondo corrisponda alla coordinata x. Ad esempio, Texel 1 2 fa riferimento al pixel della mappa \[ \] \[ di trama in \] (x,y) = (2,1).

Questa tabella contiene il layout di memoria per il blocco a 8 byte (64 bit).



| Indirizzo di Word | Parola a 16 bit    |
|--------------|----------------|
| 0            | Colore \_ 0       |
| 1            | Colore \_ 1       |
| 2            | Bitmap Word \_ 0 |
| 3            | Bitmap Word \_ 1 |



 

Il \_ colore 0 e il \_ colore 1, i colori ai due estremi, sono disposti come segue:



| BITS        | Color                 |
|-------------|-----------------------|
| 4:0 (LSB \* ) | Componente colore blu  |
| 10:5        | Componente colore verde |
| 15:11       | Componente colore rosso   |



 

\*bit meno significativo

Bitmap Word \_ 0 è disposto come segue:



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

Bitmap Word \_ 1 è strutturato come segue:



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



 

## <a name="example-of-opaque-color-encoding"></a>Esempio di codifica colori opaca

Come esempio di codifica opaca, si supponga che i colori rosso e nero siano agli estremi. Il rosso è \_ il colore 0 e il nero il \_ colore 1. Sono disponibili quattro colori interpolati che formano la sfumatura distribuita in modo uniforme tra di essi. Per determinare i valori per la bitmap 4x4, vengono usati i calcoli seguenti:


```
00 ? color_0
01 ? color_1
10 ? 2/3 color_0 + 1/3 color_1
11 ? 1/3 color_0 + 2/3 color_1
```



La bitmap sarà quindi simile al diagramma seguente.

![Diagramma che mostra il layout bitmap espanso.](images/colors2.png)

L'aspetto è simile alla serie di colori illustrata di seguito.

> [!Note]  
> In un'immagine viene visualizzato il pixel (0,0) in alto a sinistra.

 

![illustrazione di una sfumatura codificata opaca](images/redsquares.png)

## <a name="example-of-1-bit-alpha-encoding"></a>Esempio di codifica alfa a 1 bit

Questo formato viene selezionato quando l'intero senza segno a 16 bit, il colore 0, è minore dell'intero senza segno a \_ 16 bit, colore \_ 1. Un esempio di dove è possibile usare questo formato è la foglia su un albero, mostrata su un cielo blu. Alcuni texel possono essere contrassegnati come trasparenti, mentre tre sfumature di verde sono ancora disponibili per le foglia. Due colori correggino gli estremi e il terzo è un colore interpolato.

La figura seguente è un esempio di tale immagine.

![illustrazione della codifica alfa a 1 bit](images/greenthing.png)

Si noti che se l'immagine viene visualizzata come bianca, il texel viene codificato come trasparente. Si noti anche che i componenti RGBA dei texel trasparenti devono essere impostati su zero prima della fusione.

La codifica bitmap per i colori e la trasparenza viene determinata usando i calcoli seguenti.


```
00 ? color_0
01 ? color_1
10 ? 1/2 color_0 + 1/2 color_1
11   ?   Transparent
```



La bitmap sarà quindi simile al diagramma seguente.

![diagramma del layout bitmap espanso](images/colors3.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse di trama compresse](compressed-texture-resources.md)
</dt> </dl>

 

 



