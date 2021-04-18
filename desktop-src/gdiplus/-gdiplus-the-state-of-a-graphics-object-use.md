---
description: La classe Graphics è il nucleo di Windows GDI+. Per creare qualsiasi elemento, è necessario creare un oggetto graphics, impostarne le proprietà e chiamarne i metodi (DrawLine, DrawImage, DrawString e like).
ms.assetid: 7d70f9fe-c0b2-4d65-815d-483d06df96ad
title: Stato di un oggetto Graphics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661733f944b08633b5df84eed3ac488e612d9e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550413"
---
# <a name="the-state-of-a-graphics-object"></a><span data-ttu-id="a18cb-104">Stato di un oggetto Graphics</span><span class="sxs-lookup"><span data-stu-id="a18cb-104">The State of a Graphics Object</span></span>

<span data-ttu-id="a18cb-105">La classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) è il nucleo di Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="a18cb-105">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is at the heart of Windows GDI+.</span></span> <span data-ttu-id="a18cb-106">Per creare qualsiasi elemento, è necessario creare un oggetto **Graphics** , impostarne le proprietà e chiamarne i metodi ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))e like).</span><span class="sxs-lookup"><span data-stu-id="a18cb-106">To draw anything, you create a **Graphics** object, set its properties, and call its methods ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)), and the like).</span></span>

<span data-ttu-id="a18cb-107">L'esempio seguente crea un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , quindi chiama il metodo [**Graphics::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) dell'oggetto **Graphics** :</span><span class="sxs-lookup"><span data-stu-id="a18cb-107">The following example constructs a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object and then calls the [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) method of the **Graphics** object:</span></span>


```
HDC          hdc;
PAINTSTRUCT  ps;

hdc = BeginPaint(hWnd, &ps);
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));  // opaque blue
   graphics.DrawRectangle(&pen, 10, 10, 200, 100);
}
EndPaint(hWnd, &ps);
```



<span data-ttu-id="a18cb-108">Nel codice precedente, il metodo [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) restituisce un handle a un contesto di dispositivo e tale handle viene passato al costruttore [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="a18cb-108">In the preceding code, the [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) method returns a handle to a device context, and that handle is passed to the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="a18cb-109">Un contesto di dispositivo è una struttura (gestita da Windows) che include informazioni sul dispositivo di visualizzazione specifico usato.</span><span class="sxs-lookup"><span data-stu-id="a18cb-109">A device context is a structure (maintained by Windows) that holds information about the particular display device being used.</span></span>

## <a name="graphics-state"></a><span data-ttu-id="a18cb-110">Stato grafica</span><span class="sxs-lookup"><span data-stu-id="a18cb-110">Graphics State</span></span>

<span data-ttu-id="a18cb-111">Un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) non fornisce metodi di disegno, ad esempio [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) e [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)).</span><span class="sxs-lookup"><span data-stu-id="a18cb-111">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object does more than provide drawing methods, such as [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) and [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)).</span></span> <span data-ttu-id="a18cb-112">Un oggetto **Graphics** gestisce anche lo stato della grafica, che può essere suddiviso nelle categorie seguenti:</span><span class="sxs-lookup"><span data-stu-id="a18cb-112">A **Graphics** object also maintains graphics state, which can be divided into the following categories:</span></span>

-   <span data-ttu-id="a18cb-113">Collegamento a un contesto di dispositivo</span><span class="sxs-lookup"><span data-stu-id="a18cb-113">A link to a device context</span></span>
-   <span data-ttu-id="a18cb-114">Impostazioni qualità</span><span class="sxs-lookup"><span data-stu-id="a18cb-114">Quality settings</span></span>
-   <span data-ttu-id="a18cb-115">Trasformazioni</span><span class="sxs-lookup"><span data-stu-id="a18cb-115">Transformations</span></span>
-   <span data-ttu-id="a18cb-116">Area di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="a18cb-116">A clipping region</span></span>

### <a name="device-context"></a><span data-ttu-id="a18cb-117">Contesto di dispositivo</span><span class="sxs-lookup"><span data-stu-id="a18cb-117">Device Context</span></span>

<span data-ttu-id="a18cb-118">In qualità di programmatore di applicazioni, non è necessario pensare all'interazione tra un oggetto [**grafico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e il relativo contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a18cb-118">As an application programmer, you don't have to think about the interaction between a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and its device context.</span></span> <span data-ttu-id="a18cb-119">Questa interazione viene gestita da GDI+ dietro le quinte.</span><span class="sxs-lookup"><span data-stu-id="a18cb-119">This interaction is handled by GDI+ behind the scenes.</span></span>

