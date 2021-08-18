---
description: Uso di RGB a 16 bit
ms.assetid: 0a245187-4120-4003-9a8f-6b1e8fa40d38
title: Uso di RGB a 16 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660d5b0223bab6c19a89e4316f7dffce56ec0545f83c72f7316b9278dfa3e4c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071795"
---
# <a name="working-with-16-bit-rgb"></a>Uso di RGB a 16 bit

Per RGB non compresso a 16 bit sono definiti due formati:

-   MEDIASUBTYPE \_ 555 usa cinque bit ciascuno per i componenti rosso, verde e blu in un pixel. Il bit più significativo in **WORD viene** ignorato.
-   MEDIASUBTYPE 565 usa cinque bit per i componenti rosso e blu \_ e sei bit per il componente verde. Questo formato riflette il fatto che la visione umana è più sensibile alle parti verdi dello spettro visibile.

**RGB 565**

Per estrarre i componenti di colore da un'immagine RGB 565, considerare ogni pixel come tipo **WORD** e usare le maschere di bit seguenti:


```C++
WORD red_mask = 0xF800;
WORD green_mask = 0x7E0;
WORD blue_mask = 0x1F;
```



Ottenere i componenti di colore da un pixel come indicato di seguito:


```C++
BYTE red_value = (pixel & red_mask) >> 11;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);
```



Tenere presente che i canali rosso e blu sono a 5 bit e il canale verde è a 6 bit. Per convertire questi valori in componenti a 8 bit (per RGB a 24 o 32 bit), è necessario spostare a sinistra il numero appropriato di bit:


```C++
// Expand to 8-bit values.
BYTE red   = red_value << 3;
BYTE green = green_value << 2;
BYTE blue  = blue_value << 3;
```



Invertire questo processo per creare un RGB da 565 pixel. Supponendo che i valori dei colori siano stati troncati al numero corretto di bit:


```C++
WORD pixel565 = (red_value << 11) | (green_value << 5) | blue_value;
```



**RGB 555**

L'uso di RGB 555 è essenzialmente lo stesso di RGB 565, ad eccezione delle maschere di bit e delle operazioni di spostamento di bit diverse. Per ottenere i componenti di colore da un RGB da 555 pixel, eseguire le operazioni seguenti:


```C++
WORD red_mask = 0x7C00;
WORD green_mask = 0x3E0;
WORD blue_mask = 0x1F;

BYTE red_value = (pixel & red_mask) >> 10;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);

// Expand to 8-bit values:
BYTE red   = red_value << 3;
BYTE green = green_value << 3;
BYTE blue  = blue_value << 3;
```



Per imballare i valori dei colori rosso, verde e blu in un RGB di 555 pixel, eseguire le operazioni seguenti:


```C++
WORD pixel565 = (red << 10) | (green << 5) | blue;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sottotipi video RGB non compressi](uncompressed-rgb-video-subtypes.md)
</dt> </dl>

 

 



