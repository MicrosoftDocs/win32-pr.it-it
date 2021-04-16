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
# <a name="types-of-coordinate-systems"></a><span data-ttu-id="f536a-103">Tipi di sistemi di coordinate</span><span class="sxs-lookup"><span data-stu-id="f536a-103">Types of Coordinate Systems</span></span>

<span data-ttu-id="f536a-104">Windows GDI+ utilizza tre spazi delle coordinate: mondo, pagina e dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f536a-104">Windows GDI+ uses three coordinate spaces: world, page, and device.</span></span> <span data-ttu-id="f536a-105">Quando si effettua la chiamata `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , i punti passati alla [**grafica::D Metodo rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) (0, 0) e (160, 80) si trovano nello spazio delle coordinate internazionali.</span><span class="sxs-lookup"><span data-stu-id="f536a-105">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, the points that you pass to the [**Graphics::DrawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) method — (0, 0) and (160, 80) — are in the world coordinate space.</span></span> <span data-ttu-id="f536a-106">Prima che GDI+ possa creare la riga sullo schermo, le coordinate passano attraverso una sequenza di trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="f536a-106">Before GDI+ can draw the line on the screen, the coordinates pass through a sequence of transformations.</span></span> <span data-ttu-id="f536a-107">Una trasformazione converte le coordinate internazionali in coordinate di pagina e un'altra trasformazione converte le coordinate di pagina in coordinate del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f536a-107">One transformation converts world coordinates to page coordinates, and another transformation converts page coordinates to device coordinates.</span></span>

<span data-ttu-id="f536a-108">Si supponga di voler usare un sistema di coordinate con la relativa origine nel corpo dell'area client anziché nell'angolo superiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="f536a-108">Suppose you want to work with a coordinate system that has its origin in the body of the client area rather than the upper-left corner.</span></span> <span data-ttu-id="f536a-109">Supponiamo, ad esempio, che si desideri che l'origine sia 100 pixel dal bordo sinistro dell'area client e 50 pixel dalla parte superiore dell'area client.</span><span class="sxs-lookup"><span data-stu-id="f536a-109">Say, for example, that you want the origin to be 100 pixels from the left edge of the client area and 50 pixels from the top of the client area.</span></span> <span data-ttu-id="f536a-110">Nella figura seguente viene illustrato un sistema di coordinate di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="f536a-110">The following illustration shows such a coordinate system.</span></span>

![Screenshot di una finestra contenente gli assi delle coordinate con etichetta](images/aboutgdip05-art01.png)

