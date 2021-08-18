---
title: Applicazione di trasformazioni in Direct2D
description: Applicazione di trasformazioni in Direct2D
ms.assetid: 4b54dcfc-f915-4e4a-aa88-ee23c341c2a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab83cb9a7981ada944de07e362c2f568889a84a4f90f2171150fbab948ab3a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388491"
---
# <a name="applying-transforms-in-direct2d"></a>Applicazione di trasformazioni in Direct2D

In [Drawing with Direct2D (Disegno con Direct2D)](drawing-with-direct2d.md)si è visto che il metodo [**ID2D1RenderTarget::FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) disegna un'ellisse allineata agli assi x e y. Ma si supponga di voler disegnare un'ellisse inclinata in un angolo?

![immagine che mostra un'ellisse inclinata.](images/graphics16.png)

Usando le trasformazioni, è possibile modificare una forma nei modi seguenti.

-   Rotazione intorno a un punto.
-   Ridimensionamento.
-   Traslazione (spostamento nella direzione X o Y).
-   A inclinazione (nota anche come *inclinazione).*

Una trasformazione è un'operazione matematica che esegue il mapping di un set di punti a un nuovo set di punti. Ad esempio, il diagramma seguente mostra un triangolo ruotato intorno al punto P3. Dopo l'applicazione della rotazione, il punto P1 viene mappato a P1', il punto P2 viene mappato a P2' e il punto P3 viene mappato a se stesso.

![diagramma che mostra la rotazione intorno a un punto.](images/graphics17.png)

Le trasformazioni vengono implementate tramite matrici. Tuttavia, non è necessario comprendere la matematica delle matrici per poterle usare. Per altre informazioni sui calcoli matematici, vedere [Appendice: Trasformazioni di matrice.](appendix--matrix-transforms.md)

Per applicare una trasformazione in Direct2D, chiama il [**metodo ID2D1RenderTarget::SetTransform.**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) Questo metodo accetta una [**struttura D2D1 \_ MATRIX \_ 3X2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) che definisce la trasformazione. È possibile inizializzare questa struttura chiamando metodi sulla [**classe D2D1::Matrix3x2F.**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) Questa classe contiene metodi statici che restituiscono una matrice per ogni tipo di trasformazione:

-   [**Matrix3x2F::Rotation**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)
-   [**Matrix3x2F::Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))
-   [**Matrix3x2F::Translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))
-   [**Matrix3x2F::Skew**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)

Ad esempio, il codice seguente applica una rotazione di 20 gradi intorno al punto (100, 100).


```C++
pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(20, D2D1::Point2F(100,100)));
```

La trasformazione viene applicata a tutte le operazioni di disegno successive fino a quando non si [**chiama nuovamente SetTransform.**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) Per rimuovere la trasformazione corrente, chiamare **SetTransform** con la matrice di identità. Per creare la matrice di identità, chiamare [**la funzione Matrix3x2F::Identity.**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix)


```C++
pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
```

## <a name="drawing-clock-hands"></a>Disegnare le mani dell'orologio

Inserire le trasformazioni da usare convertendo il programma Circle in un orologio analogo. A tale scopo, è possibile aggiungere linee per le mani.

![screenshot del programma di orologio analogo.](images/graphics18.png)

Invece di calcolare le coordinate per le linee, è possibile calcolare l'angolo e quindi applicare una trasformazione di rotazione. Il codice seguente illustra una funzione che disegna una mano dell'orologio. Il *parametro fAngle* fornisce l'angolo della mano, in gradi.

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

Questo codice disegna una linea verticale, a partire dal centro del viso dell'orologio e terminando in corrispondenza del *punto endPoint*. La linea viene ruotata intorno al centro dell'ellisse applicando una trasformazione di rotazione. Il punto centrale per la rotazione è il centro dell'ellisse che forma la faccia dell'orologio.

![diagramma che mostra la rotazione della mano dell'orologio.](images/graphics19.png)

Nel codice seguente viene illustrato come viene disegnata l'intera faccia dell'orologio.

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

È possibile scaricare il progetto completo Visual Studio esempio di [orologio Direct2D.](direct2d-clock-sample.md) Solo per essere divertente, la versione di download aggiunge un gradimento radiale alla faccia dell'orologio.

## <a name="combining-transforms"></a>Combinazione di trasformazioni

Le quattro trasformazioni di base possono essere combinate moltiplicando due o più matrici. Ad esempio, il codice seguente combina una rotazione con una traslazione.

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(20);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(40, 10);

pRenderTarget->SetTransform(rot * trans);
```

La [**classe Matrix3x2F fornisce**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) [**l'operatore \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) per la moltiplicazione di matrici. L'ordine in cui si moltiplicano le matrici è importante. L'impostazione di una trasformazione (M × N) significa "Applica prima M, seguito da N". Ad esempio, ecco la rotazione seguita dalla traslazione:

![diagramma che mostra la rotazione seguita dalla traslazione.](images/graphics20.png)

Ecco il codice per questa trasformazione:

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(rot * trans);
```

Confrontare ora tale trasformazione con una trasformazione nell'ordine inverso, traslazione seguita dalla rotazione.

![diagramma che mostra la traslazione seguita dalla rotazione.](images/graphics21.png)

La rotazione viene eseguita intorno al centro del rettangolo originale. Ecco il codice per questa trasformazione.

```C++
D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(trans * rot);
```

Come si può vedere, le matrici sono uguali, ma l'ordine delle operazioni è cambiato. Ciò si verifica perché la moltiplicazione della matrice non è commutativa: M × N ≠ N × M.

## <a name="next"></a>Prossima

[Appendice: Trasformazioni di matrice](appendix--matrix-transforms.md)