---
description: Per riempire una forma con un colore a tinta unita, creare un oggetto SolidBrush e quindi passare l'indirizzo di tale oggetto SolidBrush come argomento a uno dei metodi Fill della classe Graphics.
ms.assetid: cedef138-5047-4a72-8b89-5a95062a351c
title: Riempimento di una forma con un colore a tinta unita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c4a6221d84c4a891d377d974f168468917799e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994261"
---
# <a name="filling-a-shape-with-a-solid-color"></a>Riempimento di una forma con un colore a tinta unita

Per riempire una forma con un colore a tinta unita, creare un oggetto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) e quindi passare l'indirizzo di tale oggetto **SolidBrush** come argomento a uno dei metodi Fill della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Nell'esempio seguente viene illustrato come riempire un'ellisse con il colore rosso:


```
SolidBrush solidBrush(Color(255, 255, 0, 0));
stat = graphics.FillEllipse(&solidBrush, 0, 0, 100, 60);
```



Nell'esempio precedente, il costruttore [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) accetta un riferimento a un oggetto [**colore**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) come unico argomento. I valori utilizzati dal costruttore di **colori** rappresentano i componenti alfa, rosso, verde e blu del colore. Ognuno di questi valori deve essere compreso tra 0 e 255. Il primo 255 indica che il colore è completamente opaco e il secondo 255 indica che il componente rosso è a intensità piena. I due zeri indicano che i componenti verde e blu hanno un'intensità pari a 0.

I quattro numeri (0, 0, 100, 60) passati al metodo [**Graphics:: FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) specificano la posizione e le dimensioni del rettangolo di delimitazione per l'ellisse. Il rettangolo ha un angolo superiore sinistro di (0,0), una larghezza di 100 e un'altezza di 60.

 

 