### <a name="quality-settings"></a><span data-ttu-id="a18cb-120">Impostazioni qualità</span><span class="sxs-lookup"><span data-stu-id="a18cb-120">Quality Settings</span></span>

<span data-ttu-id="a18cb-121">Un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) dispone di diverse proprietà che influiscono sulla qualità degli elementi disegnati sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="a18cb-121">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object has several properties that influence the quality of the items that are drawn on the screen.</span></span> <span data-ttu-id="a18cb-122">Per visualizzare e modificare queste proprietà, è possibile chiamare i metodi get e set.</span><span class="sxs-lookup"><span data-stu-id="a18cb-122">You can view and manipulate these properties by calling get and set methods.</span></span> <span data-ttu-id="a18cb-123">Ad esempio, è possibile chiamare il metodo [**Graphics:: SetTextRenderingHint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) per specificare il tipo di anti-aliasing, se presente, applicato al testo.</span><span class="sxs-lookup"><span data-stu-id="a18cb-123">For example, you can call the [**Graphics::SetTextRenderingHint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) method to specify the type of antialiasing (if any) applied to text.</span></span> <span data-ttu-id="a18cb-124">Altri metodi set che influenzano la qualità sono [**Graphics:: SetSmoothingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics:: SetCompositingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics:: SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality)e [**Graphics:: SetInterpolationMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).</span><span class="sxs-lookup"><span data-stu-id="a18cb-124">Other set methods that influence quality are [**Graphics::SetSmoothingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics::SetCompositingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality), and [**Graphics::SetInterpolationMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).</span></span>

<span data-ttu-id="a18cb-125">Nell'esempio seguente vengono disegnati due ellissi, uno con la modalità di smussatura impostata su [\* \* \* \* SmoothingModeAntiAlias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) \* \* e uno con la modalità di smussatura impostata su [\* \* \* \* SmoothingModeHighSpeed \* \* \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode):</span><span class="sxs-lookup"><span data-stu-id="a18cb-125">The following example draws two ellipses, one with the smoothing mode set to [\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) and one with the smoothing mode set to [\*\*\*\*SmoothingModeHighSpeed\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode):</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 0, 255, 0));  // opaque green

graphics.SetSmoothingMode(SmoothingModeAntiAlias);
graphics.DrawEllipse(&pen, 0, 0, 200, 100);
graphics.SetSmoothingMode(SmoothingModeHighSpeed);
graphics.DrawEllipse(&pen, 0, 150, 200, 100);
```



### <a name="transformations"></a><span data-ttu-id="a18cb-126">Trasformazioni</span><span class="sxs-lookup"><span data-stu-id="a18cb-126">Transformations</span></span>

<span data-ttu-id="a18cb-127">Un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) gestisce due trasformazioni (mondo e pagina) che vengono applicate a tutti gli elementi disegnati da tale oggetto **grafico** .</span><span class="sxs-lookup"><span data-stu-id="a18cb-127">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object maintains two transformations (world and page) that are applied to all items drawn by that **Graphics** object.</span></span> <span data-ttu-id="a18cb-128">Qualsiasi trasformazione affine può essere archiviata nella trasformazione globale.</span><span class="sxs-lookup"><span data-stu-id="a18cb-128">Any affine transformation can be stored in the world transformation.</span></span> <span data-ttu-id="a18cb-129">Le trasformazioni affini includono il ridimensionamento, la rotazione, la reflection, la distorsione e la conversione.</span><span class="sxs-lookup"><span data-stu-id="a18cb-129">Affine transformations include scaling, rotating, reflecting, skewing, and translating.</span></span> <span data-ttu-id="a18cb-130">La trasformazione pagina può essere utilizzata per la scalabilità e per la modifica delle unità, ad esempio da pixel a pollici.</span><span class="sxs-lookup"><span data-stu-id="a18cb-130">The page transformation can be used for scaling and for changing units (for example, pixels to inches).</span></span> <span data-ttu-id="a18cb-131">Per ulteriori informazioni sulle trasformazioni, vedere [sistemi di coordinate e trasformazioni](-gdiplus-coordinate-systems-and-transformations-about.md).</span><span class="sxs-lookup"><span data-stu-id="a18cb-131">For more information on transformations, see [Coordinate Systems and Transformations](-gdiplus-coordinate-systems-and-transformations-about.md).</span></span>

<span data-ttu-id="a18cb-132">Nell'esempio seguente vengono impostate le trasformazioni globali e di pagina di un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="a18cb-132">The following example sets the world and page transformations of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="a18cb-133">La trasformazione globale è impostata su una rotazione di 30 gradi.</span><span class="sxs-lookup"><span data-stu-id="a18cb-133">The world transformation is set to a 30-degree rotation.</span></span> <span data-ttu-id="a18cb-134">La trasformazione pagina viene impostata in modo che le coordinate passate alla seconda [**grafica::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) verranno considerate millimetri anziché pixel.</span><span class="sxs-lookup"><span data-stu-id="a18cb-134">The page transformation is set so that the coordinates passed to the second [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) will be treated as millimeters instead of pixels.</span></span> <span data-ttu-id="a18cb-135">Il codice effettua due chiamate identiche all'oggetto **Graphics::D Metodo rawellipse** .</span><span class="sxs-lookup"><span data-stu-id="a18cb-135">The code makes two identical calls to the **Graphics::DrawEllipse** method.</span></span> <span data-ttu-id="a18cb-136">La trasformazione globale viene applicata alla prima **grafica::D chiamata rawellipse** e entrambe le trasformazioni (mondo e pagina) vengono applicate alla seconda **grafica::D chiamata rawellipse** .</span><span class="sxs-lookup"><span data-stu-id="a18cb-136">The world transformation is applied to the first **Graphics::DrawEllipse** call, and both transformations (world and page) are applied to the second **Graphics::DrawEllipse** call.</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0));

graphics.ResetTransform();
graphics.RotateTransform(30.0f);            // World transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
graphics.SetPageUnit(UnitMillimeter);       // Page transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
```



