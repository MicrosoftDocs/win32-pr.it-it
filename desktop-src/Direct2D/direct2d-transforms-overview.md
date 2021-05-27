---
title: Cenni preliminari sulle trasformazioni
description: Introduce l'API di trasformazione Microsoft Direct2D per Windows 7. Direct2D consente agli sviluppatori Win32 di eseguire trasformazioni grafiche 2D.
ms.assetid: eea8177d-c19e-4972-a9a6-ad5d541b090f
keywords:
- Direct2D, panoramica delle trasformazioni
- Direct2D, sistemi di coordinate
- Direct2D, destinazioni di rendering
- Trasformazioni Direct2D,2D
- Trasformazioni 2D
- trasformazioni,informazioni
- trasformazioni, destinazioni di rendering
- trasformazioni,oggetti
- destinazioni di rendering, trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b924c51d73e71f206fbb250f4a7dd50ca71db2a
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549146"
---
# <a name="transforms-overview"></a>Cenni preliminari sulle trasformazioni

Questo argomento illustra le nozioni di base delle trasformazioni Direct2D e include esempi di varie trasformazioni. Contiene le parti seguenti:

-   [Che cos'è una trasformazione Direct2D?](#what-is-a-direct2d-transform)
-   [Spazio delle coordinate Direct2D](#the-direct2d-coordinate-space)
-   [Creazione di matrici di trasformazione](#creating-transformation-matrices)
-   [Rendering delle trasformazioni di destinazione](#rendering-target-transforms)
-   [Trasformazioni dei pennelli](#brush-transforms)
-   [Trasformazioni geometry](#geometry-transforms)
-   [Effetto di una trasformazione destinazione di rendering sulle clip](#how-a-render-target-transform-affects-clips)
-   [Summary](#summary)
-   [Argomenti correlati](#related-topics)

## <a name="what-is-a-direct2d-transform"></a>Che cos'è una trasformazione Direct2D?

Una trasformazione specifica come eseguire il mapping dei punti di un oggetto da uno spazio delle coordinate a un altro o da una posizione a un'altra all'interno dello stesso spazio delle coordinate. Questo mapping è descritto da una matrice di trasformazione, definita come raccolta di tre righe con tre colonne di valori FLOAT, come illustrato nella tabella seguente.



|    &nbsp;       |       &nbsp;    |  &nbsp; |
|-----------------|-----------------|-----|
| M11Default: 1.0 | M12Default: 0.0 | 0,0 |
| M21Default: 0.0 | M22Default: 1.0 | 0,0 |
| M31OffsetX: 0.0 | M32OffsetY: 0.0 | 1.0 |



 

In questa matrice i membri M11, M12, M21 e M22 definiscono una trasformazione lineare che può ridimensionare, ruotare o inclinare un oggetto; I membri OffsetX e OffsetY definiscono la traslazione da applicare dopo l'applicazione della trasformazione lineare. Per le trasformazioni affine, i valori nella terza colonna sono sempre 0.0, 0.0 e 1.0.

Poiché Direct2D supporta solo trasformazioni affine (lineari), la relativa matrice di trasformazione è definita come matrice 3 per 2, omettendo la terza colonna dalla matrice di trasformazione precedente. La tabella seguente illustra il layout della matrice di trasformazione Direct2D.



|    &nbsp;       |       &nbsp;    | 
|-----------------|-----------------|
| M11Default: 1.0 | M12Default: 0.0 |
| M21Default: 0.0 | M22Default: 1.0 |
| M31OffsetX: 0.0 | M32OffsetY: 0.0 |



 

In Direct2D questa matrice 3 per 2 è rappresentata dalla [**struttura D2D1 \_ MATRIX \_ 3X2.**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) Per semplificare le operazioni comuni della matrice, Direct2D fornisce anche una classe denominata [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f), derivata dalla struttura **D2D1 \_ MATRIX \_ 3X2.**

Il costruttore predefinito per [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) lascia l'oggetto non inizializzato. Per recuperare una matrice di identità, [**usare Matrix3x2F::Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix).

Quando una trasformazione di identità viene applicata a un oggetto, non modifica la posizione, la forma o le dimensioni dell'oggetto. È simile al modo in cui la moltiplicazione di un numero per 1 non modifica il numero. In altre parole, la trasformazione dell'identità lascia sole le coordinate dei punti e non sposta i punti in una nuova posizione. Qualsiasi trasformazione diversa dalla trasformazione identity modificherà la posizione, la forma e/o le dimensioni degli oggetti.

Le trasformazioni riguardano tutte le coordinate e comprendere lo spazio delle coordinate Direct2D è importante per comprendere l'uso delle trasformazioni.

## <a name="the-direct2d-coordinate-space"></a>Spazio delle coordinate Direct2D

Direct2D usa uno spazio delle coordinate a sinistra; in altri, i valori positivi dell'asse X aumentano verso destra e i valori positivi dell'asse y aumentano verso il basso. Tutti gli elementi sullo schermo vengono posizionati rispetto all'origine, ovvero il punto in cui si intersecano l'asse x e l'asse y (0, 0), come illustrato nella figura seguente. Le destinazioni di rendering Direct2D usano questo spazio delle coordinate.

![illustrazione dell'asse x e dell'asse y di uno spazio delle coordinate mancino](images/coordinatespace.png)

Modificando i valori in una matrice di trasformazione, è possibile ruotare, ridimensionare, inclinare e spostare (traslare) un oggetto. Ad esempio, se si imposta OffsetX su 100 e OffsetY su 200, si sposta l'oggetto a destra di 100 pixel e verso il basso di 200 pixel.

Per mostrare l'effetto dello spostamento dell'oggetto, è necessario applicare la trasformazione traduzione per eseguire il rendering di destinazioni, pennelli o geometrie. L'applicazione di una trasformazione alle destinazioni di rendering influisce sull'intero schermo, mentre l'applicazione di una trasformazione a un pennello o a una geometria influisce solo su quel pennello o geometria specifico. Per creare una matrice di trasformazione, usare la [**classe Matrix3x2F.**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f)

## <a name="creating-transformation-matrices"></a>Creazione di matrici di trasformazione

Per la creazione di trasformazioni di rotazione, scala, inclinazione e traslazione, la [**classe Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) fornisce i metodi statici illustrati nella tabella seguente. La colonna Esempio della tabella contiene collegamenti agli argomenti delle procedure che illustrano come usare ogni metodo di trasformazione.



| Metodo                                                                   | Descrizione                                                                                                     | Esempio                                            | Illustrazione                                                                                                                            |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**matrix3x2f::rotate**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)                          | crea una trasformazione di rotazione con l'angolo e il punto centrale specificati.                                | [come ruotare un oggetto](how-to-rotate.md)       | ![illustrazione di un quadrato ruotato di 45 gradi in senso orario intorno al centro del quadrato originale](images/rotate-ovw.png)                 |
| [**matrix3x2f::scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f)) | crea una trasformazione della scala con i fattori di scala e il punto centrale specificati.                           | [come ridimensionare un oggetto](how-to-scale.md)         | ![illustrazione di un quadrato ridimensionato del 130%](images/scale-ovw.png)                                                                           |
| [**matrix3x2f::skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)                              | crea una trasformazione a inclinazione con i valori dell'asse x e dell'asse y e il punto centrale specificati.                 | [come inclinare un oggetto](how-to-skew.md)           | ![illustrazione di un quadrato a inclinazione di 30 gradi in senso antiorario rispetto all'asse y](images/skew-ovw.png)                                     |
| [**matrix3x2f::translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))                | crea una trasformazione di traslazione e specifica gli spostamenti nella direzione dell'asse x e dell'asse y. | [come traslare un oggetto](how-to-translate.md) | ![illustrazione di un quadrato spostato di 20 unità lungo l'asse x positivo e di 10 unità lungo l'asse y positivo](images/translation-ovw.png) |



 

## <a name="rendering-target-transforms"></a>Rendering delle trasformazioni di destinazione

Una destinazione di rendering è una risorsa che eredita [**dall'interfaccia ID2D1RenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) Crea risorse per il disegno ed esegue operazioni di disegno effettive. Fornisce anche metodi per trasformare lo spazio delle coordinate. È possibile chiamare il [**metodo ID2D1RenderTarget::SetTransform**](id2d1rendertarget-settransform.md) per applicare la trasformazione specificata alla destinazione di rendering. Tutte le operazioni di disegno successive vengono eseguite nello spazio trasformato.

Per eseguire il rendering del contenuto, usare i metodi di disegno della destinazione di rendering. Prima di iniziare a disegnare, chiamare il [**metodo BeginDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) Per completare il rendering del contenuto, chiamare il [**metodo EndDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) Per un esempio, vedere [Come applicare più trasformazioni a un oggetto](how-to-apply-multiple-transforms.md).

## <a name="brush-transforms"></a>Trasformazioni dei pennelli

È possibile regolare la trasformazione sul pennello chiamando [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)). Per questa trasformazione, è possibile pensare al pennello come a un foglio di carta di grandi dimensioni e alle diverse primitive di rendering (testo, geometria, rettangolo e così via) come stencil. Quando si regola la trasformazione del pennello, è come se si scorre il foglio di carta grande sotto lo stencil, senza modificare la posizione dello stencil stesso. È possibile usare questa tecnica per rendere il testo dissolvenza dal giallo al nero nello spazio 3D.

Quando la trasformazione del pennello è la trasformazione di identità, i pennelli vengono visualizzati nello stesso spazio delle coordinate della destinazione di rendering in cui vengono disegnati. La trasformazione del pennello consente a un chiamante di modificare il mapping delle coordinate del pennello a questo spazio.

Lo spazio del pennello viene specificato in modo diverso in Direct2D rispetto a Windows Presentation Foundation (WPF). In Direct2D, lo spazio del pennello non è relativo all'oggetto disegnato, ma è il sistema di coordinate corrente della destinazione di rendering, trasformato dalla trasformazione del pennello, se presente. Per fare in modo che il pennello riempia un oggetto come è stato fatto in WPF, è necessario convertire l'origine dello spazio del pennello nell'angolo superiore sinistro del rettangolo di selezione dell'oggetto e quindi ridimensionare lo spazio del pennello in modo che il riquadro di base riempia il rettangolo di selezione dell'oggetto.

Per altre informazioni sulle trasformazioni dei pennelli, vedere [Cenni preliminari sui pennelli Direct2D.](direct2d-brushes-overview.md)

## <a name="geometry-transforms"></a>Trasformazioni geometriche

Quando si ridimensionano, spostano, traslano o inclinano le geometrie, è possibile applicare direttamente una trasformazione a una geometria specifica, non a una trasformazione di destinazione di rendering che influisce sull'intero schermo. Una trasformazione di destinazione di rendering influisce in genere sul tratto e sul riempimento di una geometria. Al contrario, una trasformazione geometrica influisce solo sul riempimento di una geometria, perché la trasformazione viene applicata a una geometria prima che venga tracciata.

> [!Note]  
> A partire Windows 8, la trasformazione del mondo non influisce sul tratto se si imposta il tipo di tratto su D2D1 STROKE TRANSFORM TYPE FIXED (TIPO DI TRASFORMAZIONE TRATTO [**D2D1 \_ \_ \_ \_ FIXED)**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type) o D2D1 STROKE TRANSFORM TYPE (TIPO DI TRASFORMAZIONE TRATTO [**D2D1) \_ \_ \_ \_ .**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)

 

È possibile modificare la trasformazione su una geometria chiamando [**ID2D1Factory::CreateTransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) per creare un [**oggetto ID2D1TransformedGeometry.**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) Per altre informazioni sulle trasformazioni geometriche, vedere [Cenni preliminari sulle geometrie Direct2D.](direct2d-geometries-overview.md)

## <a name="how-a-render-target-transform-affects-clips"></a>Effetti di una trasformazione di destinazione di rendering sulle clip

La trasformazione in una destinazione di rendering influisce sul modo in cui viene calcolato il rettangolo di selezione di una clip allineata all'asse. Quando viene [**chiamato PushAxisAlignedClip,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) il parametro *clipRect* viene trasformato dalla trasformazione world corrente impostata nella destinazione di rendering. Dopo che la trasformazione è stata applicata a *clipRect,* viene calcolato il rettangolo di selezione allineato all'asse per *clipRect.* Per migliorare l'efficienza, il contenuto viene ritagliato in base a questo rettangolo di selezione allineato all'asse e non all'oggetto *clipRect* originale passato. I diagrammi seguenti illustrano come viene applicata una trasformazione di rotazione alla destinazione di rendering, all'oggetto *clipRect* risultante e a un rettangolo di selezione calcolato allineato all'asse.

1.  Si supponga che il rettangolo nella figura seguente sia una destinazione di rendering allineata ai pixel dello schermo.

    ![illustrazione di un rettangolo (destinazione di rendering)](images/pushaxisalignedclip-step1-rendertarget.png)

2.  Applicare una trasformazione di rotazione alla destinazione di rendering. Nella figura seguente il rettangolo nero rappresenta la destinazione di rendering originale e il rettangolo tratteggiato rosso rappresenta la destinazione di rendering trasformata.

    ![Illustrazione del rettangolo originale e di un rettangolo ruotato (destinazione di rendering trasformata)](images/pushaxisalignedclip-step2-transformed.png)

3.  Dopo [**aver chiamato PushAxisAlignedClip,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) la trasformazione di rotazione viene applicata a *clipRect*. Nella figura seguente il rettangolo blu rappresenta l'oggetto *clipRect trasformato.*

    ![Illustrazione di un rettangolo blu più piccolo (cliprect) all'interno del rettangolo ruotato (destinazione di rendering trasformata)](images/pushaxisalignedclip-step3-cliprecttransformed.png)

4.  Viene calcolato il rettangolo di selezione allineato all'asse. Nella figura seguente il rettangolo tratteggiato verde rappresenta il rettangolo di selezione. Tutto il contenuto viene ritagliato in questo rettangolo di selezione allineato all'asse.

    ![Illustrazione di un rettangolo di selezione verde sul piccolo rettangolo blu (cliprect)](images/pushaxisalignedclip-step4-boundingbox.png)

## <a name="summary"></a>Riepilogo

Direct2D semplifica la trasformazione di oggetti bidimensionali con spazi di coordinate semplificati e classi correlate. Usando vari tipi di trasformazioni, è possibile traslare, ruotare, inclinare e ridimensionare gli oggetti per ottenere molti effetti visivi straordinari.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su Direct2D](reference.md)
</dt> </dl>

 

 