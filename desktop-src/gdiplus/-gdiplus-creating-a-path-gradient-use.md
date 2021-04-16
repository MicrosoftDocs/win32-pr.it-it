---
description: La classe PathGradientBrush consente di personalizzare la modalità di riempimento di una forma con colori a modifica graduale.
ms.assetid: f6a8085c-3d6a-494f-a1ee-5fa96efb1aae
title: Creazione di una sfumatura del percorso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ef39793547b1485525f8cf1fd5b344773e7a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568247"
---
# <a name="creating-a-path-gradient"></a><span data-ttu-id="8cc28-103">Creazione di una sfumatura del percorso</span><span class="sxs-lookup"><span data-stu-id="8cc28-103">Creating a Path Gradient</span></span>

<span data-ttu-id="8cc28-104">La classe [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) consente di personalizzare la modalità di riempimento di una forma con colori a modifica graduale.</span><span class="sxs-lookup"><span data-stu-id="8cc28-104">The [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) class allows you to customize the way you fill a shape with gradually changing colors.</span></span> <span data-ttu-id="8cc28-105">Un oggetto **PathGradientBrush** ha un percorso limite e un punto centrale.</span><span class="sxs-lookup"><span data-stu-id="8cc28-105">A **PathGradientBrush** object has a boundary path and a center point.</span></span> <span data-ttu-id="8cc28-106">È possibile specificare un colore per il punto centrale e un altro colore per il limite.</span><span class="sxs-lookup"><span data-stu-id="8cc28-106">You can specify one color for the center point and another color for the boundary.</span></span> <span data-ttu-id="8cc28-107">È anche possibile specificare colori distinti per ognuno dei diversi punti lungo il limite.</span><span class="sxs-lookup"><span data-stu-id="8cc28-107">You can also specify separate colors for each of several points along the boundary.</span></span>

> [!Note]  
> <span data-ttu-id="8cc28-108">In GDI+ un percorso è una sequenza di linee e curve gestite da un oggetto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="8cc28-108">In GDI+, a path is a sequence of lines and curves maintained by a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="8cc28-109">Per ulteriori informazioni sui percorsi GDI+, vedere [percorsi](-gdiplus-paths-about.md) e [costruzione e](-gdiplus-constructing-and-drawing-paths-use.md)creazione di percorsi.</span><span class="sxs-lookup"><span data-stu-id="8cc28-109">For more information about GDI+ paths, see [Paths](-gdiplus-paths-about.md) and [Constructing and Drawing Paths](-gdiplus-constructing-and-drawing-paths-use.md).</span></span>

 

<span data-ttu-id="8cc28-110">Nell'esempio seguente viene riempita un'ellisse con un pennello sfumatura del percorso.</span><span class="sxs-lookup"><span data-stu-id="8cc28-110">The following example fills an ellipse with a path gradient brush.</span></span> <span data-ttu-id="8cc28-111">Il colore centrale è impostato su blu e il colore limite è impostato su Aqua.</span><span class="sxs-lookup"><span data-stu-id="8cc28-111">The center color is set to blue and the boundary color is set to aqua.</span></span>


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 140, 70);

// Use the path to construct a brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to blue.
pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

// Set the color along the entire boundary of the path to aqua.
Color colors[] = {Color(255, 0, 255, 255)};
int count = 1;
pthGrBrush.SetSurroundColors(colors, &count);

