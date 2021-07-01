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
# <a name="types-of-coordinate-systems"></a><span data-ttu-id="72e86-103">Tipi di sistemi di coordinate</span><span class="sxs-lookup"><span data-stu-id="72e86-103">Types of Coordinate Systems</span></span>

<span data-ttu-id="72e86-104">GDI+ di Windows usa tre spazi delle coordinate: mondo, pagina e dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72e86-104">Windows GDI+ uses three coordinate spaces: world, page, and device.</span></span> <span data-ttu-id="72e86-105">Quando si effettua la chiamata, i punti passati al metodo `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` [**Graphics::D rawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) ( (0, 0) e (160, 80) sono nello spazio delle coordinate del mondo.</span><span class="sxs-lookup"><span data-stu-id="72e86-105">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, the points that you pass to the [**Graphics::DrawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) method — (0, 0) and (160, 80) — are in the world coordinate space.</span></span> <span data-ttu-id="72e86-106">Prima che GDI+ possa disegnare la linea sullo schermo, le coordinate passano attraverso una sequenza di trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="72e86-106">Before GDI+ can draw the line on the screen, the coordinates pass through a sequence of transformations.</span></span> <span data-ttu-id="72e86-107">Una trasformazione converte le coordinate del mondo in coordinate di pagina e un'altra trasformazione converte le coordinate della pagina in coordinate del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72e86-107">One transformation converts world coordinates to page coordinates, and another transformation converts page coordinates to device coordinates.</span></span>

<span data-ttu-id="72e86-108">Si supponga di voler usare un sistema di coordinate con origine nel corpo dell'area client anziché nell'angolo superiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="72e86-108">Suppose you want to work with a coordinate system that has its origin in the body of the client area rather than the upper-left corner.</span></span> <span data-ttu-id="72e86-109">Si supponga, ad esempio, che l'origine sia a 100 pixel dal bordo sinistro dell'area client e a 50 pixel dalla parte superiore dell'area client.</span><span class="sxs-lookup"><span data-stu-id="72e86-109">Say, for example, that you want the origin to be 100 pixels from the left edge of the client area and 50 pixels from the top of the client area.</span></span> <span data-ttu-id="72e86-110">Nella figura seguente viene illustrato un sistema di coordinate di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="72e86-110">The following illustration shows such a coordinate system.</span></span>

![Screenshot di una finestra contenente gli assi delle coordinate etichettati](images/aboutgdip05-art01.png)

