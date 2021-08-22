---
description: Un singolo oggetto Matrix può archiviare una singola trasformazione o una sequenza di trasformazioni.
ms.assetid: 1dc68ff8-6b17-4934-82da-ab2fc612aafa
title: Importanza dell'ordine delle trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8a7c0c840fa5c2debaccef4450c525bab8cf7f6e4373653eadaf53a6538891
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359581"
---
# <a name="why-transformation-order-is-significant"></a>Importanza dell'ordine delle trasformazioni

Un singolo [**oggetto Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) può archiviare una singola trasformazione o una sequenza di trasformazioni. Quest'ultima è denominata *trasformazione composita*.   La matrice di una trasformazione composita viene ottenuta moltiplicando le matrici delle singole trasformazioni.

In una trasformazione composita, l'ordine delle singole trasformazioni è importante. Ad esempio, se si ruota prima, quindi si ridimensiona, quindi si trasla, si ottiene un risultato diverso rispetto a quello che si ottiene prima traslando, quindi ruotando e quindi ridimensionando. In Windows GDI+, le trasformazioni composite vengono compilate da sinistra a destra. Se S, R e T sono rispettivamente matrici di scala, rotazione e traslazione, il prodotto SRT (in quell'ordine) è la matrice della trasformazione composita che prima ridimensiona, quindi ruota e quindi trasla. La matrice prodotta dal prodotto SRT è diversa dalla matrice prodotta dal prodotto TRS.

Un motivo significativo è che le trasformazioni come la rotazione e la scalabilità vengono eseguite rispetto all'origine del sistema di coordinate. Il ridimensionamento di un oggetto centrato nell'origine produce un risultato diverso rispetto al ridimensionamento di un oggetto spostato dall'origine. Analogamente, la rotazione di un oggetto centrato in corrispondenza dell'origine produce un risultato diverso rispetto alla rotazione di un oggetto spostato dall'origine.

L'esempio seguente combina ridimensionamento, rotazione e traslazione (in questo ordine) per formare una trasformazione composita. [L'argomento ****MatrixOrderAppend*** passato](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) al metodo [**Graphics::RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) specifica che la rotazione seguirà il ridimensionamento. Analogamente, l'argomento [****MatrixOrderAppend***](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passato al metodo [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) specifica che la traslazione seguirà la rotazione.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.TranslateTransform(150.0f, 150.0f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



Nell'esempio seguente vengono effettuate le stesse chiamate al metodo dell'esempio precedente, ma l'ordine delle chiamate viene invertito. L'ordine delle operazioni risultante viene prima traslato, quindi ruotato, quindi ridimensionato, che produce un risultato molto diverso rispetto alla prima scala, quindi ruota, quindi trasla:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



Un modo per invertire l'ordine delle singole trasformazioni in una trasformazione composita è invertire l'ordine di una sequenza di chiamate al metodo. Un secondo modo per controllare l'ordine delle operazioni è modificare l'argomento dell'ordine della matrice. L'esempio seguente è lo stesso dell'esempio precedente, ad eccezione del fatto che [***MatrixOrderAppend*** è](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) stato modificato in [****MatrixOrderPrepend****.](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) La moltiplicazione della matrice viene eseguita nell'ordine SRT, dove S, R e T sono rispettivamente le matrici per scalare, ruotare e traslare. L'ordine della trasformazione composita è prima ridimensionare, quindi ruotare e quindi traslare.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f,MatrixOrderPrepend);
graphics.RotateTransform(28.0f, MatrixOrderPrepend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderPrepend);
graphics.DrawRectangle(&pen, rect);
```



Il risultato dell'esempio precedente è lo stesso risultato ottenuto nel primo esempio di questa sezione. Questo perché è stato invertito sia l'ordine delle chiamate al metodo che l'ordine della moltiplicazione della matrice.

 

 



