---
description: Uso di RGB a 16 bit
ms.assetid: 0a245187-4120-4003-9a8f-6b1e8fa40d38
title: Uso di RGB a 16 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6bf4b3217af4d0261d4ab26ca011881762a2a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313393"
---
# <a name="working-with-16-bit-rgb"></a>Uso di RGB a 16 bit

Sono definiti due formati per RGB non compresso a 16 bit:

-   MEDIASUBTYPE \_ 555 utilizza cinque bit per i componenti rosso, verde e blu in un pixel. Il bit più significativo nella **parola** viene ignorato.
-   MEDIASUBTYPE \_ 565 utilizza cinque bit per i componenti rosso e blu e sei bit per il componente verde. Questo formato riflette il fatto che la visione umana è più sensibile alle parti verdi dello spettro visibile.

**RGB 565**

Per estrarre i componenti dei colori da un'immagine RGB 565, considerare ogni pixel come un tipo di **parola** e usare le maschere di bit seguenti:


```C++
WORD red_mask = 0xF800;
WORD green_mask = 0x7E0;
WORD blue_mask = 0x1F;
```



Ottenere i componenti dei colori da un pixel come indicato di seguito:


```C++
BYTE red_value = (pixel & red_mask) >> 11;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);
```



Tenere presente che i canali rosso e blu sono a 5 bit e il canale verde è a 6 bit. Per convertire questi valori in componenti a 8 bit (per RGB a 24 bit o a 32 bit), è necessario spostare a sinistra il numero di bit appropriato:


```C++
// Expand to 8-bit values.
BYTE red   = red_value << 3;
BYTE green = green_value << 2;
BYTE blue  = blue_value << 3;
```



Invertire questo processo per creare un pixel RGB 565. Supponendo che i valori dei colori siano stati troncati al numero corretto di bit:


```C++
WORD pixel565 = (red_value << 11) | (green_value << 5) | blue_value;
```



**RGB 555**

L'uso di RGB 555 è essenzialmente uguale a quello di RGB 565, tranne per le maschere di bit e le operazioni di spostamento di bit sono diverse. Per ottenere i componenti colore da un pixel RGB 555, procedere come segue:


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



Per comprimere i valori di colore rosso, verde e blu in un pixel RGB 555, procedere come segue:


```C++
WORD pixel565 = (red << 10) | (green << 5) | blue;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sottotipi video RGB non compressi](uncompressed-rgb-video-subtypes.md)
</dt> </dl>

 

 