<span data-ttu-id="72e86-112">Quando si effettua la chiamata `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , si ottiene la riga illustrata nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="72e86-112">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, you get the line shown in the following illustration.</span></span>

![Screenshot della finestra precedente, ma con una linea blu che si estende in diagonale dall'origine](images/aboutgdip05-art02.png)

<span data-ttu-id="72e86-114">Le coordinate degli endpoint della linea nei tre spazi delle coordinate sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="72e86-114">The coordinates of the endpoints of your line in the three coordinate spaces are as follows:</span></span>



| <span data-ttu-id="72e86-115">Space</span><span class="sxs-lookup"><span data-stu-id="72e86-115">Space</span></span>       |  <span data-ttu-id="72e86-116">Coordinate dell'endpoint</span><span class="sxs-lookup"><span data-stu-id="72e86-116">Endpoint coordinates</span></span>                       |
|--------|-------------------------|
| <span data-ttu-id="72e86-117">World</span><span class="sxs-lookup"><span data-stu-id="72e86-117">World</span></span>  | <span data-ttu-id="72e86-118">da (0, 0) a (160, 80)</span><span class="sxs-lookup"><span data-stu-id="72e86-118">(0, 0) to (160, 80)</span></span>     |
| <span data-ttu-id="72e86-119">Pagina</span><span class="sxs-lookup"><span data-stu-id="72e86-119">Page</span></span>   | <span data-ttu-id="72e86-120">da (100, 50) a (260, 130)</span><span class="sxs-lookup"><span data-stu-id="72e86-120">(100, 50) to (260, 130)</span></span> |
| <span data-ttu-id="72e86-121">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="72e86-121">Device</span></span> | <span data-ttu-id="72e86-122">da (100, 50) a (260, 130)</span><span class="sxs-lookup"><span data-stu-id="72e86-122">(100, 50) to (260, 130)</span></span> |



 

<span data-ttu-id="72e86-123">Si noti che lo spazio delle coordinate della pagina ha l'origine nell'angolo superiore sinistro dell'area client. questo sarà sempre il caso.</span><span class="sxs-lookup"><span data-stu-id="72e86-123">Note that the page coordinate space has its origin at the upper-left corner of the client area; this will always be the case.</span></span> <span data-ttu-id="72e86-124">Si noti anche che, poiché l'unità di misura è il pixel, le coordinate del dispositivo sono le stesse delle coordinate della pagina.</span><span class="sxs-lookup"><span data-stu-id="72e86-124">Also note that because the unit of measure is the pixel, the device coordinates are the same as the page coordinates.</span></span> <span data-ttu-id="72e86-125">Se si imposta l'unità di misura su un valore diverso dai pixel (ad esempio, pollici), le coordinate del dispositivo saranno diverse dalle coordinate della pagina.</span><span class="sxs-lookup"><span data-stu-id="72e86-125">If you set the unit of measure to something other than pixels (for example, inches), then the device coordinates will be different from the page coordinates.</span></span>

<span data-ttu-id="72e86-126">La trasformazione che esegue il mapping delle coordinate del mondo alle coordinate della pagina è detta *trasformazione globale* e viene gestita da un [**oggetto**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Graphics.</span><span class="sxs-lookup"><span data-stu-id="72e86-126">The transformation that maps world coordinates to page coordinates is called the *world transformation* and is maintained by a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="72e86-127">Nell'esempio precedente la trasformazione world è una traslazione di 100 unità nella direzione x e di 50 unità nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="72e86-127">In the previous example, the world transformation is a translation 100 units in the x direction and 50 units in the y direction.</span></span> <span data-ttu-id="72e86-128">L'esempio seguente imposta la trasformazione globale di un **oggetto Graphics** e quindi usa tale **oggetto Graphics** per disegnare la linea illustrata nella figura precedente.</span><span class="sxs-lookup"><span data-stu-id="72e86-128">The following example sets the world transformation of a **Graphics** object and then uses that **Graphics** object to draw the line shown in the previous figure.</span></span>


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



<span data-ttu-id="72e86-129">La trasformazione che esegue il mapping delle coordinate della pagina alle coordinate del dispositivo è detta *trasformazione di pagina*.</span><span class="sxs-lookup"><span data-stu-id="72e86-129">The transformation that maps page coordinates to device coordinates is called the *page transformation*.</span></span> <span data-ttu-id="72e86-130">La classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornisce quattro metodi per modificare e controllare la trasformazione della pagina: [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics::GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics::SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)e [**Graphics::GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale).</span><span class="sxs-lookup"><span data-stu-id="72e86-130">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides four methods for manipulating and inspecting the page transformation: [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics::GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics::SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale), and [**Graphics::GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale).</span></span> <span data-ttu-id="72e86-131">La **classe Graphics** fornisce anche due metodi, [**Graphics::GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) e [**Graphics::GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), per esaminare i punti orizzontali e verticali per pollice del dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="72e86-131">The **Graphics** class also provides two methods, [**Graphics::GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) and [**Graphics::GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), for examining the horizontal and vertical dots per inch of the display device.</span></span>

<span data-ttu-id="72e86-132">È possibile usare il [**metodo Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) della [**classe Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per specificare un'unità di misura.</span><span class="sxs-lookup"><span data-stu-id="72e86-132">You can use the [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to specify a unit of measure.</span></span> <span data-ttu-id="72e86-133">Nell'esempio seguente viene disegnata una linea da (0, 0) a (2, 1) dove il punto (2, 1) è 2 pollici a destra e 1 pollice verso il basso dal punto (0, 0).</span><span class="sxs-lookup"><span data-stu-id="72e86-133">The following example draws a line from (0, 0) to (2, 1) where the point (2, 1) is 2 inches to the right and 1 inch down from the point (0, 0).</span></span>


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> <span data-ttu-id="72e86-134">Se non si specifica lo spessore della penna quando si costruisce la penna, nell'esempio precedente verrà disegnata una linea larga un pollice.</span><span class="sxs-lookup"><span data-stu-id="72e86-134">If you don't specify a pen width when you construct your pen, the previous example will draw a line that is one inch wide.</span></span> <span data-ttu-id="72e86-135">È possibile specificare la larghezza della penna nel secondo argomento per il [**costruttore Pen:**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen)</span><span class="sxs-lookup"><span data-stu-id="72e86-135">You can specify the pen width in the second argument to the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) constructor:</span></span>
> <br/><br/>
> <span data-ttu-id="72e86-136">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span><span class="sxs-lookup"><span data-stu-id="72e86-136">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span></span>

 

<span data-ttu-id="72e86-137">Se si presuppone che il dispositivo di visualizzazione abbia 96 punti per pollice nella direzione orizzontale e 96 punti per pollice nella direzione verticale, gli endpoint della linea nell'esempio precedente hanno le coordinate seguenti nei tre spazi delle coordinate:</span><span class="sxs-lookup"><span data-stu-id="72e86-137">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



| <span data-ttu-id="72e86-138">Space</span><span class="sxs-lookup"><span data-stu-id="72e86-138">Space</span></span>       | <span data-ttu-id="72e86-139">Coordinate dell'endpoint</span><span class="sxs-lookup"><span data-stu-id="72e86-139">Endpoint coordinates</span></span>                    |
|--------|---------------------|
| <span data-ttu-id="72e86-140">World</span><span class="sxs-lookup"><span data-stu-id="72e86-140">World</span></span>  | <span data-ttu-id="72e86-141">(0, 0) a (2, 1)</span><span class="sxs-lookup"><span data-stu-id="72e86-141">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="72e86-142">Pagina</span><span class="sxs-lookup"><span data-stu-id="72e86-142">Page</span></span>   | <span data-ttu-id="72e86-143">(0, 0) a (2, 1)</span><span class="sxs-lookup"><span data-stu-id="72e86-143">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="72e86-144">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="72e86-144">Device</span></span> | <span data-ttu-id="72e86-145">(da 0, 0 a (192, 96)</span><span class="sxs-lookup"><span data-stu-id="72e86-145">(0, 0, to (192, 96)</span></span> |



 

<span data-ttu-id="72e86-146">È possibile combinare il mondo e le trasformazioni di pagina per ottenere un'ampia gamma di effetti.</span><span class="sxs-lookup"><span data-stu-id="72e86-146">You can combine the world and page transformations to achieve a variety of effects.</span></span> <span data-ttu-id="72e86-147">Si supponga, ad esempio, di voler usare pollici come unità di misura e che l'origine del sistema di coordinate sia a 2 pollici dal bordo sinistro dell'area client e a 1/2 pollice dalla parte superiore dell'area client.</span><span class="sxs-lookup"><span data-stu-id="72e86-147">For example, suppose you want to use inches as the unit of measure and you want the origin of your coordinate system to be 2 inches from the left edge of the client area and 1/2 inch from the top of the client area.</span></span> <span data-ttu-id="72e86-148">L'esempio seguente imposta le trasformazioni world e page di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e quindi disegna una linea da (0, 0) a (2, 1).</span><span class="sxs-lookup"><span data-stu-id="72e86-148">The following example sets the world and page transformations of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and then draws a line from (0, 0) to (2, 1).</span></span>


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



<span data-ttu-id="72e86-149">La figura seguente mostra la linea e il sistema di coordinate.</span><span class="sxs-lookup"><span data-stu-id="72e86-149">The following illustration shows the line and coordinate system.</span></span>

![Screenshot della finestra precedente, ma più ampia, con gli assi posizionati a sinistra e etichettati in modo diverso](images/aboutgdip05-art03.png)

<span data-ttu-id="72e86-151">Se si presuppone che il dispositivo di visualizzazione abbia 96 punti per pollice nella direzione orizzontale e 96 punti per pollice nella direzione verticale, gli endpoint della linea nell'esempio precedente hanno le coordinate seguenti nei tre spazi delle coordinate:</span><span class="sxs-lookup"><span data-stu-id="72e86-151">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



| <span data-ttu-id="72e86-152">Space</span><span class="sxs-lookup"><span data-stu-id="72e86-152">Space</span></span>       | <span data-ttu-id="72e86-153">Coordinate dell'endpoint</span><span class="sxs-lookup"><span data-stu-id="72e86-153">Endpoint coordinates</span></span>                        |
|--------|-------------------------|
| <span data-ttu-id="72e86-154">World</span><span class="sxs-lookup"><span data-stu-id="72e86-154">World</span></span>  | <span data-ttu-id="72e86-155">(0, 0) a (2, 1)</span><span class="sxs-lookup"><span data-stu-id="72e86-155">(0, 0) to (2, 1)</span></span>        |
| <span data-ttu-id="72e86-156">Pagina</span><span class="sxs-lookup"><span data-stu-id="72e86-156">Page</span></span>   | <span data-ttu-id="72e86-157">da (2, 0,5) a (4, 1,5)</span><span class="sxs-lookup"><span data-stu-id="72e86-157">(2, 0.5) to (4, 1.5)</span></span>    |
| <span data-ttu-id="72e86-158">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="72e86-158">Device</span></span> | <span data-ttu-id="72e86-159">(192, 48) a (384, 144)</span><span class="sxs-lookup"><span data-stu-id="72e86-159">(192, 48) to (384, 144)</span></span> |



 

 

 
