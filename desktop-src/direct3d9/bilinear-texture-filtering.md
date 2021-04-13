---
description: Le trame vengono sempre risolte in modo lineare da (0,0, 0,0) nell'angolo superiore sinistro a (1,0, 1,0) nell'angolo inferiore destro, come illustrato nella figura seguente.
ms.assetid: 16fb04b9-4476-4dbe-a24f-51c0813a7917
title: Filtraggio bilineare della trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51213e5187c775963de2fa740847d55084c5be2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401492"
---
# <a name="bilinear-texture-filtering-direct3d-9"></a>Filtraggio bilineare della trama (Direct3D 9)

Le trame vengono sempre risolte in modo lineare da (0,0, 0,0) nell'angolo superiore sinistro a (1,0, 1,0) nell'angolo inferiore destro, come illustrato nella figura seguente.

![illustrazione della trama 4x4 con blocchi di colore solidi](images/bilinear-fig7a.png)

Le trame vengono in genere rappresentate come se fossero composte da blocchi di colore solidi, ma in realtà è più corretto pensare alle trame nello stesso modo in cui si pensa alla visualizzazione raster: ogni Texel è definito al centro esatto di una cella della griglia, come illustrato nella figura seguente.

![illustrazione della trama 4x4 con Texel definiti al centro delle celle della griglia](images/bilinear-fig7b.png)

Se si chiede al campionatore di trame il colore di questa trama a coordinate UV (0,375, 0,375), si otterrà un rosso solido (255, 0, 0). Ciò ha un senso perfetto perché il centro esatto della cella rossa del Texel è a UV (0,375, 0,375). Cosa accade se si chiede al campionatore il colore della trama a UV (0,25, 0,25)? Non è altrettanto semplice, perché il punto a UV (0,25, 0,25) si trova nell'angolo esatto di 4 Texel.

Lo schema più semplice consiste nel fare in modo che il campionatore restituisca il colore del Texel più vicino; Questa operazione è denominata filtro punti (vedere [campionamento dei punti più vicini (Direct3D 9)](nearest-point-sampling.md)) ed è in genere indesiderato a causa di risultati granulari o di blocco. Il campionamento dei punti con la trama a UV (0,25, 0,25) Mostra un altro problema sottile con il filtro dei punti più vicini: i quattro Texel sono equidistanti dal punto di campionamento, quindi non esiste un singolo Texel più vicino. Uno di questi quattro Texel verrà scelto come colore restituito, ma la selezione dipenderà dalla modalità di arrotondamento della coordinata, che può comportare l'inserimento di elementi di strappo (vedere l'articolo di campionamento Nearest-Point nell'SDK).

Uno schema di filtro leggermente più preciso e più comune consiste nel calcolare la media ponderata dei 4 Texel più vicini al punto di campionamento. si tratta di un filtro bilineare e il costo di calcolo aggiuntivo è in genere trascurabile perché questa routine viene implementata nell'hardware grafico moderno. Ecco i colori ottenibili in alcuni punti di campionamento diversi usando i filtri bilineari:


```
UV: (0.5, 0.5)
```



Questo punto è al bordo esatto tra i Texel rosso, verde, blu e bianco. Il colore restituito dal campionatore è grigio:


```
  0.25 * (255, 0, 0)
  0.25 * (0, 255, 0) 
  0.25 * (0, 0, 255) 
## + 0.25 * (255, 255, 255) 
------------------------
= (128, 128, 128)
```




```
UV: (0.5, 0.375)
```



Questo punto si trova al punto medio del bordo tra i Texel rossi e verdi. Il colore restituito dal campionatore è giallo-grigio (si noti che i contributi dei Texel blu e bianco vengono ridimensionati a 0):


```
  0.5 * (255, 0, 0)
  0.5 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (128, 128, 0)
```




```
UV: (0.375, 0.375)
```



Si tratta dell'indirizzo del Texel rosso, che corrisponde al colore restituito (tutti gli altri Texel nel calcolo di filtro vengono ponderati in 0):


```
  1.0 * (255, 0, 0)
  0.0 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (255, 0, 0)
```



Confrontare questi calcoli con la figura seguente, che mostra cosa accade se il calcolo del filtro bilineare viene eseguito a ogni indirizzo di trama nella trama 4x4.

![illustrazione della trama 4x4 con filtro bilineare eseguito a ogni indirizzo di trama](images/bilinear-fig7c.jpg)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtraggio trama](texture-filtering.md)
</dt> </dl>

 

 



