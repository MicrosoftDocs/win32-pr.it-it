---
description: GDI+ fornisce gradienti lineari orizzontali, verticali e diagonali. Per impostazione predefinita, il colore in una sfumatura lineare cambia in modo uniforme. Tuttavia, è possibile personalizzare una sfumatura lineare in modo che il colore cambi in modo non uniforme.
ms.assetid: 9b0236b2-be6b-4918-a106-5b0e6c3dd5ff
title: Creazione di una sfumatura lineare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d66b9f5a3a07061e8b3d19140c25a9f3a33052a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553274"
---
# <a name="creating-a-linear-gradient"></a><span data-ttu-id="b6ba2-105">Creazione di una sfumatura lineare</span><span class="sxs-lookup"><span data-stu-id="b6ba2-105">Creating a Linear Gradient</span></span>

<span data-ttu-id="b6ba2-106">GDI+ fornisce gradienti lineari orizzontali, verticali e diagonali.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-106">GDI+ provides horizontal, vertical, and diagonal linear gradients.</span></span> <span data-ttu-id="b6ba2-107">Per impostazione predefinita, il colore in una sfumatura lineare cambia in modo uniforme.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-107">By default, the color in a linear gradient changes uniformly.</span></span> <span data-ttu-id="b6ba2-108">Tuttavia, è possibile personalizzare una sfumatura lineare in modo che il colore cambi in modo non uniforme.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-108">However, you can customize a linear gradient so that the color changes in a non-uniform fashion.</span></span>