graphics.FillEllipse(&pthGrBrush, 0, 0, 140, 70);
```



<span data-ttu-id="8cc28-112">Nell'illustrazione seguente viene mostrata l'ellisse piena.</span><span class="sxs-lookup"><span data-stu-id="8cc28-112">The following illustration shows the filled ellipse.</span></span>

![illustrazione che mostra un'ellisse con riempimento sfumato](images/pathgradient1.png)

<span data-ttu-id="8cc28-114">Per impostazione predefinita, un pennello sfumatura del percorso non si estende al di fuori del limite del percorso.</span><span class="sxs-lookup"><span data-stu-id="8cc28-114">By default, a path gradient brush does not extend outside the boundary of the path.</span></span> <span data-ttu-id="8cc28-115">Se si utilizza il pennello sfumatura percorso per riempire una forma che si estende oltre il limite del tracciato, l'area della schermata all'esterno del percorso non verrà compilata.</span><span class="sxs-lookup"><span data-stu-id="8cc28-115">If you use the path gradient brush to fill a shape that extends beyond the boundary of the path, the area of the screen outside the path will not be filled.</span></span> <span data-ttu-id="8cc28-116">La figura seguente mostra cosa accade se si modifica la chiamata [**Graphics:: FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) nel codice precedente a `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)` .</span><span class="sxs-lookup"><span data-stu-id="8cc28-116">The following illustration shows what happens if you change the [**Graphics::FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) call in the preceding code to `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)`.</span></span>

![illustrazione che mostra una sezione orizzontale dell'ellisse precedente](images/pathgradient2.png)

## <a name="specifying-points-on-the-boundary"></a><span data-ttu-id="8cc28-118">Specifica di punti sul limite</span><span class="sxs-lookup"><span data-stu-id="8cc28-118">Specifying Points on the Boundary</span></span>

<span data-ttu-id="8cc28-119">Nell'esempio seguente viene creato un pennello sfumatura tracciato da un percorso a forma di stella.</span><span class="sxs-lookup"><span data-stu-id="8cc28-119">The following example constructs a path gradient brush from a star-shaped path.</span></span> <span data-ttu-id="8cc28-120">Il codice chiama il metodo [**PathGradientBrush:: SetCenterColor**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) per impostare il colore al centro della stella su rosso.</span><span class="sxs-lookup"><span data-stu-id="8cc28-120">The code calls the [**PathGradientBrush::SetCenterColor**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) method to set the color at the centroid of the star to red.</span></span> <span data-ttu-id="8cc28-121">Il codice chiama quindi il metodo [**PathGradientBrush:: SetSurroundColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) per specificare vari colori (archiviati nella matrice [**Colors**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) ) nei singoli punti della matrice [**Points**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="8cc28-121">Then the code calls the [**PathGradientBrush::SetSurroundColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) method to specify various colors (stored in the [**colors**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) array) at the individual points in the [**points**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) array.</span></span> <span data-ttu-id="8cc28-122">L'istruzione del codice finale riempie il tracciato a forma di stella con il pennello sfumatura del percorso.</span><span class="sxs-lookup"><span data-stu-id="8cc28-122">The final code statement fills the star-shaped path with the path gradient brush.</span></span>


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0),    Point(100, 50), 
                  Point(150, 50),  Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150),   Point(37, 75), 
                  Point(0, 50),    Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
```



<span data-ttu-id="8cc28-123">La figura seguente mostra la stella piena.</span><span class="sxs-lookup"><span data-stu-id="8cc28-123">The following illustration shows the filled star.</span></span>

![illustrazione che mostra una stella a cinque punte che si riempie dal rosso al centro fino a vari colori in ogni punto della stella](images/pathgradient3.png)

<span data-ttu-id="8cc28-125">Nell'esempio seguente viene costruito un pennello sfumatura del percorso basato su una matrice di punti.</span><span class="sxs-lookup"><span data-stu-id="8cc28-125">The following example constructs a path gradient brush based on an array of points.</span></span> <span data-ttu-id="8cc28-126">Un colore viene assegnato a ognuno dei cinque punti della matrice.</span><span class="sxs-lookup"><span data-stu-id="8cc28-126">A color is assigned to each of the five points in the array.</span></span> <span data-ttu-id="8cc28-127">Se fosse necessario connettere i cinque punti per linee rette, si otterrebbe un poligono a cinque lati.</span><span class="sxs-lookup"><span data-stu-id="8cc28-127">If you were to connect the five points by straight lines, you would get a five-sided polygon.</span></span> <span data-ttu-id="8cc28-128">Un colore viene assegnato anche al centro (baricentro) del poligono, in questo esempio il centro (80, 75) è impostato su bianco.</span><span class="sxs-lookup"><span data-stu-id="8cc28-128">A color is also assigned to the center (centroid) of that polygon — in this example, the center (80, 75) is set to white.</span></span> <span data-ttu-id="8cc28-129">L'istruzione final code nell'esempio riempie un rettangolo con il pennello sfumatura del percorso.</span><span class="sxs-lookup"><span data-stu-id="8cc28-129">The final code statement in the example fills a rectangle with the path gradient brush.</span></span>