<span data-ttu-id="a18cb-137">Nella figura seguente sono illustrati i due ellissi.</span><span class="sxs-lookup"><span data-stu-id="a18cb-137">The following illustration shows the two ellipses.</span></span> <span data-ttu-id="a18cb-138">Si noti che la rotazione di 30 gradi riguarda l'origine del sistema di coordinate (angolo superiore sinistro dell'area client), non dei centri dei puntini di sospensione.</span><span class="sxs-lookup"><span data-stu-id="a18cb-138">Note that the 30-degree rotation is about the origin of the coordinate system (upper-left corner of the client area), not about the centers of the ellipses.</span></span> <span data-ttu-id="a18cb-139">Si noti inoltre che la larghezza della penna di 1 indica 1 pixel per la prima ellisse e 1 millimetro per la seconda ellisse.</span><span class="sxs-lookup"><span data-stu-id="a18cb-139">Also note that the pen width of 1 means 1 pixel for the first ellipse and 1 millimeter for the second ellipse.</span></span>

![Screenshot di una finestra contenente una piccola ellisse, un'ellisse sottile e un'ellisse grande e più spessa](images/graphicsascon1.png)

 

### <a name="clipping-region"></a><span data-ttu-id="a18cb-141">Area di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="a18cb-141">Clipping Region</span></span>

<span data-ttu-id="a18cb-142">Un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) mantiene un'area di ridimensionamento che si applica a tutti gli elementi disegnati da tale oggetto **grafico** .</span><span class="sxs-lookup"><span data-stu-id="a18cb-142">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object maintains a clipping region that applies to all items drawn by that **Graphics** object.</span></span> <span data-ttu-id="a18cb-143">È possibile impostare l'area di ridimensionamento chiamando il metodo [seclip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) .</span><span class="sxs-lookup"><span data-stu-id="a18cb-143">You can set the clipping region by calling the [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) method.</span></span>

<span data-ttu-id="a18cb-144">Nell'esempio seguente viene creata un'area con più forme formando l'Unione di due rettangoli.</span><span class="sxs-lookup"><span data-stu-id="a18cb-144">The following example creates a plus-shaped region by forming the union of two rectangles.</span></span> <span data-ttu-id="a18cb-145">Tale area viene designata come area di visualizzazione di un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="a18cb-145">That region is designated as the clipping region of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="a18cb-146">Il codice disegna quindi due righe limitate all'interno dell'area di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="a18cb-146">Then the code draws two lines that are restricted to the interior of the clipping region.</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0), 5);  // opaque red, width 5
SolidBrush brush(Color(255, 180, 255, 255));  // opaque aqua

// Create a plus-shaped region by forming the union of two rectangles.
Region region(Rect(50, 0, 50, 150));
region.Union(Rect(0, 50, 150, 50));
graphics.FillRegion(&brush, &region);

// Set the clipping region.
graphics.SetClip(&region);

// Draw two clipped lines.
graphics.DrawLine(&pen, 0, 30, 150, 160);
graphics.DrawLine(&pen, 40, 20, 190, 150);
```



<span data-ttu-id="a18cb-147">Nella figura seguente sono illustrate le linee ritagliate.</span><span class="sxs-lookup"><span data-stu-id="a18cb-147">The following illustration shows the clipped lines.</span></span>

![illustrazione che mostra una forma colorata incrociata da due linee rosse diagonali](images/graphicsascon2.png)

 

 
