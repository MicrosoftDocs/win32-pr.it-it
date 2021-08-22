---
description: La trasformazione globale è una proprietà della classe Graphics.
ms.assetid: 22f43b29-ea7b-4faf-9795-2242bf704ed3
title: Utilizzo della trasformazione di tipo World
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6288b5640e330a827e96b632541dac44e9463b87c566c16a94797810c4c92c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977241"
---
# <a name="using-the-world-transformation"></a>Utilizzo della trasformazione di tipo World

La trasformazione globale è una proprietà della [**classe Graphics.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) I numeri che specificano la trasformazione globale vengono archiviati in un [**oggetto Matrix,**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) che rappresenta una matrice di 3 ×3. Le **classi Matrix** e **Graphics** hanno diversi metodi per impostare i numeri nella matrice di trasformazione globale. Gli esempi in questa sezione modificano i rettangoli perché i rettangoli sono facili da disegnare ed è facile vedere gli effetti delle trasformazioni sui rettangoli.

Si inizia creando un rettangolo 50 per 50 e individuarlo all'origine (0, 0). L'origine si trova nell'angolo superiore sinistro dell'area client.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.DrawRectangle(&pen, rect);
```



Il codice seguente applica una trasformazione di ridimensionamento che espande il rettangolo di un fattore di 1,75 nella direzione x e riduce il rettangolo di un fattore di 0,5 nella direzione y:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.DrawRectangle(&pen, rect);
```



Il risultato è un rettangolo più lungo nella direzione x e più breve nella direzione y rispetto all'originale.

Per ruotare il rettangolo anziché ridimensionarlo, usare il codice seguente anziché il codice precedente:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.RotateTransform(28.0f);
graphics.DrawRectangle(&pen, rect);
```



Per traslare il rettangolo, usare il codice seguente:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.DrawRectangle(&pen, rect);
```



 

 