<span data-ttu-id="8cc28-130">Il colore utilizzato per riempire il rettangolo è bianco in corrispondenza di (80, 75) e viene modificato gradualmente man mano che si allontana (80, 75) verso i punti nella matrice.</span><span class="sxs-lookup"><span data-stu-id="8cc28-130">The color used to fill the rectangle is white at (80, 75) and changes gradually as you move away from (80, 75) toward the points in the array.</span></span> <span data-ttu-id="8cc28-131">Ad esempio, quando si passa da (80, 75) a (0, 0), il colore cambia gradualmente da bianco a rosso e quando si passa da (80, 75) a (160, 0), il colore cambia gradualmente dal bianco al verde.</span><span class="sxs-lookup"><span data-stu-id="8cc28-131">For example, as you move from (80, 75) to (0, 0), the color changes gradually from white to red, and as you move from (80, 75) to (160, 0), the color changes gradually from white to green.</span></span>


```
// Construct a path gradient brush based on an array of points.
PointF ptsF[] = {PointF(0.0f, 0.0f), 
                 PointF(160.0f, 0.0f), 
                 PointF(160.0f, 200.0f),
                 PointF(80.0f, 150.0f),
                 PointF(0.0f, 200.0f)};

PathGradientBrush pBrush(ptsF, 5);

// An array of five points was used to construct the path gradient
// brush. Set the color of each point in that array.
Color colors[] = {Color(255, 255, 0, 0),  // (0, 0) red
                  Color(255, 0, 255, 0),  // (160, 0) green
                  Color(255, 0, 255, 0),  // (160, 200) green
                  Color(255, 0, 0, 255),  // (80, 150) blue
                  Color(255, 255, 0, 0)}; // (0, 200) red

int count = 5;
pBrush.SetSurroundColors(colors, &count);

// Set the center color to white.
pBrush.SetCenterColor(Color(255, 255, 255, 255));

// Use the path gradient brush to fill a rectangle.
graphics.FillRectangle(&pBrush, Rect(0, 0, 180, 220));
```



