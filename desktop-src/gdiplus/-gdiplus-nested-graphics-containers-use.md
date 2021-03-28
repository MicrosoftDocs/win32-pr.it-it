---
description: In Windows GDI+ sono disponibili contenitori che è possibile utilizzare per sostituire temporaneamente o aumentare parte dello stato in un oggetto Graphics.
ms.assetid: f3fce8ef-903a-4b9d-b76c-562739d02eb3
title: Contenitori di oggetti Graphics annidati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f9d9feac3494b423d844cb1e3da359af33eaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967202"
---
# <a name="nested-graphics-containers"></a><span data-ttu-id="fab1c-103">Contenitori di oggetti Graphics annidati</span><span class="sxs-lookup"><span data-stu-id="fab1c-103">Nested Graphics Containers</span></span>

<span data-ttu-id="fab1c-104">In Windows GDI+ sono disponibili contenitori che è possibile utilizzare per sostituire temporaneamente o aumentare parte dello stato in un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="fab1c-104">Windows GDI+ provides containers that you can use to temporarily replace or augment part of the state in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="fab1c-105">Per creare un contenitore, chiamare il metodo [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) di un oggetto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="fab1c-105">You create a container by calling the [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) method of a **Graphics** object.</span></span> <span data-ttu-id="fab1c-106">È possibile chiamare **Graphics:: BeginContainer** ripetutamente per creare contenitori nidificati.</span><span class="sxs-lookup"><span data-stu-id="fab1c-106">You can call **Graphics::BeginContainer** repeatedly to form nested containers.</span></span>

## <a name="transformations-in-nested-containers"></a><span data-ttu-id="fab1c-107">Trasformazioni nei contenitori annidati</span><span class="sxs-lookup"><span data-stu-id="fab1c-107">Transformations in Nested Containers</span></span>

<span data-ttu-id="fab1c-108">Nell'esempio seguente vengono creati un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un contenitore all'interno dell'oggetto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="fab1c-108">The following example creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container within that **Graphics** object.</span></span> <span data-ttu-id="fab1c-109">La trasformazione globale dell'oggetto **Graphics** è una conversione di unità 100 nella direzione x e 80 unità nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="fab1c-109">The world transformation of the **Graphics** object is a translation 100 units in the x direction and 80 units in the y direction.</span></span> <span data-ttu-id="fab1c-110">La trasformazione globale del contenitore è una rotazione di 30 gradi.</span><span class="sxs-lookup"><span data-stu-id="fab1c-110">The world transformation of the container is a 30-degree rotation.</span></span> <span data-ttu-id="fab1c-111">Il codice effettua la chiamata</span><span class="sxs-lookup"><span data-stu-id="fab1c-111">The code makes the call</span></span>


```
DrawRectangle(&pen, -60, -30, 120, 60)
```



<span data-ttu-id="fab1c-112">doppio.</span><span class="sxs-lookup"><span data-stu-id="fab1c-112">twice.</span></span> <span data-ttu-id="fab1c-113">La prima chiamata a [**Graphics::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) si trova *all'interno del contenitore*; ovvero la chiamata è tra le chiamate a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) e [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer).</span><span class="sxs-lookup"><span data-stu-id="fab1c-113">The first call to [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) is *inside the container*; that is, the call is in between the calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer).</span></span> <span data-ttu-id="fab1c-114">La seconda chiamata a **Graphics::D rawrectangle** è successiva alla chiamata a **Graphics:: EndContainer**.</span><span class="sxs-lookup"><span data-stu-id="fab1c-114">The second call to **Graphics::DrawRectangle** is after the call to **Graphics::EndContainer**.</span></span>


```
Graphics           graphics(hdc);
Pen                pen(Color(255, 255, 0, 0));
GraphicsContainer  graphicsContainer;

graphics.TranslateTransform(100.0f, 80.0f);

graphicsContainer = graphics.BeginContainer();
   graphics.RotateTransform(30.0f);
   graphics.DrawRectangle(&pen, -60, -30, 120, 60);
graphics.EndContainer(graphicsContainer);

graphics.DrawRectangle(&pen, -60, -30, 120, 60);
```



