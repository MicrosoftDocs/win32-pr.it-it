---
description: 'Windows GDI+ utilizza tre spazi delle coordinate: mondo, pagina e dispositivo.'
ms.assetid: eb20f5e9-25f5-4f27-8ea5-83f6819425ed
title: Tipi di sistemi di coordinate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05908196662918eb93f4fa6e2b356a6989ed5a58
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104564172"
---
# <a name="types-of-coordinate-systems"></a>Tipi di sistemi di coordinate

Windows GDI+ utilizza tre spazi delle coordinate: mondo, pagina e dispositivo. Quando si effettua la chiamata `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , i punti passati alla [**grafica::D Metodo rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) (0, 0) e (160, 80) si trovano nello spazio delle coordinate internazionali. Prima che GDI+ possa creare la riga sullo schermo, le coordinate passano attraverso una sequenza di trasformazioni. Una trasformazione converte le coordinate internazionali in coordinate di pagina e un'altra trasformazione converte le coordinate di pagina in coordinate del dispositivo.

Si supponga di voler usare un sistema di coordinate con la relativa origine nel corpo dell'area client anziché nell'angolo superiore sinistro. Supponiamo, ad esempio, che si desideri che l'origine sia 100 pixel dal bordo sinistro dell'area client e 50 pixel dalla parte superiore dell'area client. Nella figura seguente viene illustrato un sistema di coordinate di questo tipo.

![Screenshot di una finestra contenente gli assi delle coordinate con etichetta](images/aboutgdip05-art01.png)

Quando si effettua la chiamata `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , si ottiene la riga illustrata nella figura seguente.

![screenshot della finestra precedente, ma con una linea blu che si estende in senso diagonale dall'origine](images/aboutgdip05-art02.png)

Le coordinate degli endpoint della linea nei tre spazi delle coordinate sono le seguenti:



|        |                         |
|--------|-------------------------|
| World  | (0, 0) a (160, 80)     |
| Pagina   | (100, 50) a (260, 130) |
| Dispositivo | (100, 50) a (260, 130) |



 

Si noti che lo spazio delle coordinate della pagina ha origine nell'angolo superiore sinistro dell'area client. Questo sarà sempre il caso. Si noti inoltre che, poiché l'unità di misura è il pixel, le coordinate del dispositivo corrispondono alle coordinate della pagina. Se si imposta l'unità di misura su un valore diverso da pixel (ad esempio, pollici), le coordinate del dispositivo saranno diverse dalle coordinate della pagina.

La trasformazione che esegue il mapping delle coordinate internazionali alle coordinate di pagina viene chiamata *trasformazione globale* ed è gestita da un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Nell'esempio precedente, la trasformazione globale è una conversione di unità 100 nella direzione x e 50 unità nella direzione y. Nell'esempio seguente viene impostata la trasformazione globale di un oggetto **Graphics** , quindi viene utilizzato l'oggetto **Graphics** per creare la riga illustrata nella figura precedente.


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



La trasformazione che esegue il mapping delle coordinate della pagina alle coordinate del dispositivo è detta *trasformazione pagina*. La classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornisce quattro metodi per la modifica e il controllo della trasformazione di pagina [**: graphics:: SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics:: GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics:: SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)e [**Graphics:: GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale). La classe **Graphics** fornisce anche due metodi, [**Graphics:: GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) e [**Graphics:: GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), per esaminare i punti orizzontali e verticali per pollice del dispositivo di visualizzazione.

È possibile usare il metodo [**Graphics:: SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per specificare un'unità di misura. Nell'esempio seguente viene disegnata una riga da (0,0) a (2, 1) in cui il punto (2, 1) è di 2 centimetri a destra e 1 pollice verso il basso rispetto al punto (0, 0).


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> Se non si specifica una larghezza della penna quando si costruisce la penna, nell'esempio precedente verrà disegnato un valore di una linea di un pollice. È possibile specificare la larghezza della penna nel secondo argomento del costruttore [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) :
> <br/><br/>
> `Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.

 

Se si presuppone che il dispositivo di visualizzazione includa 96 punti per pollice nella direzione orizzontale e 96 punti per pollice nella direzione verticale, gli endpoint della riga nell'esempio precedente hanno le coordinate seguenti nei tre spazi delle coordinate:



|        |                     |
|--------|---------------------|
| World  | (0, 0) in (2, 1)    |
| Pagina   | (0, 0) in (2, 1)    |
| Dispositivo | (0, 0, a (192, 96) |



 

È possibile combinare le trasformazioni del mondo e della pagina per ottenere una varietà di effetti. Si supponga, ad esempio, di voler usare i pollici come unità di misura e che l'origine del sistema di coordinate sia 2 centimetri dal bordo sinistro dell'area client e 1/2 di pollice dalla parte superiore dell'area client. Nell'esempio seguente vengono impostate le trasformazioni globali e di pagina di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , quindi viene disegnata una riga da (0,0) a (2, 1).


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



Nella figura seguente viene illustrato il sistema di coordinate e linee.

![screenshot della finestra precedente, ma più ampio, con gli assi posizionati a sinistra ed etichettati in modo diverso](images/aboutgdip05-art03.png)

Se si presuppone che il dispositivo di visualizzazione includa 96 punti per pollice nella direzione orizzontale e 96 punti per pollice nella direzione verticale, gli endpoint della riga nell'esempio precedente hanno le coordinate seguenti nei tre spazi delle coordinate:



|        |                         |
|--------|-------------------------|
| World  | (0, 0) in (2, 1)        |
| Pagina   | (da 2 a 0,5) a (4, 1,5)    |
| Dispositivo | (192, 48) a (384, 144) |



 

 

 
