---
title: Applicazione di trasformazioni in Direct2D
description: Applicazione di trasformazioni in Direct2D
ms.assetid: 4b54dcfc-f915-4e4a-aa88-ee23c341c2a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8edddbb3150f16428c56bd4c6da828c9b2ce594e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727338"
---
# <a name="applying-transforms-in-direct2d"></a><span data-ttu-id="2b1fb-103">Applicazione di trasformazioni in Direct2D</span><span class="sxs-lookup"><span data-stu-id="2b1fb-103">Applying Transforms in Direct2D</span></span>

<span data-ttu-id="2b1fb-104">Nel [disegno con Direct2D](drawing-with-direct2d.md)è stato rilevato che il metodo [**ID2D1RenderTarget:: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) disegna un'ellisse allineata agli assi x e y.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-104">In [Drawing with Direct2D](drawing-with-direct2d.md), we saw that the [**ID2D1RenderTarget::FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method draws an ellipse that is aligned to the x- and y-axes.</span></span> <span data-ttu-id="2b1fb-105">Ma si supponga di voler creare un'ellisse inclinata in un angolo?</span><span class="sxs-lookup"><span data-stu-id="2b1fb-105">But suppose that you want to draw an ellipse tilted at an angle?</span></span>

![immagine che mostra un'ellisse inclinata.](images/graphics16.png)

<span data-ttu-id="2b1fb-107">Utilizzando le trasformazioni, è possibile modificare una forma nei modi seguenti.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-107">By using transforms, you can alter a shape in the following ways.</span></span>

-   <span data-ttu-id="2b1fb-108">Rotazione intorno a un punto.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-108">Rotation around a point.</span></span>
-   <span data-ttu-id="2b1fb-109">Ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-109">Scaling.</span></span>
-   <span data-ttu-id="2b1fb-110">Traduzione (spostamento nella direzione X o Y).</span><span class="sxs-lookup"><span data-stu-id="2b1fb-110">Translation (displacement in the X or Y direction).</span></span>
-   <span data-ttu-id="2b1fb-111">Asimmetria (anche nota come *cesoia*).</span><span class="sxs-lookup"><span data-stu-id="2b1fb-111">Skew (also known as *shear*).</span></span>

<span data-ttu-id="2b1fb-112">Una trasformazione è un'operazione matematica che esegue il mapping di un set di punti a un nuovo set di punti.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-112">A transform is a mathematical operation that maps a set of points to a new set of points.</span></span> <span data-ttu-id="2b1fb-113">Il diagramma seguente, ad esempio, Mostra un triangolo ruotato intorno al punto P3.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-113">For example, the following diagram shows a triangle rotated around the point P3.</span></span> <span data-ttu-id="2b1fb-114">Dopo l'applicazione della rotazione, il punto P1 viene mappato a P1', il punto P2 viene mappato a P2' e il punto P3 viene mappato a se stesso.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-114">After the rotation is applied, the point P1 is mapped to P1', the point P2 is mapped to P2', and the point P3 maps to itself.</span></span>

![diagramma che mostra la rotazione intorno a un punto.](images/graphics17.png)

<span data-ttu-id="2b1fb-116">Le trasformazioni vengono implementate tramite matrici.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-116">Transforms are implemented by using matrices.</span></span> <span data-ttu-id="2b1fb-117">Non è tuttavia necessario comprendere la matematica delle matrici per utilizzarle.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-117">However, you do not have to understand the mathematics of matrices in order to use them.</span></span> <span data-ttu-id="2b1fb-118">Per ulteriori informazioni sui calcoli matematici, vedere [Appendice: trasformazioni matrice](appendix--matrix-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="2b1fb-118">If you want to learn more about the math, see [Appendix: Matrix Transforms](appendix--matrix-transforms.md).</span></span>

<span data-ttu-id="2b1fb-119">Per applicare una trasformazione in Direct2D, chiamare il metodo [**ID2D1RenderTarget:: setransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) .</span><span class="sxs-lookup"><span data-stu-id="2b1fb-119">To apply a transform in Direct2D, call the [**ID2D1RenderTarget::SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) method.</span></span> <span data-ttu-id="2b1fb-120">Questo metodo accetta una struttura [**d2d1 \_ Matrix \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) che definisce la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-120">This method takes a [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) structure that defines the transformation.</span></span> <span data-ttu-id="2b1fb-121">È possibile inizializzare questa struttura chiamando metodi sulla classe [**D2D1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) .</span><span class="sxs-lookup"><span data-stu-id="2b1fb-121">You can initialize this structure by calling methods on the [**D2D1::Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="2b1fb-122">Questa classe contiene metodi statici che restituiscono una matrice per ogni tipo di trasformazione:</span><span class="sxs-lookup"><span data-stu-id="2b1fb-122">This class contains static methods that return a matrix for each kind of transform:</span></span>

-   [<span data-ttu-id="2b1fb-123">**Matrix3x2F:: Rotation**</span><span class="sxs-lookup"><span data-stu-id="2b1fb-123">**Matrix3x2F::Rotation**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)
-   <span data-ttu-id="2b1fb-124">[**Matrix3x2F:: scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))</span><span class="sxs-lookup"><span data-stu-id="2b1fb-124">[**Matrix3x2F::Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))</span></span>
-   <span data-ttu-id="2b1fb-125">[**Matrix3x2F:: translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))</span><span class="sxs-lookup"><span data-stu-id="2b1fb-125">[**Matrix3x2F::Translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))</span></span>
-   [<span data-ttu-id="2b1fb-126">**Matrix3x2F:: asimmetria**</span><span class="sxs-lookup"><span data-stu-id="2b1fb-126">**Matrix3x2F::Skew**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)

