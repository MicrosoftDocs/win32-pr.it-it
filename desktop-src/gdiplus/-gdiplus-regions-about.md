---
description: Un'area è una parte della superficie di visualizzazione.
ms.assetid: eb78d7a0-6293-487f-88c5-88ba455b965f
title: Aree geografiche (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd15a7a25b341556b312c540f6fa4caf870da75aa4973be1d7c1e8102511e6ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885018"
---
# <a name="regions-gdi"></a>Aree geografiche (GDI+)

Un'area è una parte della superficie di visualizzazione. Le aree possono essere semplici (un singolo rettangolo) o complesse (una combinazione di poligoni e curve chiuse). La figura seguente mostra due aree: una costruita da un rettangolo e l'altra costruita da un percorso.

![Figura che mostra un'area rettangolare trasparente sovrapposta a una forma curva opaca](images/aboutgdip02-art27.png)

Le aree vengono spesso usate per il ritaglio e l'hit testing. Il ritaglio comporta la limitazione del disegno a una determinata area dello schermo, in genere la parte dello schermo che deve essere aggiornata. L'hit testing prevede il controllo per verificare se il cursore si trova in una determinata area dello schermo quando viene premuto un pulsante del mouse.

È possibile costruire un'area da un rettangolo o da un percorso. È anche possibile creare aree complesse combinando aree esistenti. La [**classe Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) fornisce i metodi seguenti per combinare aree: [Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstregion)), [Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstregion)), [Xor](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)), [Exclude](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion))e [**Region::Complement**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-complement(inconstgraphicspath)).

L'intersezione di due aree è il set di tutti i punti appartenenti a entrambe le aree. L'unione è il set di tutti i punti appartenenti a una o all'altra o a entrambe le aree. Il complemento di un'area è il set di tutti i punti non presenti nell'area. La figura seguente mostra l'intersezione e l'unione delle due aree nella figura precedente.

![figura che mostra l'intersezione delle aree nella figura precedente e la relativa intersezione](images/aboutgdip02-art28.png)

Il [metodo Xor,](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)) applicato a una coppia di aree, produce un'area che contiene tutti i punti che appartengono a un'area o all'altra, ma non a entrambi. Il [metodo Exclude,](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion)) applicato a una coppia di aree, produce un'area che contiene tutti i punti nella prima area non presenti nella seconda area. La figura seguente illustra le aree risultanti dall'applicazione dei metodi Xor ed Exclude alle due aree illustrate all'inizio di questo argomento.

![figura che mostra le parti in una delle due aree, ma non in entrambe, e la parte del rettangolo che non si sovrappone all'area curva](images/aboutgdip02-art29.png)

Per riempire un'area, sono necessari un [**oggetto Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) un [**oggetto Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) e un [**oggetto Region.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) **L'oggetto Graphics** fornisce il [**metodo Graphics::FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion) e l'oggetto **Brush** archivia gli attributi del riempimento, ad esempio il colore o il motivo. L'esempio seguente riempie un'area con un colore a tinta unita.


```
myGraphics.FillRegion(&mySolidBrush, &myRegion);
```



 

 