<span data-ttu-id="fab1c-115">Nel codice precedente, il rettangolo disegnato dall'interno del contenitore viene trasformato prima dalla trasformazione globale del contenitore (rotazione), quindi dalla trasformazione globale dell'oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) (Translation).</span><span class="sxs-lookup"><span data-stu-id="fab1c-115">In the preceding code, the rectangle drawn from inside the container is transformed first by the world transformation of the container (rotation) and then by the world transformation of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object (translation).</span></span> <span data-ttu-id="fab1c-116">Il rettangolo disegnato dall'esterno del contenitore viene trasformato solo dalla trasformazione globale dell'oggetto **Graphics** (Translation).</span><span class="sxs-lookup"><span data-stu-id="fab1c-116">The rectangle drawn from outside the container is transformed only by the world transformation of the **Graphics** object (translation).</span></span> <span data-ttu-id="fab1c-117">Nella figura seguente sono illustrati i due rettangoli.</span><span class="sxs-lookup"><span data-stu-id="fab1c-117">The following illustration shows the two rectangles.</span></span>

![Screenshot di una finestra con due rettangoli rossi centrati nello stesso punto, ma con rotazioni diverse](images/nestedcontainers1.png)

 

## <a name="clipping-in-nested-containers"></a><span data-ttu-id="fab1c-119">Ritaglio in contenitori annidati</span><span class="sxs-lookup"><span data-stu-id="fab1c-119">Clipping in Nested Containers</span></span>