<span data-ttu-id="2b1fb-127">Il codice seguente, ad esempio, applica una rotazione di 20 gradi intorno al punto (100, 100).</span><span class="sxs-lookup"><span data-stu-id="2b1fb-127">For example, the following code applies a 20-degree rotation around the point (100, 100).</span></span>


```C++
pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(20, D2D1::Point2F(100,100)));
```

<span data-ttu-id="2b1fb-128">La trasformazione viene applicata a tutte le operazioni di disegno successive fino a quando non si chiama di nuovo la [**trasformazione**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) .</span><span class="sxs-lookup"><span data-stu-id="2b1fb-128">The transform is applied to all later drawing operations until you call [**SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) again.</span></span> <span data-ttu-id="2b1fb-129">Per rimuovere la trasformazione corrente, chiamare **setransform** con la matrice di identità.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-129">To remove the current transform, call **SetTransform** with the identity matrix.</span></span> <span data-ttu-id="2b1fb-130">Per creare la matrice di identità, chiamare la funzione [**Matrix3x2F:: Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) .</span><span class="sxs-lookup"><span data-stu-id="2b1fb-130">To create the identity matrix, call the [**Matrix3x2F::Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) function.</span></span>


```C++
pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
```

## <a name="drawing-clock-hands"></a><span data-ttu-id="2b1fb-131">Disegno delle lancette dell'orologio</span><span class="sxs-lookup"><span data-stu-id="2b1fb-131">Drawing Clock Hands</span></span>

<span data-ttu-id="2b1fb-132">Si inseriranno le trasformazioni da usare convertendo il programma Circle in un orologio analogico.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-132">Let's put transforms to use by converting our Circle program into an analog clock.</span></span> <span data-ttu-id="2b1fb-133">A tale scopo, è possibile aggiungere linee per le mani.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-133">We can do this by adding lines for the hands.</span></span>

![screenshot del programma analogico.](images/graphics18.png)

<span data-ttu-id="2b1fb-135">Anziché calcolare le coordinate per le linee, è possibile calcolare l'angolo e quindi applicare una trasformazione di rotazione.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-135">Instead of calculating the coordinates for the lines, we can calculate the angle and then apply a rotation transform.</span></span> <span data-ttu-id="2b1fb-136">Il codice seguente illustra una funzione che disegna una mano di clock.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-136">The following code shows a function that draws one clock hand.</span></span> <span data-ttu-id="2b1fb-137">Il parametro *fAngle* restituisce l'angolo della mano, in gradi.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-137">The *fAngle* parameter gives the angle of the hand, in degrees.</span></span>

```C++
void Scene::DrawClockHand(float fHandLength, float fAngle, float fStrokeWidth)
{
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(fAngle, m_ellipse.point)
            );

    // endPoint defines one end of the hand.
    D2D_POINT_2F endPoint = D2D1::Point2F(
        m_ellipse.point.x,
        m_ellipse.point.y - (m_ellipse.radiusY * fHandLength)
        );

    // Draw a line from the center of the ellipse to endPoint.
    m_pRenderTarget->DrawLine(
        m_ellipse.point, endPoint, m_pStroke, fStrokeWidth);
}
```

<span data-ttu-id="2b1fb-138">Questo codice disegna una linea verticale, a partire dal centro del quadrante dell'orologio fino all' *endpoint* punto.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-138">This code draws a vertical line, starting from the center of the clock face and ending at the point *endPoint*.</span></span> <span data-ttu-id="2b1fb-139">La linea viene ruotata attorno al centro dell'ellisse applicando una trasformazione di rotazione.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-139">The line is rotated around the center of the ellipse by applying a rotation transform.</span></span> <span data-ttu-id="2b1fb-140">Il punto centrale della rotazione è il centro dell'ellisse che forma il quadrante dell'orologio.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-140">The center point for the rotation is the center of ellipse that forms the clock face.</span></span>

![diagramma che mostra la rotazione della mano di clock.](images/graphics19.png)

<span data-ttu-id="2b1fb-142">Il codice seguente illustra come viene disegnato l'intero quadrante.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-142">The following code shows how the whole clock face is drawn.</span></span>

