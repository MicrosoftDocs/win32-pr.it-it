---
description: 'GDI+ di Windows usa tre spazi delle coordinate: mondo, pagina e dispositivo.'
ms.assetid: eb20f5e9-25f5-4f27-8ea5-83f6819425ed
title: Tipi di sistemi di coordinate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e259f43d4fc0d6a74021f3a6125f85652f51ac95
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120626"
---
# <a name="types-of-coordinate-systems"></a>Tipi di sistemi di coordinate

GDI+ di Windows usa tre spazi delle coordinate: mondo, pagina e dispositivo. Quando si effettua la chiamata, i punti passati al metodo `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` [**Graphics::D rawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) ( (0, 0) e (160, 80) sono nello spazio delle coordinate del mondo. Prima che GDI+ possa disegnare la linea sullo schermo, le coordinate passano attraverso una sequenza di trasformazioni. Una trasformazione converte le coordinate del mondo in coordinate di pagina e un'altra trasformazione converte le coordinate della pagina in coordinate del dispositivo.

Si supponga di voler usare un sistema di coordinate con origine nel corpo dell'area client anziché nell'angolo superiore sinistro. Si supponga, ad esempio, che l'origine sia a 100 pixel dal bordo sinistro dell'area client e a 50 pixel dalla parte superiore dell'area client. Nella figura seguente viene illustrato un sistema di coordinate di questo tipo.

![Screenshot di una finestra contenente gli assi delle coordinate etichettati](images/aboutgdip05-art01.png)

Quando si effettua la chiamata `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , si ottiene la riga illustrata nella figura seguente.

![Screenshot della finestra precedente, ma con una linea blu che si estende in diagonale dall'origine](images/aboutgdip05-art02.png)

Le coordinate degli endpoint della linea nei tre spazi delle coordinate sono le seguenti:



| Space       |  Coordinate dell'endpoint                       |
|--------|-------------------------|
| World  | da (0, 0) a (160, 80)     |
| Pagina   | da (100, 50) a (260, 130) |
| Dispositivo | da (100, 50) a (260, 130) |



 

Si noti che lo spazio delle coordinate della pagina ha l'origine nell'angolo superiore sinistro dell'area client. questo sarà sempre il caso. Si noti anche che, poiché l'unità di misura è il pixel, le coordinate del dispositivo sono le stesse delle coordinate della pagina. Se si imposta l'unità di misura su un valore diverso dai pixel (ad esempio, pollici), le coordinate del dispositivo saranno diverse dalle coordinate della pagina.

La trasformazione che esegue il mapping delle coordinate del mondo alle coordinate della pagina è detta *trasformazione globale* e viene gestita da un [**oggetto**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Graphics. Nell'esempio precedente la trasformazione world è una traslazione di 100 unità nella direzione x e di 50 unità nella direzione y. L'esempio seguente imposta la trasformazione globale di un **oggetto Graphics** e quindi usa tale **oggetto Graphics** per disegnare la linea illustrata nella figura precedente.


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



La trasformazione che esegue il mapping delle coordinate della pagina alle coordinate del dispositivo è detta *trasformazione di pagina*. La classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornisce quattro metodi per modificare e controllare la trasformazione della pagina: [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics::GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics::SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)e [**Graphics::GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale). La **classe Graphics** fornisce anche due metodi, [**Graphics::GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) e [**Graphics::GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), per esaminare i punti orizzontali e verticali per pollice del dispositivo di visualizzazione.

È possibile usare il [**metodo Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) della [**classe Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per specificare un'unità di misura. Nell'esempio seguente viene disegnata una linea da (0, 0) a (2, 1) dove il punto (2, 1) è 2 pollici a destra e 1 pollice verso il basso dal punto (0, 0).


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> Se non si specifica lo spessore della penna quando si costruisce la penna, nell'esempio precedente verrà disegnata una linea larga un pollice. È possibile specificare la larghezza della penna nel secondo argomento per il [**costruttore Pen:**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen)
> <br/><br/>
> `Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.

 

Se si presuppone che il dispositivo di visualizzazione abbia 96 punti per pollice nella direzione orizzontale e 96 punti per pollice nella direzione verticale, gli endpoint della linea nell'esempio precedente hanno le coordinate seguenti nei tre spazi delle coordinate:



| Space       | Coordinate dell'endpoint                    |
|--------|---------------------|
| World  | (0, 0) a (2, 1)    |
| Pagina   | (0, 0) a (2, 1)    |
| Dispositivo | (da 0, 0 a (192, 96) |



 

È possibile combinare il mondo e le trasformazioni di pagina per ottenere un'ampia gamma di effetti. Si supponga, ad esempio, di voler usare pollici come unità di misura e che l'origine del sistema di coordinate sia a 2 pollici dal bordo sinistro dell'area client e a 1/2 pollice dalla parte superiore dell'area client. L'esempio seguente imposta le trasformazioni world e page di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e quindi disegna una linea da (0, 0) a (2, 1).


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



La figura seguente mostra la linea e il sistema di coordinate.

![Screenshot della finestra precedente, ma più ampia, con gli assi posizionati a sinistra e etichettati in modo diverso](images/aboutgdip05-art03.png)

Se si presuppone che il dispositivo di visualizzazione abbia 96 punti per pollice nella direzione orizzontale e 96 punti per pollice nella direzione verticale, gli endpoint della linea nell'esempio precedente hanno le coordinate seguenti nei tre spazi delle coordinate:



| Space       | Coordinate dell'endpoint                        |
|--------|-------------------------|
| World  | (0, 0) a (2, 1)        |
| Pagina   | da (2, 0,5) a (4, 1,5)    |
| Dispositivo | (192, 48) a (384, 144) |



 

 

 