<span data-ttu-id="f536a-112">Quando si effettua la chiamata `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , si ottiene la riga illustrata nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="f536a-112">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, you get the line shown in the following illustration.</span></span>

![screenshot della finestra precedente, ma con una linea blu che si estende in senso diagonale dall'origine](images/aboutgdip05-art02.png)

<span data-ttu-id="f536a-114">Le coordinate degli endpoint della linea nei tre spazi delle coordinate sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="f536a-114">The coordinates of the endpoints of your line in the three coordinate spaces are as follows:</span></span>



|        |                         |
|--------|-------------------------|
| <span data-ttu-id="f536a-115">World</span><span class="sxs-lookup"><span data-stu-id="f536a-115">World</span></span>  | <span data-ttu-id="f536a-116">(0, 0) a (160, 80)</span><span class="sxs-lookup"><span data-stu-id="f536a-116">(0, 0) to (160, 80)</span></span>     |
| <span data-ttu-id="f536a-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="f536a-117">Page</span></span>   | <span data-ttu-id="f536a-118">(100, 50) a (260, 130)</span><span class="sxs-lookup"><span data-stu-id="f536a-118">(100, 50) to (260, 130)</span></span> |
| <span data-ttu-id="f536a-119">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="f536a-119">Device</span></span> | <span data-ttu-id="f536a-120">(100, 50) a (260, 130)</span><span class="sxs-lookup"><span data-stu-id="f536a-120">(100, 50) to (260, 130)</span></span> |



 

<span data-ttu-id="f536a-121">Si noti che lo spazio delle coordinate della pagina ha origine nell'angolo superiore sinistro dell'area client. Questo sarà sempre il caso.</span><span class="sxs-lookup"><span data-stu-id="f536a-121">Note that the page coordinate space has its origin at the upper-left corner of the client area; this will always be the case.</span></span> <span data-ttu-id="f536a-122">Si noti inoltre che, poiché l'unità di misura è il pixel, le coordinate del dispositivo corrispondono alle coordinate della pagina.</span><span class="sxs-lookup"><span data-stu-id="f536a-122">Also note that because the unit of measure is the pixel, the device coordinates are the same as the page coordinates.</span></span> <span data-ttu-id="f536a-123">Se si imposta l'unità di misura su un valore diverso da pixel (ad esempio, pollici), le coordinate del dispositivo saranno diverse dalle coordinate della pagina.</span><span class="sxs-lookup"><span data-stu-id="f536a-123">If you set the unit of measure to something other than pixels (for example, inches), then the device coordinates will be different from the page coordinates.</span></span>

<span data-ttu-id="f536a-124">La trasformazione che esegue il mapping delle coordinate internazionali alle coordinate di pagina viene chiamata *trasformazione globale* ed è gestita da un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="f536a-124">The transformation that maps world coordinates to page coordinates is called the *world transformation* and is maintained by a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="f536a-125">Nell'esempio precedente, la trasformazione globale è una conversione di unità 100 nella direzione x e 50 unità nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="f536a-125">In the previous example, the world transformation is a translation 100 units in the x direction and 50 units in the y direction.</span></span> <span data-ttu-id="f536a-126">Nell'esempio seguente viene impostata la trasformazione globale di un oggetto **Graphics** , quindi viene utilizzato l'oggetto **Graphics** per creare la riga illustrata nella figura precedente.</span><span class="sxs-lookup"><span data-stu-id="f536a-126">The following example sets the world transformation of a **Graphics** object and then uses that **Graphics** object to draw the line shown in the previous figure.</span></span>


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



<span data-ttu-id="f536a-127">La trasformazione che esegue il mapping delle coordinate della pagina alle coordinate del dispositivo è detta *trasformazione pagina*.</span><span class="sxs-lookup"><span data-stu-id="f536a-127">The transformation that maps page coordinates to device coordinates is called the *page transformation*.</span></span> <span data-ttu-id="f536a-128">La classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornisce quattro metodi per la modifica e il controllo della trasformazione di pagina [**: graphics:: SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics:: GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics:: SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)e [**Graphics:: GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale).</span><span class="sxs-lookup"><span data-stu-id="f536a-128">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides four methods for manipulating and inspecting the page transformation: [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics::GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics::SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale), and [**Graphics::GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale).</span></span> <span data-ttu-id="f536a-129">La classe **Graphics** fornisce anche due metodi, [**Graphics:: GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) e [**Graphics:: GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), per esaminare i punti orizzontali e verticali per pollice del dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f536a-129">The **Graphics** class also provides two methods, [**Graphics::GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) and [**Graphics::GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), for examining the horizontal and vertical dots per inch of the display device.</span></span>

<span data-ttu-id="f536a-130">È possibile usare il metodo [**Graphics:: SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per specificare un'unità di misura.</span><span class="sxs-lookup"><span data-stu-id="f536a-130">You can use the [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to specify a unit of measure.</span></span> <span data-ttu-id="f536a-131">Nell'esempio seguente viene disegnata una riga da (0,0) a (2, 1) in cui il punto (2, 1) è di 2 centimetri a destra e 1 pollice verso il basso rispetto al punto (0, 0).</span><span class="sxs-lookup"><span data-stu-id="f536a-131">The following example draws a line from (0, 0) to (2, 1) where the point (2, 1) is 2 inches to the right and 1 inch down from the point (0, 0).</span></span>


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> <span data-ttu-id="f536a-132">Se non si specifica una larghezza della penna quando si costruisce la penna, nell'esempio precedente verrà disegnato un valore di una linea di un pollice.</span><span class="sxs-lookup"><span data-stu-id="f536a-132">If you don't specify a pen width when you construct your pen, the previous example will draw a line that is one inch wide.</span></span> <span data-ttu-id="f536a-133">È possibile specificare la larghezza della penna nel secondo argomento del costruttore [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) :</span><span class="sxs-lookup"><span data-stu-id="f536a-133">You can specify the pen width in the second argument to the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) constructor:</span></span>
> <br/><br/>
> <span data-ttu-id="f536a-134">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span><span class="sxs-lookup"><span data-stu-id="f536a-134">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span></span>

 

<span data-ttu-id="f536a-135">Se si presuppone che il dispositivo di visualizzazione includa 96 punti per pollice nella direzione orizzontale e 96 punti per pollice nella direzione verticale, gli endpoint della riga nell'esempio precedente hanno le coordinate seguenti nei tre spazi delle coordinate:</span><span class="sxs-lookup"><span data-stu-id="f536a-135">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



|        |                     |
|--------|---------------------|
| <span data-ttu-id="f536a-136">World</span><span class="sxs-lookup"><span data-stu-id="f536a-136">World</span></span>  | <span data-ttu-id="f536a-137">(0, 0) in (2, 1)</span><span class="sxs-lookup"><span data-stu-id="f536a-137">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="f536a-138">Pagina</span><span class="sxs-lookup"><span data-stu-id="f536a-138">Page</span></span>   | <span data-ttu-id="f536a-139">(0, 0) in (2, 1)</span><span class="sxs-lookup"><span data-stu-id="f536a-139">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="f536a-140">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="f536a-140">Device</span></span> | <span data-ttu-id="f536a-141">(0, 0, a (192, 96)</span><span class="sxs-lookup"><span data-stu-id="f536a-141">(0, 0, to (192, 96)</span></span> |



 

<span data-ttu-id="f536a-142">È possibile combinare le trasformazioni del mondo e della pagina per ottenere una varietà di effetti.</span><span class="sxs-lookup"><span data-stu-id="f536a-142">You can combine the world and page transformations to achieve a variety of effects.</span></span> <span data-ttu-id="f536a-143">Si supponga, ad esempio, di voler usare i pollici come unità di misura e che l'origine del sistema di coordinate sia 2 centimetri dal bordo sinistro dell'area client e 1/2 di pollice dalla parte superiore dell'area client.</span><span class="sxs-lookup"><span data-stu-id="f536a-143">For example, suppose you want to use inches as the unit of measure and you want the origin of your coordinate system to be 2 inches from the left edge of the client area and 1/2 inch from the top of the client area.</span></span> <span data-ttu-id="f536a-144">Nell'esempio seguente vengono impostate le trasformazioni globali e di pagina di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , quindi viene disegnata una riga da (0,0) a (2, 1).</span><span class="sxs-lookup"><span data-stu-id="f536a-144">The following example sets the world and page transformations of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and then draws a line from (0, 0) to (2, 1).</span></span>


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



<span data-ttu-id="f536a-145">Nella figura seguente viene illustrato il sistema di coordinate e linee.</span><span class="sxs-lookup"><span data-stu-id="f536a-145">The following illustration shows the line and coordinate system.</span></span>

![screenshot della finestra precedente, ma più ampio, con gli assi posizionati a sinistra ed etichettati in modo diverso](images/aboutgdip05-art03.png)

<span data-ttu-id="f536a-147">Se si presuppone che il dispositivo di visualizzazione includa 96 punti per pollice nella direzione orizzontale e 96 punti per pollice nella direzione verticale, gli endpoint della riga nell'esempio precedente hanno le coordinate seguenti nei tre spazi delle coordinate:</span><span class="sxs-lookup"><span data-stu-id="f536a-147">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



|        |                         |
|--------|-------------------------|
| <span data-ttu-id="f536a-148">World</span><span class="sxs-lookup"><span data-stu-id="f536a-148">World</span></span>  | <span data-ttu-id="f536a-149">(0, 0) in (2, 1)</span><span class="sxs-lookup"><span data-stu-id="f536a-149">(0, 0) to (2, 1)</span></span>        |
| <span data-ttu-id="f536a-150">Pagina</span><span class="sxs-lookup"><span data-stu-id="f536a-150">Page</span></span>   | <span data-ttu-id="f536a-151">(da 2 a 0,5) a (4, 1,5)</span><span class="sxs-lookup"><span data-stu-id="f536a-151">(2, 0.5) to (4, 1.5)</span></span>    |
| <span data-ttu-id="f536a-152">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="f536a-152">Device</span></span> | <span data-ttu-id="f536a-153">(192, 48) a (384, 144)</span><span class="sxs-lookup"><span data-stu-id="f536a-153">(192, 48) to (384, 144)</span></span> |



 

 

 
