---
description: Lo stato graphics &\# 8212; area di ridimensionamento, trasformazioni e impostazioni di qualità &\# 8212; è archiviato in un oggetto Graphics.
ms.assetid: 98b9fa12-02e7-42bf-9cbd-03ee696188f6
title: Contenitori di oggetti Graphics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8bf6469d0835137be1bb76b7727fd961bba16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565515"
---
# <a name="graphics-containers"></a><span data-ttu-id="a0815-103">Contenitori di oggetti Graphics</span><span class="sxs-lookup"><span data-stu-id="a0815-103">Graphics Containers</span></span>

<span data-ttu-id="a0815-104">Lo stato della grafica, ovvero area di ridimensionamento, trasformazioni e impostazioni di qualità, viene archiviato in un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="a0815-104">Graphics state — clipping region, transformations, and quality settings — is stored in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="a0815-105">Windows GDI+ consente di sostituire temporaneamente o aumentare parte dello stato in un oggetto **Graphics** utilizzando un contenitore.</span><span class="sxs-lookup"><span data-stu-id="a0815-105">Windows GDI+ allows you to temporarily replace or augment part of the state in a **Graphics** object by using a container.</span></span> <span data-ttu-id="a0815-106">Per avviare un contenitore, chiamare il metodo [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) di un oggetto **Graphics** e terminare un contenitore chiamando il metodo [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) .</span><span class="sxs-lookup"><span data-stu-id="a0815-106">You start a container by calling the [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) method of a **Graphics** object, and you end a container by calling the [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) method.</span></span> <span data-ttu-id="a0815-107">In between **Graphics:: BeginContainer** e **Graphics:: EndContainer** tutte le modifiche di stato apportate all'oggetto **Graphics** appartengono al contenitore e non sovrascrivono lo stato esistente dell'oggetto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="a0815-107">In between **Graphics::BeginContainer** and **Graphics::EndContainer**, any state changes you make to the **Graphics** object belong to the container and do not overwrite the existing state of the **Graphics** object.</span></span>

<span data-ttu-id="a0815-108">Nell'esempio seguente viene creato un contenitore all'interno di un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="a0815-108">The following example creates a container within a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="a0815-109">La trasformazione globale dell'oggetto **Graphics** è una traduzione 200 unità a destra e la trasformazione globale del contenitore è una conversione 100 unità inattive.</span><span class="sxs-lookup"><span data-stu-id="a0815-109">The world transformation of the **Graphics** object is a translation 200 units to the right, and the world transformation of the container is a translation 100 units down.</span></span>


```
myGraphics.TranslateTransform(200.0f, 0.0f);

myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.TranslateTransform(0.0f, 100.0f);
   myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
myGraphics.EndContainer(myGraphicsContainer);

myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
```



<span data-ttu-id="a0815-110">Si noti che nell'esempio precedente, l'istruzione `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` eseguita tra le chiamate a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) e [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) produce un rettangolo diverso dalla stessa istruzione effettuata dopo la chiamata a **Graphics:: EndContainer**.</span><span class="sxs-lookup"><span data-stu-id="a0815-110">Note that in the previous example, the statement `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` made in between the calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) produces a different rectangle than the same statement made after the call to **Graphics::EndContainer**.</span></span> <span data-ttu-id="a0815-111">Solo la traduzione orizzontale si applica alla chiamata **DrawRectangle** effettuata all'esterno del contenitore.</span><span class="sxs-lookup"><span data-stu-id="a0815-111">Only the horizontal translation applies to the **DrawRectangle** call made outside of the container.</span></span> <span data-ttu-id="a0815-112">Entrambe le trasformazioni, ovvero la traduzione orizzontale di 200 unità e la conversione verticale di 100 unità, si applicano alla [**grafica::D chiamata rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) effettuata all'interno del contenitore.</span><span class="sxs-lookup"><span data-stu-id="a0815-112">Both transformations — the horizontal translation of 200 units and the vertical translation of 100 units — apply to the [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) call made inside the container.</span></span> <span data-ttu-id="a0815-113">Nella figura seguente sono illustrati i due rettangoli.</span><span class="sxs-lookup"><span data-stu-id="a0815-113">The following illustration shows the two rectangles.</span></span>

