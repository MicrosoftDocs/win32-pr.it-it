---
description: Per riempire una forma con un colore a tinta unita, creare un oggetto SolidBrush e quindi passare l'indirizzo di tale oggetto SolidBrush come argomento a uno dei metodi di riempimento della classe Graphics.
ms.assetid: cedef138-5047-4a72-8b89-5a95062a351c
title: Riempimento di una forma con un colore a tinta unita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ad3ecb5efb3bde32f696db8b97319d89834886eb63a70cd45289e49db03863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036719"
---
# <a name="filling-a-shape-with-a-solid-color"></a>Riempimento di una forma con un colore a tinta unita

Per riempire una forma con un colore a tinta unita, creare un [**oggetto SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) e quindi passare l'indirizzo di tale **oggetto SolidBrush** come argomento a uno dei metodi di riempimento della [**classe Graphics.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) L'esempio seguente illustra come riempire un'ellisse con il colore rosso:


```
SolidBrush solidBrush(Color(255, 255, 0, 0));
stat = graphics.FillEllipse(&solidBrush, 0, 0, 100, 60);
```



Nell'esempio precedente, il [**costruttore SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) accetta un riferimento all'oggetto [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) come unico argomento. I valori utilizzati dal **costruttore Color** rappresentano i componenti alfa, rosso, verde e blu del colore. Ognuno di questi valori deve essere compreso nell'intervallo compreso tra 0 e 255. Il primo 255 indica che il colore è completamente opaco e il secondo 255 indica che il componente rosso è a piena intensità. I due zeri indicano che i componenti verde e blu hanno entrambe un'intensità pari a 0.

I quattro numeri (0, 0, 100, 60) passati al metodo [**Graphics::FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) specificano la posizione e le dimensioni del rettangolo di delimitazione per l'ellisse. Il rettangolo ha un angolo superiore sinistro (0, 0), una larghezza di 100 e un'altezza di 60.

 

 