<span data-ttu-id="8cc28-132">Si noti che nel codice precedente non è presente alcun oggetto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="8cc28-132">Note that there is no [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object in the preceding code.</span></span> <span data-ttu-id="8cc28-133">Il costruttore [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) particolare nell'esempio riceve un puntatore a una matrice di punti, ma non richiede un oggetto **GraphicsPath** .</span><span class="sxs-lookup"><span data-stu-id="8cc28-133">The particular [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) constructor in the example receives a pointer to an array of points but does not require a **GraphicsPath** object.</span></span> <span data-ttu-id="8cc28-134">Si noti inoltre che il pennello sfumatura del percorso viene utilizzato per riempire un rettangolo, non un percorso.</span><span class="sxs-lookup"><span data-stu-id="8cc28-134">Also, note that the path gradient brush is used to fill a rectangle, not a path.</span></span> <span data-ttu-id="8cc28-135">Il rettangolo è più grande del percorso utilizzato per definire il pennello, quindi parte del rettangolo non viene disegnata dal pennello.</span><span class="sxs-lookup"><span data-stu-id="8cc28-135">The rectangle is larger than the path used to define the brush, so some of the rectangle is not painted by the brush.</span></span> <span data-ttu-id="8cc28-136">Nella figura seguente viene illustrato il rettangolo (linea tratteggiata) e la parte del rettangolo disegnata dal pennello sfumatura del percorso.</span><span class="sxs-lookup"><span data-stu-id="8cc28-136">The following illustration shows the rectangle (dotted line) and the portion of the rectangle painted by the path gradient brush.</span></span>

![illustrazione che mostra un rettangolo delimitato da una linea tratteggiata, parzialmente disegnata da una sfumatura multicolore](images/gradient4.png)

## <a name="customizing-a-path-gradient"></a><span data-ttu-id="8cc28-138">Personalizzazione di una sfumatura di tracciato</span><span class="sxs-lookup"><span data-stu-id="8cc28-138">Customizing a Path Gradient</span></span>

<span data-ttu-id="8cc28-139">Un modo per personalizzare un pennello sfumatura del tracciato consiste nell'impostare le scale dello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="8cc28-139">One way to customize a path gradient brush is to set its focus scales.</span></span> <span data-ttu-id="8cc28-140">Le scale dello stato attivo specificano un percorso interno che si trova all'interno del percorso principale.</span><span class="sxs-lookup"><span data-stu-id="8cc28-140">The focus scales specify an inner path that lies inside the main path.</span></span> <span data-ttu-id="8cc28-141">Il colore centrale viene visualizzato ovunque all'interno del percorso interno anziché solo al punto centrale.</span><span class="sxs-lookup"><span data-stu-id="8cc28-141">The center color is displayed everywhere inside that inner path rather than only at the center point.</span></span> <span data-ttu-id="8cc28-142">Per impostare le scale dello stato attivo di un pennello sfumatura del tracciato, chiamare il metodo [**PathGradientBrush:: SetFocusScales**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) .</span><span class="sxs-lookup"><span data-stu-id="8cc28-142">To set the focus scales of a path gradient brush, call the [**PathGradientBrush::SetFocusScales**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) method.</span></span>

<span data-ttu-id="8cc28-143">Nell'esempio seguente viene creato un pennello sfumatura del percorso basato su un percorso ellittico.</span><span class="sxs-lookup"><span data-stu-id="8cc28-143">The following example creates a path gradient brush based on an elliptical path.</span></span> <span data-ttu-id="8cc28-144">Il codice imposta il colore limite su blu, imposta il colore centrale su Aqua, quindi usa il pennello sfumatura tracciato per riempire il percorso ellittico.</span><span class="sxs-lookup"><span data-stu-id="8cc28-144">The code sets the boundary color to blue, sets the center color to aqua, and then uses the path gradient brush to fill the elliptical path.</span></span>

<span data-ttu-id="8cc28-145">Il codice imposta quindi le scale dello stato attivo del pennello sfumatura del percorso.</span><span class="sxs-lookup"><span data-stu-id="8cc28-145">Next the code sets the focus scales of the path gradient brush.</span></span> <span data-ttu-id="8cc28-146">La scala dello stato attivo x è impostata su 0,3 e la scala dello stato attivo y è impostata su 0,8.</span><span class="sxs-lookup"><span data-stu-id="8cc28-146">The x focus scale is set to 0.3, and the y focus scale is set to 0.8.</span></span> <span data-ttu-id="8cc28-147">Il codice chiama il metodo [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in modo che la chiamata successiva a [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) riempia un'ellisse che si trova a destra della prima ellisse.</span><span class="sxs-lookup"><span data-stu-id="8cc28-147">The code calls the [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object so that the subsequent call to [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) fills an ellipse that sits to the right of the first ellipse.</span></span>

<span data-ttu-id="8cc28-148">Per visualizzare l'effetto delle scale di messa a fuoco, Immaginate una piccola ellisse che condivide il centro con l'ellisse principale.</span><span class="sxs-lookup"><span data-stu-id="8cc28-148">To see the effect of the focus scales, imagine a small ellipse that shares its center with the main ellipse.</span></span> <span data-ttu-id="8cc28-149">L'ellisse (interna) di piccole dimensioni è l'ellisse principale ridimensionata orizzontalmente (attorno al centro) per un fattore di 0,3 e verticalmente in base a un fattore di 0,8.</span><span class="sxs-lookup"><span data-stu-id="8cc28-149">The small (inner) ellipse is the main ellipse scaled (about its center) horizontally by a factor of 0.3 and vertically by a factor of 0.8.</span></span> <span data-ttu-id="8cc28-150">Quando si passa dal limite dell'ellisse esterna al limite dell'ellisse interna, il colore passa gradualmente da blu a Aqua.</span><span class="sxs-lookup"><span data-stu-id="8cc28-150">As you move from the boundary of the outer ellipse to the boundary of the inner ellipse, the color changes gradually from blue to aqua.</span></span> <span data-ttu-id="8cc28-151">Quando si passa dal limite dell'ellisse interna al centro condiviso, il colore rimane Aqua.</span><span class="sxs-lookup"><span data-stu-id="8cc28-151">As you move from the boundary of the inner ellipse to the shared center, the color remains aqua.</span></span>


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 200, 100);

// Create a path gradient brush based on the elliptical path.
PathGradientBrush pthGrBrush(&path);
pthGrBrush.SetGammaCorrection(TRUE);

// Set the color along the entire boundary to blue.
Color color(Color(255, 0, 0, 255));
INT num = 1;
pthGrBrush.SetSurroundColors(&color, &num);

// Set the center color to aqua.
pthGrBrush.SetCenterColor(Color(255, 0, 255, 255));
 
// Use the path gradient brush to fill the ellipse. 
graphics.FillPath(&pthGrBrush, &path);

// Set the focus scales for the path gradient brush.
pthGrBrush.SetFocusScales(0.3f, 0.8f);

// Use the path gradient brush to fill the ellipse again.
// Show this filled ellipse to the right of the first filled ellipse.
graphics.TranslateTransform(220.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



<span data-ttu-id="8cc28-152">Nella figura seguente viene illustrato l'output del codice precedente.</span><span class="sxs-lookup"><span data-stu-id="8cc28-152">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="8cc28-153">L'ellisse a sinistra è Aqua solo al punto centrale.</span><span class="sxs-lookup"><span data-stu-id="8cc28-153">The ellipse on the left is aqua only at the center point.</span></span> <span data-ttu-id="8cc28-154">L'ellisse a destra è Aqua ovunque all'interno del percorso interno.</span><span class="sxs-lookup"><span data-stu-id="8cc28-154">The ellipse on the right is aqua everywhere inside the inner path.</span></span>

![illustrazione che mostra due ellissi che ombreggiano da Aqua a blu: la prima è molto piccola. il secondo è molto più](images/focusscales1.png)

<span data-ttu-id="8cc28-156">Un altro modo per personalizzare un pennello sfumatura del tracciato consiste nel specificare una matrice di colori preimpostati e una matrice di posizioni di interpolazione.</span><span class="sxs-lookup"><span data-stu-id="8cc28-156">Another way to customize a path gradient brush is to specify an array of preset colors and an array of interpolation positions.</span></span>

<span data-ttu-id="8cc28-157">Nell'esempio seguente viene creato un pennello sfumatura del percorso basato su un triangolo.</span><span class="sxs-lookup"><span data-stu-id="8cc28-157">The following example creates a path gradient brush based on a triangle.</span></span> <span data-ttu-id="8cc28-158">Il codice chiama il metodo [**PathGradientBrush:: SetInterpolationColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) del pennello sfumatura del percorso per specificare una matrice di colori di interpolazione (verde scuro, Aqua, blu) e una matrice di posizioni di interpolazione (0, 0,25, 1).</span><span class="sxs-lookup"><span data-stu-id="8cc28-158">The code calls the [**PathGradientBrush::SetInterpolationColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) method of the path gradient brush to specify an array of interpolation colors (dark green, aqua, blue) and an array of interpolation positions (0, 0.25, 1).</span></span> <span data-ttu-id="8cc28-159">Quando si passa dal limite del triangolo al punto centrale, il colore cambia gradualmente da verde scuro a Aqua e quindi da Aqua a blu.</span><span class="sxs-lookup"><span data-stu-id="8cc28-159">As you move from the boundary of the triangle to the center point, the color changes gradually from dark green to aqua and then from aqua to blue.</span></span> <span data-ttu-id="8cc28-160">Il passaggio da verde scuro a Aqua avviene nel 25% della distanza dal verde scuro al blu.</span><span class="sxs-lookup"><span data-stu-id="8cc28-160">The change from dark green to aqua happens in 25 percent of the distance from dark green to blue.</span></span>


```
// Vertices of the triangle
Point points[] = {Point(100, 0), 
                  Point(200, 200), 
                  Point(0, 200)};

// No GraphicsPath object is created. The PathGradient
// brush is constructed directly from the array of points.
PathGradientBrush pthGrBrush(points, 3);

Color presetColors[] = {
   Color(255, 0, 128, 0),    // Dark green
   Color(255, 0, 255, 255),  // Aqua
   Color(255, 0, 0, 255)};   // Blue

REAL interpPositions[] = {
   0.0f,   // Dark green is at the boundary of the triangle.
   0.25f,  // Aqua is 25 percent of the way from the boundary
           // to the center point.
   1.0f};  // Blue is at the center point.
                  
pthGrBrush.SetInterpolationColors(presetColors, interpPositions, 3);

// Fill a rectangle that is larger than the triangle
// specified in the Point array. The portion of the
// rectangle outside the triangle will not be painted.
graphics.FillRectangle(&pthGrBrush, 0, 0, 200, 200);
```



<span data-ttu-id="8cc28-161">Nella figura seguente viene illustrato l'output del codice precedente.</span><span class="sxs-lookup"><span data-stu-id="8cc28-161">The following illustration shows the output of the preceding code.</span></span>

![illustrazione che mostra un triangolo che sfuma da blu al centro, a Aqua, in verde ai bordi](images/pathgradient4.png)

## <a name="setting-the-center-point"></a><span data-ttu-id="8cc28-163">Impostazione del punto centrale</span><span class="sxs-lookup"><span data-stu-id="8cc28-163">Setting the Center Point</span></span>

<span data-ttu-id="8cc28-164">Per impostazione predefinita, il punto centrale di un pennello sfumatura del tracciato si trova al centro del tracciato usato per costruire il pennello.</span><span class="sxs-lookup"><span data-stu-id="8cc28-164">By default, the center point of a path gradient brush is at the centroid of the path used to construct the brush.</span></span> <span data-ttu-id="8cc28-165">È possibile modificare la posizione del punto centrale chiamando il metodo [**PathGradientBrush:: SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) della classe [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="8cc28-165">You can change the location of the center point by calling the [**PathGradientBrush::SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) method of the [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) class.</span></span>

<span data-ttu-id="8cc28-166">Nell'esempio seguente viene creato un pennello sfumatura del percorso basato su un'ellisse.</span><span class="sxs-lookup"><span data-stu-id="8cc28-166">The following example creates a path gradient brush based on an ellipse.</span></span> <span data-ttu-id="8cc28-167">Il centro dell'ellisse si trova in (70, 35), ma il punto centrale del pennello sfumatura del tracciato è impostato su (120, 40).</span><span class="sxs-lookup"><span data-stu-id="8cc28-167">The center of the ellipse is at (70, 35), but the center point of the path gradient brush is set to (120, 40).</span></span>


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 140, 70);

// Use the path to construct a brush.
PathGradientBrush pthGrBrush(&path);

// Set the center point to a location that is not the centroid of the path.
pthGrBrush.SetCenterPoint(Point(120, 40));

// Set the color at the center point to blue.
pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

// Set the color along the entire boundary of the path to aqua.
Color colors[] = {Color(255, 0, 255, 255)};
int count = 1;
pthGrBrush.SetSurroundColors(colors, &count);

graphics.FillEllipse(&pthGrBrush, 0, 0, 140, 70);
```



<span data-ttu-id="8cc28-168">Nella figura seguente vengono illustrati l'ellisse piena e il punto centrale del pennello sfumatura del percorso.</span><span class="sxs-lookup"><span data-stu-id="8cc28-168">The following illustration shows the filled ellipse and the center point of the path gradient brush.</span></span>

![illustrazione che mostra un'ellisse che riempie da blu a Aqua da un punto centrale vicino a un'estremità](images/pathgradient5.png)

<span data-ttu-id="8cc28-170">È possibile impostare il punto centrale di un pennello sfumatura tracciato su una posizione esterna al percorso utilizzato per costruire il pennello.</span><span class="sxs-lookup"><span data-stu-id="8cc28-170">You can set the center point of a path gradient brush to a location outside the path that was used to construct the brush.</span></span> <span data-ttu-id="8cc28-171">Nel codice precedente, se si sostituisce la chiamata a [**PathGradientBrush:: SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) con `pthGrBrush.SetCenterPoint(Point(145, 35))` , si otterrà il risultato seguente.</span><span class="sxs-lookup"><span data-stu-id="8cc28-171">In the preceding code, if you replace the call to [**PathGradientBrush::SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) with `pthGrBrush.SetCenterPoint(Point(145, 35))`, you will get the following result.</span></span>

![illustrazione che mostra un'ellisse riempita da rosso a giallo da un punto centrale esterno al bordo dell'ellisse](images/pathgradient6.png)

<span data-ttu-id="8cc28-173">Nell'illustrazione precedente, i punti all'estrema destra dell'ellisse non sono puri blu (anche se sono molto vicini).</span><span class="sxs-lookup"><span data-stu-id="8cc28-173">In the preceding illustration, the points at the far right of the ellipse are not pure blue (although they are very close).</span></span> <span data-ttu-id="8cc28-174">I colori della sfumatura sono posizionati come se il riempimento avesse avuto la possibilità di raggiungere il punto (145, 35), il colore avrebbe raggiunto il blu puro (0, 0, 255).</span><span class="sxs-lookup"><span data-stu-id="8cc28-174">The colors in the gradient are positioned as if the fill had been allowed to reach the point (145, 35), the color would have reached pure blue (0, 0, 255).</span></span> <span data-ttu-id="8cc28-175">Tuttavia, il riempimento non raggiunge mai (145, 35) perché un pennello sfumatura del percorso disegna solo all'interno del percorso.</span><span class="sxs-lookup"><span data-stu-id="8cc28-175">But the fill never reaches (145, 35) because a path gradient brush paints only inside its path.</span></span>

 

 
