---
title: Spazi colori HLS
description: Gli spazi colori HLS sono ampiamente usati anche dagli autori. I componenti di colore sono tonalità, luminosità e saturazione (chroma).
ms.assetid: 8c80d200-c4d0-4233-8f53-a9637dff9ab2
keywords:
- Windows Sistema colori (WCS), spazi colori HLS
- WCS (Windows Color System),Spazi colori HLS
- gestione dei colori delle immagini, spazi colori HLS
- gestione dei colori, spazi colori HLS
- colori, spazi colori HLS
- spazi colori, HLS
- Spazi colori HLS
- Hue
- Saturazione
- Leggerezza
- saturazione zero
- Saturazione della luminosità della tonalità (HLS)
- HLS (saturazione della luminosità della tonalità)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d0dc0c47555f5358360a1ac81faf113c0fd6e98572c4d0c96852070a1749073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934967"
---
# <a name="hls-color-spaces"></a>Spazi colori HLS

Gli [spazi](c.md) colori HLS sono ampiamente usati anche dagli autori. I componenti di colore sono tonalità, luminosità e saturazione (chroma).

Hue ha lo stesso significato del modello HSV, ad eccezione del fatto che un angolo di tonalità 0 corrisponde al blu in questo modello. Magenta è a 60, il rosso a 120. Come per il modello HSV, i colori complementari sono distanti 180.

La leggerezza è la quantità di nero o bianco in un colore. L'aumento della leggerezza aggiunge il bianco alla tonalità. La riduzione della leggerezza aggiunge nero alla tonalità.

[La saturazione](s.md) nel modello HLS è una misura della "purezza" di una tonalità. Quando la saturazione diminuisce, la tonalità diventa più grigia. Un valore di saturazione pari a zero restituisce un valore in scala di grigi.

La figura seguente è un disegno di linee dello spazio HLS, ovvero un doppio esadecimale. Qualsiasi sezione incrociata orizzontale dello spazio colori HLS è un esagono. HLS è uno spazio colori normalizzato. Ciò significa che i valori di leggerezza e saturazione sono compresi tra 0,0 e 1,0 inclusi. Hue varia da 0 a 360 inclusi.

![Spazio colore hls](images/hlsline.png)

Gli spazi colori HLS possono essere dipendenti dal dispositivo o indipendenti dal dispositivo.

 

 




