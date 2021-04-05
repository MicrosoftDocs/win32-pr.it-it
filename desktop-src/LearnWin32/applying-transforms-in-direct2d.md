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
# <a name="applying-transforms-in-direct2d"></a>Applicazione di trasformazioni in Direct2D

Nel [disegno con Direct2D](drawing-with-direct2d.md)è stato rilevato che il metodo [**ID2D1RenderTarget:: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) disegna un'ellisse allineata agli assi x e y. Ma si supponga di voler creare un'ellisse inclinata in un angolo?

![immagine che mostra un'ellisse inclinata.](images/graphics16.png)

Utilizzando le trasformazioni, è possibile modificare una forma nei modi seguenti.

-   Rotazione intorno a un punto.
-   Ridimensionamento.
-   Traduzione (spostamento nella direzione X o Y).
-   Asimmetria (anche nota come *cesoia*).

Una trasformazione è un'operazione matematica che esegue il mapping di un set di punti a un nuovo set di punti. Il diagramma seguente, ad esempio, Mostra un triangolo ruotato intorno al punto P3. Dopo l'applicazione della rotazione, il punto P1 viene mappato a P1', il punto P2 viene mappato a P2' e il punto P3 viene mappato a se stesso.

![diagramma che mostra la rotazione intorno a un punto.](images/graphics17.png)

Le trasformazioni vengono implementate tramite matrici. Non è tuttavia necessario comprendere la matematica delle matrici per utilizzarle. Per ulteriori informazioni sui calcoli matematici, vedere [Appendice: trasformazioni matrice](appendix--matrix-transforms.md).

Per applicare una trasformazione in Direct2D, chiamare il metodo [**ID2D1RenderTarget:: setransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) . Questo metodo accetta una struttura [**d2d1 \_ Matrix \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) che definisce la trasformazione. È possibile inizializzare questa struttura chiamando metodi sulla classe [**D2D1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) . Questa classe contiene metodi statici che restituiscono una matrice per ogni tipo di trasformazione:

-   [**Matrix3x2F:: Rotation**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)
-   [**Matrix3x2F:: scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))
-   [**Matrix3x2F:: translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))
-   [**Matrix3x2F:: asimmetria**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)

Il codice seguente, ad esempio, applica una rotazione di 20 gradi intorno al punto (100, 100).


```C++
pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(20, D2D1::Point2F(100,100)));
```

La trasformazione viene applicata a tutte le operazioni di disegno successive fino a quando non si chiama di nuovo la [**trasformazione**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) . Per rimuovere la trasformazione corrente, chiamare **setransform** con la matrice di identità. Per creare la matrice di identità, chiamare la funzione [**Matrix3x2F:: Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) .


```C++
pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
```

## <a name="drawing-clock-hands"></a>Disegno delle lancette dell'orologio

Si inseriranno le trasformazioni da usare convertendo il programma Circle in un orologio analogico. A tale scopo, è possibile aggiungere linee per le mani.

![screenshot del programma analogico.](images/graphics18.png)

Anziché calcolare le coordinate per le linee, è possibile calcolare l'angolo e quindi applicare una trasformazione di rotazione. Il codice seguente illustra una funzione che disegna una mano di clock. Il parametro *fAngle* restituisce l'angolo della mano, in gradi.

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

Questo codice disegna una linea verticale, a partire dal centro del quadrante dell'orologio fino all' *endpoint* punto. La linea viene ruotata attorno al centro dell'ellisse applicando una trasformazione di rotazione. Il punto centrale della rotazione è il centro dell'ellisse che forma il quadrante dell'orologio.

![diagramma che mostra la rotazione della mano di clock.](images/graphics19.png)

Il codice seguente illustra come viene disegnato l'intero quadrante.

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

È possibile scaricare il progetto di Visual Studio completo dall' [esempio di clock Direct2D](direct2d-clock-sample.md). (Solo per divertimento, la versione di download aggiunge un effetto Gradiant radiale al quadrante).

## <a name="combining-transforms"></a>Combinazione di trasformazioni

Le quattro trasformazioni di base possono essere combinate moltiplicando due o più matrici. Il codice seguente, ad esempio, combina una rotazione con una traduzione.

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(20);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(40, 10);

pRenderTarget->SetTransform(rot * trans);
```

La classe [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) fornisce [**Operator \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) per la moltiplicazione di matrici. L'ordine in cui si moltiplicano le matrici è importante. Impostando una trasformazione (M × N) si significa "applica M prima, seguito da N". Ecco ad esempio la rotazione seguita dalla traduzione:

![diagramma che mostra la rotazione seguita dalla conversione.](images/graphics20.png)

Ecco il codice per questa trasformazione:

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(rot * trans);
```

A questo punto, confrontare la trasformazione con una trasformazione nell'ordine inverso, la conversione seguita dalla rotazione.

![diagramma che mostra la traduzione seguita dalla rotazione.](images/graphics21.png)

La rotazione viene eseguita attorno al centro del rettangolo originale. Ecco il codice per questa trasformazione.

```C++
D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(trans * rot);
```

Come si può notare, le matrici sono uguali, ma l'ordine delle operazioni è stato modificato. Ciò si verifica perché la moltiplicazione di matrici non è commutativa: M × N ≠ N × M.

## <a name="next"></a>Prossima

[Appendice: trasformazioni matrice](appendix--matrix-transforms.md)