![Screenshot di una finestra con due rettangoli disegnati con una penna blu, uno posizionato sopra l'altro](images/aboutgdip05-art17.png)

<span data-ttu-id="a0815-115">I contenitori possono essere annidati all'interno dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="a0815-115">Containers can be nested within containers.</span></span> <span data-ttu-id="a0815-116">Nell'esempio seguente viene creato un contenitore in un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un altro contenitore all'interno del primo contenitore.</span><span class="sxs-lookup"><span data-stu-id="a0815-116">The following example creates a container within a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and another container within the first container.</span></span> <span data-ttu-id="a0815-117">La trasformazione globale dell'oggetto **Graphics** è una conversione di unità 100 nella direzione x e 80 unità nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="a0815-117">The world transformation of the **Graphics** object is a translation 100 units in the x direction and 80 units in the y direction.</span></span> <span data-ttu-id="a0815-118">La trasformazione globale del primo contenitore è una rotazione di 30 gradi.</span><span class="sxs-lookup"><span data-stu-id="a0815-118">The world transformation of the first container is a 30-degree rotation.</span></span> <span data-ttu-id="a0815-119">La trasformazione globale del secondo contenitore è una scala per un fattore 2 nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="a0815-119">The world transformation of the second container is a scaling by a factor of 2 in the x direction.</span></span> <span data-ttu-id="a0815-120">Viene eseguita una chiamata al metodo [**Graphics::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) all'interno del secondo contenitore.</span><span class="sxs-lookup"><span data-stu-id="a0815-120">A call to the [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) method is made inside the second container.</span></span>


```
myGraphics.TranslateTransform(100.0f, 80.0f, MatrixOrderAppend);

container1 = myGraphics.BeginContainer();
   myGraphics.RotateTransform(30.0f, MatrixOrderAppend);

   container2 = myGraphics.BeginContainer();
      myGraphics.ScaleTransform(2.0f, 1.0f);
      myGraphics.DrawEllipse(&myPen, -30, -20, 60, 40);
   myGraphics.EndContainer(container2);

myGraphics.EndContainer(container1);
```



<span data-ttu-id="a0815-121">La figura seguente mostra l'ellisse.</span><span class="sxs-lookup"><span data-stu-id="a0815-121">The following illustration shows the ellipse.</span></span>

![Screenshot di una finestra che contiene un'ellisse blu ruotata con il relativo centro contrassegnato come (100, 80)](images/aboutgdip05-art18.png)

<span data-ttu-id="a0815-123">Si noti che tutte e tre le trasformazioni si applicano alla [**grafica::D chiamata rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) effettuata nel secondo contenitore (più interno).</span><span class="sxs-lookup"><span data-stu-id="a0815-123">Note that all three transformations apply to the [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) call made in the second (innermost) container.</span></span> <span data-ttu-id="a0815-124">Si noti anche l'ordine delle trasformazioni: prima scala, quindi ruota, quindi trasla.</span><span class="sxs-lookup"><span data-stu-id="a0815-124">Also note the order of the transformations: first scale, then rotate, then translate.</span></span> <span data-ttu-id="a0815-125">La trasformazione più interna viene applicata per prima e la trasformazione più esterna viene applicata per ultima.</span><span class="sxs-lookup"><span data-stu-id="a0815-125">The innermost transformation is applied first, and the outermost transformation is applied last.</span></span>

<span data-ttu-id="a0815-126">È possibile impostare qualsiasi proprietà di un oggetto [**grafico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) all'interno di un contenitore (tra le chiamate a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) e [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span><span class="sxs-lookup"><span data-stu-id="a0815-126">Any property of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object can be set inside a container (in between calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span></span> <span data-ttu-id="a0815-127">È ad esempio possibile impostare un'area di ridimensionamento all'interno di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="a0815-127">For example, a clipping region can be set inside a container.</span></span> <span data-ttu-id="a0815-128">Qualsiasi disegno eseguito all'interno del contenitore sarà limitato all'area di visualizzazione del contenitore e sarà limitato anche alle aree di visualizzazione di qualsiasi contenitore esterno e all'area di visualizzazione dell'oggetto **Graphics** stesso.</span><span class="sxs-lookup"><span data-stu-id="a0815-128">Any drawing done inside the container will be restricted to the clipping region of that container and will also be restricted to the clipping regions of any outer containers and the clipping region of the **Graphics** object itself.</span></span>

<span data-ttu-id="a0815-129">Le proprietà discusse finora, ovvero la trasformazione mondiale e l'area di visualizzazione, vengono combinate dai contenitori annidati.</span><span class="sxs-lookup"><span data-stu-id="a0815-129">The properties discussed so far — the world transformation and the clipping region — are combined by nested containers.</span></span> <span data-ttu-id="a0815-130">Le altre proprietà vengono temporaneamente sostituite da un contenitore annidato.</span><span class="sxs-lookup"><span data-stu-id="a0815-130">Other properties are temporarily replaced by a nested container.</span></span> <span data-ttu-id="a0815-131">Se, ad esempio, si imposta la modalità di smussatura su SmoothingModeAntiAlias all'interno di un contenitore, qualsiasi metodo di disegno chiamato all'interno del contenitore utilizzerà la modalità di smussamento AntiAlias, ma i metodi di disegno chiamati dopo [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) utilizzeranno la modalità di smussamento che era presente prima della chiamata a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span><span class="sxs-lookup"><span data-stu-id="a0815-131">For example, if you set the smoothing mode to SmoothingModeAntiAlias within a container, any drawing methods called inside that container will use the antialias smoothing mode, but drawing methods called after [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) will use the smoothing mode that was in place before the call to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span></span>

<span data-ttu-id="a0815-132">Per un altro esempio di combinazione delle trasformazioni internazionali di un oggetto [**grafico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e di un contenitore, si supponga di voler creare un occhio e posizionarlo in varie posizioni in una sequenza di visi.</span><span class="sxs-lookup"><span data-stu-id="a0815-132">For another example of combining the world transformations of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container, suppose you want to draw an eye and place it at various locations on a sequence of faces.</span></span> <span data-ttu-id="a0815-133">Nell'esempio seguente viene disegnato un occhio centrato sull'origine del sistema di coordinate.</span><span class="sxs-lookup"><span data-stu-id="a0815-133">The following example draws an eye centered at the origin of the coordinate system.</span></span>


```
void DrawEye(Graphics* pGraphics)
{
   GraphicsContainer eyeContainer;
   
   eyeContainer = pGraphics->BeginContainer();

      Pen myBlackPen(Color(255, 0, 0, 0));
      SolidBrush myGreenBrush(Color(255, 0, 128, 0));
      SolidBrush myBlackBrush(Color(255, 0, 0, 0));

      GraphicsPath myTopPath;
      myTopPath.AddEllipse(-30, -50, 60, 60);

      GraphicsPath myBottomPath;
      myBottomPath.AddEllipse(-30, -10, 60, 60);

      Region myTopRegion(&myTopPath);
      Region myBottomRegion(&myBottomPath);

      // Draw the outline of the eye.
      // The outline of the eye consists of two ellipses.
      // The top ellipse is clipped by the bottom ellipse, and
      // the bottom ellipse is clipped by the top ellipse.
      pGraphics->SetClip(&myTopRegion);
      pGraphics->DrawPath(&myBlackPen, &myBottomPath);
      pGraphics->SetClip(&myBottomRegion);
      pGraphics->DrawPath(&myBlackPen, &myTopPath);

      // Fill the iris.
      // The iris is clipped by the bottom ellipse.
      pGraphics->FillEllipse(&myGreenBrush, -10, -15, 20, 22);

      // Fill the pupil.
      pGraphics->FillEllipse(&myBlackBrush, -3, -7, 6, 9);

   pGraphics->EndContainer(eyeContainer);
}
```



<span data-ttu-id="a0815-134">Nella figura seguente vengono illustrati l'occhio e gli assi delle coordinate.</span><span class="sxs-lookup"><span data-stu-id="a0815-134">The following illustration shows the eye and the coordinate axes.</span></span>

![illustrazione che mostra un occhio composto da tre ellissi: uno per la struttura, Iris e la pupilla](images/aboutgdip05-art19.png)

<span data-ttu-id="a0815-136">La funzione DrawEye, definita nell'esempio precedente, riceve l'indirizzo di un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e crea immediatamente un contenitore all'interno dell'oggetto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="a0815-136">The DrawEye function, defined in the previous example receives the address of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and immediately creates a container within that **Graphics** object.</span></span> <span data-ttu-id="a0815-137">Questo contenitore isola il codice che chiama la funzione DrawEye dalle impostazioni delle proprietà effettuate durante l'esecuzione della funzione DrawEye.</span><span class="sxs-lookup"><span data-stu-id="a0815-137">This container insulates any code that calls the DrawEye function from property settings made during the execution of the DrawEye function.</span></span> <span data-ttu-id="a0815-138">Ad esempio, il codice nella funzione DrawEye imposta l'area di visualizzazione dell'oggetto **Graphics** , ma quando DrawEye restituisce il controllo alla routine chiamante, l'area di ridimensionamento sarà così com'era prima della chiamata a DrawEye.</span><span class="sxs-lookup"><span data-stu-id="a0815-138">For example, code in the DrawEye function sets the clipping region of the **Graphics** object, but when DrawEye returns control to the calling routine, the clipping region will be as it was before the call to DrawEye.</span></span>

<span data-ttu-id="a0815-139">Nell'esempio seguente vengono disegnati tre ellissi (visi), ognuno con un occhio all'interno.</span><span class="sxs-lookup"><span data-stu-id="a0815-139">The following example draws three ellipses (faces), each with an eye inside.</span></span>


```
// Draw an ellipse with center at (100, 100).
myGraphics.TranslateTransform(100.0f, 100.0f);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Draw the eye at the center of the ellipse.
DrawEye(&myGraphics);

// Draw an ellipse with center at 200, 100.
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Rotate the eye 40 degrees, and draw it 30 units above
// the center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.RotateTransform(-40.0f);
   myGraphics.TranslateTransform(0.0f, -30.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);

// Draw a ellipse with center at (300.0f, 100.0f).
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Stretch and rotate the eye, and draw it at the 
// center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.ScaleTransform(2.0f, 1.5f);
   myGraphics.RotateTransform(45.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);
```



<span data-ttu-id="a0815-140">Nella figura seguente sono illustrati i tre ellissi.</span><span class="sxs-lookup"><span data-stu-id="a0815-140">The following illustration shows the three ellipses.</span></span>

![Screenshot di una finestra con tre ellissi, ognuno dei quali contiene un occhio a una dimensione e una rotazione diverse](images/aboutgdip05-art20.png)

<span data-ttu-id="a0815-142">Nell'esempio precedente, tutti i puntini di sospensione vengono disegnati con la chiamata `DrawEllipse(&myBlackPen, -40, -60, 80, 120)` , che disegna un'ellisse centrata sull'origine del sistema di coordinate.</span><span class="sxs-lookup"><span data-stu-id="a0815-142">In the previous example, all ellipses are drawn with the call `DrawEllipse(&myBlackPen, -40, -60, 80, 120)`, which draws an ellipse centered at the origin of the coordinate system.</span></span> <span data-ttu-id="a0815-143">I puntini di sospensione vengono spostati dall'angolo superiore sinistro dell'area client impostando la trasformazione globale dell'oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="a0815-143">The ellipses are moved away from the upper-left corner of the client area by setting the world transformation of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="a0815-144">L'istruzione fa in modo che la prima ellisse si trovi al centro (100, 100).</span><span class="sxs-lookup"><span data-stu-id="a0815-144">The statement causes the first ellipse to be centered at (100, 100).</span></span> <span data-ttu-id="a0815-145">L'istruzione fa in modo che il centro della seconda ellisse sia 100 unità a destra del centro della prima ellisse.</span><span class="sxs-lookup"><span data-stu-id="a0815-145">The statement causes the center of the second ellipse to be 100 units to the right of the center of the first ellipse.</span></span> <span data-ttu-id="a0815-146">Analogamente, il centro della terza ellisse è 100 unità a destra del centro della seconda ellisse.</span><span class="sxs-lookup"><span data-stu-id="a0815-146">Likewise, the center of the third ellipse is 100 units to the right of the center of the second ellipse.</span></span>

<span data-ttu-id="a0815-147">I contenitori nell'esempio precedente vengono usati per trasformare l'occhio rispetto al centro di una determinata ellisse.</span><span class="sxs-lookup"><span data-stu-id="a0815-147">The containers in the previous example are used to transform the eye relative to the center of a given ellipse.</span></span> <span data-ttu-id="a0815-148">Il primo occhio viene disegnato al centro dell'ellisse senza trasformazione, quindi la chiamata DrawEye non si trova all'interno di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="a0815-148">The first eye is drawn at the center of the ellipse with no transformation, so the DrawEye call is not inside a container.</span></span> <span data-ttu-id="a0815-149">Il secondo occhio è ruotato di 40 gradi e ha disegnato 30 unità al di sopra del centro dell'ellisse, quindi la funzione DrawEye e i metodi che impostano la trasformazione vengono chiamati all'interno di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="a0815-149">The second eye is rotated 40 degrees and drawn 30 units above the center of the ellipse, so the DrawEye function and the methods that set the transformation are called inside a container.</span></span> <span data-ttu-id="a0815-150">Il terzo occhio viene allungato e ruotato e disegnato al centro dell'ellisse.</span><span class="sxs-lookup"><span data-stu-id="a0815-150">The third eye is stretched and rotated and drawn at the center of the ellipse.</span></span> <span data-ttu-id="a0815-151">Come nel secondo occhio, la funzione DrawEye e i metodi che impostano la trasformazione vengono chiamati all'interno di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="a0815-151">As with the second eye, the DrawEye function and the methods that set the transformation are called inside a container.</span></span>

 

 
