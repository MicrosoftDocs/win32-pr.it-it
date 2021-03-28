---
description: Un'area è una parte della superficie di visualizzazione.
ms.assetid: eb78d7a0-6293-487f-88c5-88ba455b965f
title: Aree geografiche (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d6a7f0a5a6d3df4b11a491111dbedf9e155c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551374"
---
# <a name="regions-gdi"></a>Aree geografiche (GDI+)

Un'area è una parte della superficie di visualizzazione. Le aree possono essere semplici (un solo rettangolo) o complesse (una combinazione di poligoni e curve chiuse). Nella figura seguente sono illustrate due aree: una costruita da un rettangolo e l'altra costruita da un percorso.

![illustrazione che mostra un'area rettangolare trasparente sovrapposta a una forma curva opaca](images/aboutgdip02-art27.png)

Le aree vengono spesso usate per il ritaglio e l'hit testing. Il ritaglio implica la limitazione del disegno a una determinata area dello schermo, in genere la parte della schermata che deve essere aggiornata. L'hit testing prevede il controllo per verificare se il cursore si trova in una determinata area dello schermo quando viene premuto un pulsante del mouse.

È possibile costruire un'area da un rettangolo o da un percorso. È anche possibile creare aree complesse combinando le aree esistenti. La classe [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) fornisce i metodi seguenti per combinare le aree [: Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstregion)), [Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstregion)), [Xor](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)), [Exclude](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion))e [**Region:: complemento**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-complement(inconstgraphicspath)).

L'intersezione di due aree è il set di tutti i punti appartenenti a entrambe le aree. L'Unione è il set di tutti i punti che appartengono a una o all'altra o a entrambe le aree. Il complemento di un'area è il set di tutti i punti che non sono presenti nell'area. Nella figura seguente vengono illustrate l'intersezione e l'Unione delle due aree nella figura precedente.

![illustrazione che mostra l'intersezione delle aree nell'illustrazione precedente e la relativa intersezione](images/aboutgdip02-art28.png)

Il metodo [Xor](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)) , applicato a una coppia di aree, produce un'area che contiene tutti i punti che appartengono a un'area o l'altra, ma non entrambi. Il metodo [Exclude](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion)) , applicato a una coppia di aree, produce un'area che contiene tutti i punti della prima area che non si trovano nella seconda area. Nella figura seguente sono illustrate le aree risultanti dall'applicazione dei metodi Xor ed Exclude alle due aree illustrate all'inizio di questo argomento.

![illustrazione che mostra le parti in entrambe le aree, ma non entrambe, e la parte del rettangolo che non si sovrappone all'area curva](images/aboutgdip02-art29.png)

Per riempire un'area, sono necessari un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , un oggetto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) e un oggetto [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) . L'oggetto **Graphics** fornisce il metodo [**Graphics:: FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion) e l'oggetto **Brush** archivia gli attributi del riempimento, ad esempio il colore o il modello. Nell'esempio seguente viene riempita un'area con un colore a tinta unita.


```
myGraphics.FillRegion(&mySolidBrush, &myRegion);
```



 

 
