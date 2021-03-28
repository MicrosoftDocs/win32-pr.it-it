---
description: Un singolo oggetto Matrix può archiviare una singola trasformazione o una sequenza di trasformazioni.
ms.assetid: 1dc68ff8-6b17-4934-82da-ab2fc612aafa
title: Importanza dell'ordine delle trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7350d63456902ff47183faa08170b3b2fef481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977527"
---
# <a name="why-transformation-order-is-significant"></a>Importanza dell'ordine delle trasformazioni

Un singolo oggetto [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) può archiviare una singola trasformazione o una sequenza di trasformazioni. Quest'ultimo è denominato *trasformazione* *composita*.   La matrice di una trasformazione composita viene ottenuta moltiplicando le matrici delle singole trasformazioni.

In una trasformazione composita, l'ordine delle singole trasformazioni è importante. Se, ad esempio, si esegue prima la rotazione, quindi si esegue la scalabilità e si traduce, si ottiene un risultato diverso da quello in cui si esegue la prima conversione, quindi si ruota e quindi si ridimensiona. In Windows GDI+ le trasformazioni composite vengono compilate da sinistra a destra. Se S, R e T sono rispettivamente matrici di scala, rotazione e conversione, il prodotto SRT (in questo ordine) è la matrice della trasformazione composita che si ridimensiona prima di tutto, quindi ruota e quindi trasla. La matrice prodotta dal prodotto SRT è diversa dalla matrice prodotta dal prodotto TRS.

Un ordine è significativo perché le trasformazioni come la rotazione e la scalabilità vengono eseguite rispetto all'origine del sistema di coordinate. Il ridimensionamento di un oggetto centrato nell'origine produce un risultato diverso rispetto alla scalabilità di un oggetto che è stato rimosso dall'origine. Analogamente, la rotazione di un oggetto centrato nell'origine produce un risultato diverso rispetto alla rotazione di un oggetto che è stato rimosso dall'origine.

Nell'esempio seguente vengono combinate la scala, la rotazione e la conversione (in questo ordine) per formare una trasformazione composita. L'argomento [* * * * MatrixOrderAppend * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) * * * passato al metodo [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) specifica che la rotazione deve seguire la scala. Analogamente, l'argomento * * * * [MatrixOrderAppend * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) * * passato al metodo [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) specifica che la conversione seguirà la rotazione.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.TranslateTransform(150.0f, 150.0f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



Nell'esempio seguente vengono eseguite le stesse chiamate al metodo dell'esempio precedente, ma l'ordine delle chiamate viene invertito. L'ordine delle operazioni risultante viene innanzitutto convertito, quindi ruotato, quindi ridimensionato, che produce un risultato molto diverso dalla prima scala, quindi ruota e quindi trasla:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



Un modo per invertire l'ordine delle singole trasformazioni in una trasformazione composita consiste nell'invertire l'ordine di una sequenza di chiamate al metodo. Un secondo modo per controllare l'ordine delle operazioni consiste nel modificare l'argomento dell'ordine della matrice. L'esempio seguente è identico a quello dell'esempio precedente, ad eccezione del fatto che [* * * * MatrixOrderAppend * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) * * è stato modificato in * * * [* MatrixOrderPrepend * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder)* *. La moltiplicazione di matrici viene eseguita nell'ordine SRT, dove S, R e T sono rispettivamente le matrici per la scala, la rotazione e la conversione. L'ordine della trasformazione composita è la prima scala, quindi ruota e quindi trasla.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f,MatrixOrderPrepend);
graphics.RotateTransform(28.0f, MatrixOrderPrepend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderPrepend);
graphics.DrawRectangle(&pen, rect);
```



Il risultato dell'esempio precedente è lo stesso risultato ottenuto nel primo esempio di questa sezione. Questo è dovuto al fatto che è stato invertito sia l'ordine delle chiamate al metodo che l'ordine della moltiplicazione di matrici.

 

 