<span data-ttu-id="fab1c-120">Nell'esempio seguente viene illustrato il modo in cui i contenitori nidificati gestiscono le aree di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="fab1c-120">The following example illustrates how nested containers handle clipping regions.</span></span> <span data-ttu-id="fab1c-121">Il codice crea un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un contenitore all'interno dell'oggetto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="fab1c-121">The code creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container within that **Graphics** object.</span></span> <span data-ttu-id="fab1c-122">L'area di visualizzazione dell'oggetto **Graphics** è un rettangolo e l'area di visualizzazione del contenitore è un'ellisse.</span><span class="sxs-lookup"><span data-stu-id="fab1c-122">The clipping region of the **Graphics** object is a rectangle, and the clipping region of the container is an ellipse.</span></span> <span data-ttu-id="fab1c-123">Il codice effettua due chiamate al metodo [**Graphics::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="fab1c-123">The code makes two calls to the [**Graphics::DrawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method.</span></span> <span data-ttu-id="fab1c-124">La prima chiamata a **Graphics::D rawline** si trova all'interno del contenitore e la seconda chiamata a **Graphics::D rawline** è esterna al contenitore (dopo la chiamata a [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span><span class="sxs-lookup"><span data-stu-id="fab1c-124">The first call to **Graphics::DrawLine** is inside the container, and the second call to **Graphics::DrawLine** is outside the container (after the call to [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span></span> <span data-ttu-id="fab1c-125">La prima riga viene ritagliata dall'intersezione delle due aree di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="fab1c-125">The first line is clipped by the intersection of the two clipping regions.</span></span> <span data-ttu-id="fab1c-126">La seconda riga viene troncata solo dall'area di ridimensionamento rettangolare dell'oggetto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="fab1c-126">The second line is clipped only by the rectangular clipping region of the **Graphics** object.</span></span>


```
Graphics           graphics(hdc);
GraphicsContainer  graphicsContainer;
Pen                redPen(Color(255, 255, 0, 0), 2);
Pen                bluePen(Color(255, 0, 0, 255), 2);
SolidBrush         aquaBrush(Color(255, 180, 255, 255));
SolidBrush         greenBrush(Color(255, 150, 250, 130));

graphics.SetClip(Rect(50, 65, 150, 120));
graphics.FillRectangle(&aquaBrush, 50, 65, 150, 120);

graphicsContainer = graphics.BeginContainer();
   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(75, 50, 100, 150);

  // Construct a region based on the path.
   Region region(&path);
   graphics.FillRegion(&greenBrush, &region);

   graphics.SetClip(&region);
   graphics.DrawLine(&redPen, 50, 0, 350, 300);
graphics.EndContainer(graphicsContainer);

graphics.DrawLine(&bluePen, 70, 0, 370, 300);
```



<span data-ttu-id="fab1c-127">Nella figura seguente sono illustrate le due righe ritagliate.</span><span class="sxs-lookup"><span data-stu-id="fab1c-127">The following illustration shows the two clipped lines.</span></span>

![illustrazione di un'ellisse all'interno di un rettangolo, con una riga ritagliata dall'ellisse e l'altra dal rettangolo](images/nestedcontainers2.png)

<span data-ttu-id="fab1c-129">Come illustrato nei due esempi precedenti, le trasformazioni e le aree di ridimensionamento sono cumulative nei contenitori nidificati.</span><span class="sxs-lookup"><span data-stu-id="fab1c-129">As the two preceding examples show, transformations and clipping regions are cumulative in nested containers.</span></span> <span data-ttu-id="fab1c-130">Se si impostano le trasformazioni globali del contenitore e dell'oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , entrambe le trasformazioni verranno applicate agli elementi disegnati dall'interno del contenitore.</span><span class="sxs-lookup"><span data-stu-id="fab1c-130">If you set the world transformations of the container and the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, both transformations will apply to items drawn from inside the container.</span></span> <span data-ttu-id="fab1c-131">La trasformazione del contenitore verrà applicata per prima e la trasformazione dell'oggetto **Graphics** verrà applicata secondo.</span><span class="sxs-lookup"><span data-stu-id="fab1c-131">The transformation of the container will be applied first, and the transformation of the **Graphics** object will be applied second.</span></span> <span data-ttu-id="fab1c-132">Se si impostano le aree di visualizzazione del contenitore e l'oggetto **Graphics** , gli elementi disegnati dall'interno del contenitore verranno ritagliati dall'intersezione delle due aree di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="fab1c-132">If you set the clipping regions of the container and the **Graphics** object, items drawn from inside the container will be clipped by the intersection of the two clipping regions.</span></span>

## <a name="quality-settings-in-nested-containers"></a><span data-ttu-id="fab1c-133">Impostazioni di qualità nei contenitori annidati</span><span class="sxs-lookup"><span data-stu-id="fab1c-133">Quality Settings in Nested Containers</span></span>

<span data-ttu-id="fab1c-134">Le impostazioni di qualità ( [**SmoothingMode**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode), [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)e like) nei contenitori annidati non sono cumulative. piuttosto, le impostazioni di qualità del contenitore sostituiscono temporaneamente le impostazioni di qualità di un oggetto [**grafico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="fab1c-134">Quality settings ( [**SmoothingMode**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode), [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint), and the like) in nested containers are not cumulative; rather, the quality settings of the container temporarily replace the quality settings of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="fab1c-135">Quando si crea un nuovo contenitore, le impostazioni di qualità per il contenitore sono impostate sui valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="fab1c-135">When you create a new container, the quality settings for that container are set to default values.</span></span> <span data-ttu-id="fab1c-136">Si supponga, ad esempio, di avere un oggetto **Graphics** con una modalità di smussatura di \* \* \* [\* SmoothingModeAntiAlias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)\* \*.</span><span class="sxs-lookup"><span data-stu-id="fab1c-136">For example, suppose you have a **Graphics** object with a smoothing mode of [\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode).</span></span> <span data-ttu-id="fab1c-137">Quando si crea un contenitore, la modalità di smussatura all'interno del contenitore è la modalità di smussatura predefinita.</span><span class="sxs-lookup"><span data-stu-id="fab1c-137">When you create a container, the smoothing mode inside the container is the default smoothing mode.</span></span> <span data-ttu-id="fab1c-138">È possibile impostare la modalità di smussatura del contenitore e tutti gli elementi disegnati dall'interno del contenitore verranno disegnati in base alla modalità impostata.</span><span class="sxs-lookup"><span data-stu-id="fab1c-138">You are free to set the smoothing mode of the container, and any items drawn from inside the container will be drawn according to the mode you set.</span></span> <span data-ttu-id="fab1c-139">Gli elementi disegnati dopo la chiamata a [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) verranno disegnati in base alla modalità di smussamento ([\* \* \* \* SmoothingModeAntiAlias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)\* \*) che era presente prima della chiamata a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span><span class="sxs-lookup"><span data-stu-id="fab1c-139">Items drawn after the call to [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) will be drawn according to the smoothing mode ([\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)) that was in place before the call to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span></span>

## <a name="several-layers-of-nested-containers"></a><span data-ttu-id="fab1c-140">Diversi livelli di contenitori annidati</span><span class="sxs-lookup"><span data-stu-id="fab1c-140">Several Layers of Nested Containers</span></span>

<span data-ttu-id="fab1c-141">Non si è limitati a un contenitore in un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="fab1c-141">You are not limited to one container in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="fab1c-142">È possibile creare una sequenza di contenitori, ognuno nidificato nell'oggetto precedente, ed è possibile specificare la trasformazione globale, l'area di ridimensionamento e le impostazioni di qualità di ognuno di questi contenitori annidati.</span><span class="sxs-lookup"><span data-stu-id="fab1c-142">You can create a sequence of containers, each nested in the preceding, and you can specify the world transformation, clipping region, and quality settings of each of those nested containers.</span></span> <span data-ttu-id="fab1c-143">Se si chiama un metodo Drawing dall'interno del contenitore più interno, le trasformazioni verranno applicate in ordine, a partire dal contenitore più interno e terminando con il contenitore più esterno.</span><span class="sxs-lookup"><span data-stu-id="fab1c-143">If you call a drawing method from inside the innermost container, the transformations will be applied in order, starting with the innermost container and ending with the outermost container.</span></span> <span data-ttu-id="fab1c-144">Gli elementi disegnati dall'interno del contenitore più interno verranno ritagliati dall'intersezione di tutte le aree di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="fab1c-144">Items drawn from inside the innermost container will be clipped by the intersection of all the clipping regions.</span></span>

<span data-ttu-id="fab1c-145">Nell'esempio seguente viene creato un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e ne viene impostato l'hint per il rendering del testo su \* \* \* [\* TextRenderingHintAntiAlias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)\* \*.</span><span class="sxs-lookup"><span data-stu-id="fab1c-145">The following example creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and sets its text rendering hint to [\*\*\*\*TextRenderingHintAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint).</span></span> <span data-ttu-id="fab1c-146">Il codice crea due contenitori, uno annidato all'interno dell'altro.</span><span class="sxs-lookup"><span data-stu-id="fab1c-146">The code creates two containers, one nested within the other.</span></span> <span data-ttu-id="fab1c-147">L'hint per il rendering del testo del contenitore esterno è impostato su [\* \* \* \* TextRenderingHintSingleBitPerPixel \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)\* \* e l'hint per il rendering del testo del contenitore interno è impostato su [\* \* \* \* TextRenderingHintAntiAlias \* \* \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint).</span><span class="sxs-lookup"><span data-stu-id="fab1c-147">The text rendering hint of the outer container is set to [\*\*\*\*TextRenderingHintSingleBitPerPixel\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint), and the text rendering hint of the inner container is set to [\*\*\*\*TextRenderingHintAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint).</span></span> <span data-ttu-id="fab1c-148">Il codice disegna tre stringhe: una dal contenitore interno, una dal contenitore esterno e una dall'oggetto **Graphics** stesso.</span><span class="sxs-lookup"><span data-stu-id="fab1c-148">The code draws three strings: one from the inner container, one from the outer container, and one from the **Graphics** object itself.</span></span>


```
Graphics graphics(hdc);
GraphicsContainer innerContainer;
GraphicsContainer outerContainer;
SolidBrush brush(Color(255, 0, 0, 255));
FontFamily fontFamily(L"Times New Roman");
Font font(&fontFamily, 36, FontStyleRegular, UnitPixel);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);

outerContainer = graphics.BeginContainer();

   graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);

   innerContainer = graphics.BeginContainer();
      graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
      graphics.DrawString(L"Inner Container", 15, &font,
         PointF(20, 10), &brush);
   graphics.EndContainer(innerContainer);

   graphics.DrawString(L"Outer Container", 15, &font, PointF(20, 50), &brush);

graphics.EndContainer(outerContainer);

graphics.DrawString(L"Graphics Object", 15, &font, PointF(20, 90), &brush);
```



<span data-ttu-id="fab1c-149">Nella figura seguente sono illustrate le tre stringhe.</span><span class="sxs-lookup"><span data-stu-id="fab1c-149">The following illustration shows the three strings.</span></span> <span data-ttu-id="fab1c-150">Le stringhe disegnate dal contenitore interno e dall'oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) sono smussate mediante l'anti-aliasing.</span><span class="sxs-lookup"><span data-stu-id="fab1c-150">The strings drawn from the inner container and the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object are smoothed by antialiasing.</span></span> <span data-ttu-id="fab1c-151">La stringa disegnata dal contenitore esterno non è smussata mediante l'anti-aliasing a causa dell'impostazione TextRenderingHintSingleBitPerPixel.</span><span class="sxs-lookup"><span data-stu-id="fab1c-151">The string drawn from the outer container is not smoothed by antialiasing because of the TextRenderingHintSingleBitPerPixel setting.</span></span>

![illustrazione di un rettangolo contenente la stessa stringa. solo i caratteri nella prima e nell'ultima riga sono uniformi](images/nestedcontainers3.png)

 

 