```C++
void Scene::RenderScene()
{
    m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::SkyBlue));

    m_pRenderTarget->FillEllipse(m_ellipse, m_pFill);
    m_pRenderTarget->DrawEllipse(m_ellipse, m_pStroke);

    // Draw hands
    SYSTEMTIME time;
    GetLocalTime(&time);

    // 60 minutes = 30 degrees, 1 minute = 0.5 degree
    const float fHourAngle = (360.0f / 12) * (time.wHour) + (time.wMinute * 0.5f);
    const float fMinuteAngle =(360.0f / 60) * (time.wMinute);

    DrawClockHand(0.6f,  fHourAngle,   6);
    DrawClockHand(0.85f, fMinuteAngle, 4);

    // Restore the identity transformation.
    m_pRenderTarget->SetTransform( D2D1::Matrix3x2F::Identity() );
}
```

<span data-ttu-id="2b1fb-143">È possibile scaricare il progetto di Visual Studio completo dall' [esempio di clock Direct2D](direct2d-clock-sample.md).</span><span class="sxs-lookup"><span data-stu-id="2b1fb-143">You can download the complete Visual Studio project from [Direct2D Clock Sample](direct2d-clock-sample.md).</span></span> <span data-ttu-id="2b1fb-144">(Solo per divertimento, la versione di download aggiunge un effetto Gradiant radiale al quadrante).</span><span class="sxs-lookup"><span data-stu-id="2b1fb-144">(Just for fun, the download version adds a radial gradiant to the clock face.)</span></span>

## <a name="combining-transforms"></a><span data-ttu-id="2b1fb-145">Combinazione di trasformazioni</span><span class="sxs-lookup"><span data-stu-id="2b1fb-145">Combining Transforms</span></span>

<span data-ttu-id="2b1fb-146">Le quattro trasformazioni di base possono essere combinate moltiplicando due o più matrici.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-146">The four basic transforms can be combined by multiplying two or more matrices.</span></span> <span data-ttu-id="2b1fb-147">Il codice seguente, ad esempio, combina una rotazione con una traduzione.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-147">For example, the following code combines a rotation with a translation.</span></span>

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(20);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(40, 10);

pRenderTarget->SetTransform(rot * trans);
```

<span data-ttu-id="2b1fb-148">La classe [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) fornisce [**Operator \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) per la moltiplicazione di matrici.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-148">The [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class provides [**operator\*()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) for matrix multiplication.</span></span> <span data-ttu-id="2b1fb-149">L'ordine in cui si moltiplicano le matrici è importante.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-149">The order in which you multiply the matrices is important.</span></span> <span data-ttu-id="2b1fb-150">Impostando una trasformazione (M × N) si significa "applica M prima, seguito da N".</span><span class="sxs-lookup"><span data-stu-id="2b1fb-150">Setting a transform (M × N) means "Apply M first, followed by N."</span></span> <span data-ttu-id="2b1fb-151">Ecco ad esempio la rotazione seguita dalla traduzione:</span><span class="sxs-lookup"><span data-stu-id="2b1fb-151">For example, here is rotation followed by translation:</span></span>

![diagramma che mostra la rotazione seguita dalla conversione.](images/graphics20.png)

<span data-ttu-id="2b1fb-153">Ecco il codice per questa trasformazione:</span><span class="sxs-lookup"><span data-stu-id="2b1fb-153">Here is the code for this transform:</span></span>

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(rot * trans);
```

<span data-ttu-id="2b1fb-154">A questo punto, confrontare la trasformazione con una trasformazione nell'ordine inverso, la conversione seguita dalla rotazione.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-154">Now compare that transform with a transform in the reverse order, translation followed by rotation.</span></span>

![diagramma che mostra la traduzione seguita dalla rotazione.](images/graphics21.png)

<span data-ttu-id="2b1fb-156">La rotazione viene eseguita attorno al centro del rettangolo originale.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-156">The rotation is performed around the center of the original rectangle.</span></span> <span data-ttu-id="2b1fb-157">Ecco il codice per questa trasformazione.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-157">Here is the code for this transform.</span></span>

```C++
D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(trans * rot);
```

<span data-ttu-id="2b1fb-158">Come si può notare, le matrici sono uguali, ma l'ordine delle operazioni è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-158">As you can see, the matrices are the same, but the order of operations has changed.</span></span> <span data-ttu-id="2b1fb-159">Ciò si verifica perché la moltiplicazione di matrici non è commutativa: M × N ≠ N × M.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-159">This happens because matrix multiplication is not commutative: M × N ≠ N × M.</span></span>

## <a name="next"></a><span data-ttu-id="2b1fb-160">Prossima</span><span class="sxs-lookup"><span data-stu-id="2b1fb-160">Next</span></span>

[<span data-ttu-id="2b1fb-161">Appendice: trasformazioni matrice</span><span class="sxs-lookup"><span data-stu-id="2b1fb-161">Appendix: Matrix Transforms</span></span>](appendix--matrix-transforms.md)