---
description: GDI+ fornisce sfumature lineari orizzontali, verticali e diagonali. Per impostazione predefinita, il colore in una sfumatura lineare cambia in modo uniforme. Tuttavia, è possibile personalizzare una sfumatura lineare in modo che il colore cambi in modo non uniforme.
ms.assetid: 9b0236b2-be6b-4918-a106-5b0e6c3dd5ff
title: Creazione di una sfumatura lineare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 922c4f1fc805aae25f53ed206d1b3e9112afbd3fa51ba544e121a70839d79d0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015197"
---
# <a name="creating-a-linear-gradient"></a>Creazione di una sfumatura lineare

GDI+ fornisce sfumature lineari orizzontali, verticali e diagonali. Per impostazione predefinita, il colore in una sfumatura lineare cambia in modo uniforme. Tuttavia, è possibile personalizzare una sfumatura lineare in modo che il colore cambi in modo non uniforme.

-   [Sfumature lineari orizzontali](#horizontal-linear-gradients)
-   [Personalizzazione delle sfumature lineari](#customizing-linear-gradients)
-   [Sfumature lineari diagonali](#diagonal-linear-gradients)

## <a name="horizontal-linear-gradients"></a>Sfumature lineari orizzontali

L'esempio seguente usa un pennello sfumato lineare orizzontale per riempire una linea, un'ellisse e un rettangolo:


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // opaque red
   Color(255, 0, 0, 255));  // opaque blue

Pen pen(&linGrBrush);

graphics.DrawLine(&pen, 0, 10, 200, 10);
graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



Il [**costruttore LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) riceve quattro argomenti: due punti e due colori. Il primo punto (0, 10) è associato al primo colore (rosso) e il secondo punto (200, 10) è associato al secondo colore (blu). Come previsto, la linea disegnata da (0, 10) a (200, 10) cambia gradualmente da rosso a blu.

I 10 punti (50, 10) e (200, 10) non sono importanti. L'aspetto importante è che i due punti hanno la stessa seconda coordinata: la linea che li collega è orizzontale. Anche l'ellisse e il rettangolo cambiano gradualmente da rosso a blu, man mano che la coordinata orizzontale va da 0 a 200.

La figura seguente mostra la linea, l'ellisse e il rettangolo. Si noti che la sfumatura di colore si ripete quando la coordinata orizzontale aumenta oltre 200.

![illustrazione che mostra una sfumatura orizzontale che riempie una linea e un'ellisse e un rettangolo più lungo dell'ellisse](images/lineargradient1.png)

## <a name="customizing-linear-gradients"></a>Personalizzazione delle sfumature lineari

Nell'esempio precedente i componenti di colore cambiano in modo lineare quando si passa da una coordinata orizzontale di 0 a una coordinata orizzontale di 200. Ad esempio, un punto la cui prima coordinata è compresa tra 0 e 200 avrà un componente blu compreso tra 0 e 255.

GDI+ consente di regolare il modo in cui un colore varia da un bordo di una sfumatura all'altro. Si supponga di voler creare un pennello sfumato che cambia da nero a rosso in base alla tabella seguente.



| Coordinata orizzontale | Componenti RGB |
|-----------------------|----------------|
| 0                     | (0, 0, 0)      |
| 40                    | (128, 0, 0)    |
| 200                   | (255, 0, 0)    |



 

Si noti che il componente rosso è a metà intensità quando la coordinata orizzontale è solo il 20% della strada da 0 a 200.

L'esempio seguente chiama il [**metodo LinearGradientBrush::SetBlend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) di un [**oggetto LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) per associare tre intensità relative a tre posizioni relative. Come nella tabella precedente, un'intensità relativa di 0,5 è associata a una posizione relativa di 0,2. Il codice riempie un'ellisse e un rettangolo con il pennello sfumato.


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 0, 0, 0),     // opaque black 
   Color(255, 255, 0, 0));  // opaque red

REAL relativeIntensities[] = {0.0f, 0.5f, 1.0f};
REAL relativePositions[]   = {0.0f, 0.2f, 1.0f};

linGrBrush.SetBlend(relativeIntensities, relativePositions, 3);

graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



La figura seguente mostra l'ellisse e il rettangolo risultanti.

![illustrazione che mostra una sfumatura orizzontale che riempie un'ellisse e un rettangolo più lungo dell'ellisse](images/lineargradient2.png)

## <a name="diagonal-linear-gradients"></a>Sfumature lineari diagonali

Le sfumature negli esempi precedenti sono state orizzontali. ciò significa che il colore cambia gradualmente man mano che ci si sposta lungo qualsiasi linea orizzontale. È anche possibile definire sfumature verticali e sfumature diagonali. Il codice seguente passa i punti (0, 0) e (200, 100) a un [**costruttore LinearGradientBrush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) Il colore blu è associato a (0, 0) e il colore verde è associato a (200, 100). Una linea (con larghezza della penna 10) e un'ellisse vengono riempite con il pennello sfumato lineare.


```
LinearGradientBrush linGrBrush(
   Point(0, 0),
   Point(200, 100),
   Color(255, 0, 0, 255),   // opaque blue
   Color(255, 0, 255, 0));  // opaque green

Pen pen(&linGrBrush, 10);

graphics.DrawLine(&pen, 0, 0, 600, 300);
graphics.FillEllipse(&linGrBrush, 10, 100, 200, 100);
```



La figura seguente mostra la linea e i puntini di sospensione. Si noti che il colore nell'ellisse cambia gradualmente man mano che ci si sposta lungo qualsiasi linea parallela alla linea che passa attraverso (0, 0) e (200, 100).

![figura che mostra una sfumatura diagonale che riempie un'ellisse e una linea diagonale](images/lineargradient3.png)

 

 



