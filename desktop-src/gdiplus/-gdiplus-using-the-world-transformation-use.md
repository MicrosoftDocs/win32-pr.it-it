---
description: La trasformazione globale è una proprietà della classe Graphics.
ms.assetid: 22f43b29-ea7b-4faf-9795-2242bf704ed3
title: Utilizzo della trasformazione di tipo World
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2138df1bbd2be6d3329695fc6898da49da93b3b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226060"
---
# <a name="using-the-world-transformation"></a>Utilizzo della trasformazione di tipo World

La trasformazione globale è una proprietà della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . I numeri che specificano la trasformazione globale vengono archiviati in un oggetto [**matrice**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) , che rappresenta una matrice 3 × 3. Le classi **Matrix** e **Graphics** hanno diversi metodi per impostare i numeri nella matrice di trasformazione mondiale. Gli esempi in questa sezione modificano i rettangoli perché i rettangoli sono facili da creare ed è facile vedere gli effetti delle trasformazioni sui rettangoli.

Per iniziare, si crea un rettangolo 50 per 50 e lo si individua all'origine (0,0). L'origine si trova nell'angolo superiore sinistro dell'area client.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.DrawRectangle(&pen, rect);
```



Il codice seguente applica una trasformazione di ridimensionamento che espande il rettangolo per un fattore di 1,75 nella direzione x e compatta il rettangolo per un fattore di 0,5 nella direzione y:


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



Per tradurre il rettangolo, usare il codice seguente:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.DrawRectangle(&pen, rect);
```



 

 