-   [<span data-ttu-id="b6ba2-109">Sfumature lineari orizzontali</span><span class="sxs-lookup"><span data-stu-id="b6ba2-109">Horizontal Linear Gradients</span></span>](#horizontal-linear-gradients)
-   [<span data-ttu-id="b6ba2-110">Personalizzazione delle sfumature lineari</span><span class="sxs-lookup"><span data-stu-id="b6ba2-110">Customizing Linear Gradients</span></span>](#customizing-linear-gradients)
-   [<span data-ttu-id="b6ba2-111">Gradienti lineari diagonali</span><span class="sxs-lookup"><span data-stu-id="b6ba2-111">Diagonal Linear Gradients</span></span>](#diagonal-linear-gradients)

## <a name="horizontal-linear-gradients"></a><span data-ttu-id="b6ba2-112">Sfumature lineari orizzontali</span><span class="sxs-lookup"><span data-stu-id="b6ba2-112">Horizontal Linear Gradients</span></span>

<span data-ttu-id="b6ba2-113">Nell'esempio seguente viene usato un pennello a sfumatura lineare orizzontale per riempire una riga, un'ellisse e un rettangolo:</span><span class="sxs-lookup"><span data-stu-id="b6ba2-113">The following example uses a horizontal linear gradient brush to fill a line, an ellipse, and a rectangle:</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // opaque red
   Color(255, 0, 0, 255));  // opaque blue

Pen pen(&linGrBrush);

graphics.DrawLine(&pen, 0, 10, 200, 10);
graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



<span data-ttu-id="b6ba2-114">Il costruttore [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) riceve quattro argomenti: due punti e due colori.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-114">The [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) constructor receives four arguments: two points and two colors.</span></span> <span data-ttu-id="b6ba2-115">Il primo punto (0, 10) è associato al primo colore (rosso) e il secondo punto (200, 10) viene associato al secondo colore (blu).</span><span class="sxs-lookup"><span data-stu-id="b6ba2-115">The first point (0, 10) is associated with the first color (red), and the second point (200, 10) is associated with the second color (blue).</span></span> <span data-ttu-id="b6ba2-116">Come ci si aspetterebbe, la linea disegnata da (0, 10) a (200, 10) cambia gradualmente da rosso a blu.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-116">As you would expect, the line drawn from (0, 10) to (200, 10) changes gradually from red to blue.</span></span>

<span data-ttu-id="b6ba2-117">I 10s nei punti (50, 10) e (200, 10) non sono importanti.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-117">The 10s in the points (50, 10) and (200, 10) are not important.</span></span> <span data-ttu-id="b6ba2-118">L'aspetto importante è che i due punti hanno la stessa seconda coordinata, ovvero la linea che la connette è orizzontale.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-118">What's important is that the two points have the same second coordinate — the line connecting them is horizontal.</span></span> <span data-ttu-id="b6ba2-119">Anche l'ellisse e il rettangolo cambiano gradualmente da rosso a blu, perché la coordinata orizzontale va da 0 a 200.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-119">The ellipse and the rectangle also change gradually from red to blue as the horizontal coordinate goes from 0 to 200.</span></span>

<span data-ttu-id="b6ba2-120">La figura seguente mostra la riga, l'ellisse e il rettangolo.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-120">The following illustration shows the line, the ellipse, and the rectangle.</span></span> <span data-ttu-id="b6ba2-121">Si noti che la sfumatura di colore si ripete quando la coordinata orizzontale aumenta oltre 200.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-121">Note that the color gradient repeats itself as the horizontal coordinate increases beyond 200.</span></span>

![illustrazione che mostra una sfumatura orizzontale che riempie una riga e un'ellisse e un rettangolo più lungo dell'ellisse](images/lineargradient1.png)

## <a name="customizing-linear-gradients"></a><span data-ttu-id="b6ba2-123">Personalizzazione delle sfumature lineari</span><span class="sxs-lookup"><span data-stu-id="b6ba2-123">Customizing Linear Gradients</span></span>

<span data-ttu-id="b6ba2-124">Nell'esempio precedente, i componenti dei colori cambiano in modo lineare quando si passa da una coordinata orizzontale di 0 a una coordinata orizzontale di 200.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-124">In the preceding example, the color components change linearly as you move from a horizontal coordinate of 0 to a horizontal coordinate of 200.</span></span> <span data-ttu-id="b6ba2-125">Ad esempio, un punto la cui prima coordinata è a metà tra 0 e 200 avrà un componente blu a metà tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-125">For example, a point whose first coordinate is halfway between 0 and 200 will have a blue component that is halfway between 0 and 255.</span></span>

<span data-ttu-id="b6ba2-126">GDI+ consente di modificare il modo in cui un colore varia da un bordo di una sfumatura all'altro.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-126">GDI+ allows you to adjust the way a color varies from one edge of a gradient to the other.</span></span> <span data-ttu-id="b6ba2-127">Si supponga di voler creare un pennello sfumato che cambi da nero a rosso in base alla tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-127">Suppose you want to create a gradient brush that changes from black to red according to the following table.</span></span>



| <span data-ttu-id="b6ba2-128">Coordinata orizzontale</span><span class="sxs-lookup"><span data-stu-id="b6ba2-128">Horizontal coordinate</span></span> | <span data-ttu-id="b6ba2-129">Componenti RGB</span><span class="sxs-lookup"><span data-stu-id="b6ba2-129">RGB components</span></span> |
|-----------------------|----------------|
| <span data-ttu-id="b6ba2-130">0</span><span class="sxs-lookup"><span data-stu-id="b6ba2-130">0</span></span>                     | <span data-ttu-id="b6ba2-131">(0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="b6ba2-131">(0, 0, 0)</span></span>      |
| <span data-ttu-id="b6ba2-132">40</span><span class="sxs-lookup"><span data-stu-id="b6ba2-132">40</span></span>                    | <span data-ttu-id="b6ba2-133">(128, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="b6ba2-133">(128, 0, 0)</span></span>    |
| <span data-ttu-id="b6ba2-134">200</span><span class="sxs-lookup"><span data-stu-id="b6ba2-134">200</span></span>                   | <span data-ttu-id="b6ba2-135">(255, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="b6ba2-135">(255, 0, 0)</span></span>    |



 

<span data-ttu-id="b6ba2-136">Si noti che il componente rosso è a metà intensità quando la coordinata orizzontale è solo il 20% della strada da 0 a 200.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-136">Note that the red component is at half intensity when the horizontal coordinate is only 20 percent of the way from 0 to 200.</span></span>

<span data-ttu-id="b6ba2-137">Nell'esempio seguente viene chiamato il metodo [**LinearGradientBrush:: seblend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) di un oggetto [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) per associare tre intensità relative con tre posizioni relative.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-137">The following example calls the [**LinearGradientBrush::SetBlend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) method of a [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) object to associate three relative intensities with three relative positions.</span></span> <span data-ttu-id="b6ba2-138">Come nella tabella precedente, un'intensità relativa di 0,5 è associata a una posizione relativa di 0,2.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-138">As in the preceding table, a relative intensity of 0.5 is associated with a relative position of 0.2.</span></span> <span data-ttu-id="b6ba2-139">Il codice riempie un'ellisse e un rettangolo con il pennello sfumatura.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-139">The code fills an ellipse and a rectangle with the gradient brush.</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 0, 0, 0),     // opaque black 
   Color(255, 255, 0, 0));  // opaque red

REAL relativeIntensities[] = {0.0f, 0.5f, 1.0f};
REAL relativePositions[]   = {0.0f, 0.2f, 1.0f};

linGrBrush.SetBlend(relativeIntensities, relativePositions, 3);

graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



<span data-ttu-id="b6ba2-140">Nella figura seguente vengono illustrati l'ellisse e il rettangolo risultanti.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-140">The following illustration shows the resulting ellipse and rectangle.</span></span>

![illustrazione che mostra una sfumatura orizzontale che riempie un'ellisse e un rettangolo più lungo dell'ellisse](images/lineargradient2.png)

## <a name="diagonal-linear-gradients"></a><span data-ttu-id="b6ba2-142">Gradienti lineari diagonali</span><span class="sxs-lookup"><span data-stu-id="b6ba2-142">Diagonal Linear Gradients</span></span>

<span data-ttu-id="b6ba2-143">Le sfumature degli esempi precedenti sono state orizzontali; ovvero il colore cambia gradualmente man mano che si sposta lungo una linea orizzontale.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-143">The gradients in the preceding examples have been horizontal; that is, the color changes gradually as you move along any horizontal line.</span></span> <span data-ttu-id="b6ba2-144">È anche possibile definire sfumature verticali e sfumature diagonali.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-144">You can also define vertical gradients and diagonal gradients.</span></span> <span data-ttu-id="b6ba2-145">Il codice seguente passa i punti (0, 0) e (200, 100) a un costruttore [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="b6ba2-145">The following code passes the points (0, 0) and (200, 100) to a [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) constructor.</span></span> <span data-ttu-id="b6ba2-146">Il colore blu è associato a (0, 0) e il colore verde è associato a (200, 100).</span><span class="sxs-lookup"><span data-stu-id="b6ba2-146">The color blue is associated with (0, 0), and the color green is associated with (200, 100).</span></span> <span data-ttu-id="b6ba2-147">Una linea (con larghezza della penna 10) e un'ellisse vengono riempite con il pennello sfumatura lineare.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-147">A line (with pen width 10) and an ellipse are filled with the linear gradient brush.</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 0),
   Point(200, 100),
   Color(255, 0, 0, 255),   // opaque blue
   Color(255, 0, 255, 0));  // opaque green

Pen pen(&linGrBrush, 10);

graphics.DrawLine(&pen, 0, 0, 600, 300);
graphics.FillEllipse(&linGrBrush, 10, 100, 200, 100);
```



<span data-ttu-id="b6ba2-148">La figura seguente mostra la riga e l'ellisse.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-148">The following illustration shows the line and the ellipse.</span></span> <span data-ttu-id="b6ba2-149">Si noti che il colore nell'ellisse cambia gradualmente man mano che si sposta lungo ogni riga che è parallela alla riga che attraversa (0,0) e (200, 100).</span><span class="sxs-lookup"><span data-stu-id="b6ba2-149">Note that the color in the ellipse changes gradually as you move along any line that is parallel to the line passing through (0, 0) and (200, 100).</span></span>

![illustrazione che mostra una sfumatura diagonale che riempie un'ellisse e una linea diagonale](images/lineargradient3.png)

 

 



