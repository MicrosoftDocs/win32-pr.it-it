---
title: Cenni preliminari sulle trasformazioni
description: Viene introdotta l'API di trasformazione Direct2D Microsoft per Windows 7. Direct2D consente agli sviluppatori Win32 di eseguire trasformazioni grafiche 2D.
ms.assetid: eea8177d-c19e-4972-a9a6-ad5d541b090f
keywords:
- Direct2D, Cenni preliminari sulle trasformazioni
- Direct2D, sistemi di coordinate
- Direct2D, destinazioni di rendering
- Trasformazioni Direct2D, 2D
- trasformazioni 2D
- trasformazioni, informazioni
- trasformazioni, destinazioni di rendering
- trasformazioni, oggetti
- destinazioni di rendering, trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f3678f7b194f0f0188ed907a63737a97e9e58c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963130"
---
# <a name="transforms-overview"></a>Cenni preliminari sulle trasformazioni

In questo argomento vengono illustrate le nozioni di base delle trasformazioni Direct2D e sono inclusi esempi di diverse trasformazioni. Contiene le parti seguenti:

-   [Che cos'è una trasformazione Direct2D?](#what-is-a-direct2d-transform)
-   [Spazio delle coordinate Direct2D](#the-direct2d-coordinate-space)
-   [Creazione di matrici di trasformazione](#creating-transformation-matrices)
-   [Trasformazioni destinazione rendering](#rendering-target-transforms)
-   [Trasformazioni di pennelli](#brush-transforms)
-   [Trasformazioni geometriche](#geometry-transforms)
-   [Effetti della trasformazione di una destinazione di rendering sulle clip](#how-a-render-target-transform-affects-clips)
-   [Summary](#summary)
-   [Argomenti correlati](#related-topics)

## <a name="what-is-a-direct2d-transform"></a>Che cos'è una trasformazione Direct2D?

Una trasformazione specifica come eseguire il mapping dei punti di un oggetto da uno spazio delle coordinate a un altro o da una posizione a un'altra nello stesso spazio delle coordinate. Questo mapping è descritto da una matrice di trasformazione, definita come una raccolta di tre righe con tre colonne di valori FLOAT, come illustrato nella tabella seguente.



|                 |                 |     |
|-----------------|-----------------|-----|
| M11Default: 1,0 | M12Default: 0,0 | 0,0 |
| M21Default: 0,0 | M22Default: 1,0 | 0,0 |
| M31OffsetX: 0,0 | M32OffsetY: 0,0 | 1.0 |



 

In questa matrice i membri M11, M12, M21 e M22 definiscono una trasformazione lineare che può ridimensionare, ruotare o inclinare un oggetto; i membri OffsetX e OffsetY definiscono la traduzione da applicare dopo che è stata eseguita la trasformazione lineare. Per le trasformazioni affini, i valori della terza colonna sono sempre 0,0, 0,0 e 1,0.

Poiché Direct2D supporta solo le trasformazioni affini (lineari), la relativa matrice di trasformazione viene definita come matrice 3 per 2, omettendo la terza colonna dalla matrice di trasformazione precedente. Nella tabella seguente viene illustrato il layout della matrice di trasformazione Direct2D.



|                 |                 |
|-----------------|-----------------|
| M11Default: 1,0 | M12Default: 0,0 |
| M21Default: 0,0 | M22Default: 1,0 |
| M31OffsetX: 0,0 | M32OffsetY: 0,0 |



 

In Direct2D questa matrice 3 per 2 è rappresentata dalla struttura [**\_ \_ 3x2 della matrice d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) . Per semplificare le operazioni comuni della matrice, Direct2D fornisce anche una classe denominata [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f), derivata dalla struttura **\_ \_ 3x2 della matrice d2d1** .

Il costruttore predefinito per [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) lascia l'oggetto non inizializzato. Per recuperare una matrice di identità, usare [**Matrix3x2F:: Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix).

Quando una trasformazione identità viene applicata a un oggetto, non modifica la posizione, la forma o la dimensione dell'oggetto. È simile al modo in cui moltiplicare un numero per 1 non cambia il numero. In altre parole, la trasformazione identità lascia solo le coordinate dei punti e non sposta i punti in una nuova posizione. Qualsiasi trasformazione diversa dalla trasformazione identità modificherà la posizione, la forma e/o le dimensioni degli oggetti.

Le trasformazioni sono tutte informazioni sulle coordinate e la comprensione dello spazio delle coordinate Direct2D è importante per comprendere l'uso delle trasformazioni.

## <a name="the-direct2d-coordinate-space"></a>Spazio delle coordinate Direct2D

Direct2D utilizza uno spazio delle coordinate di sinistra; ovvero, i valori positivi dell'asse x aumentano a destra e i valori positivi dell'asse y aumentano verso il basso. Tutti gli elementi sullo schermo sono posizionati in relazione all'origine, ovvero il punto in cui l'asse x e l'asse y si intersecano (0,0), come illustrato nella figura seguente. Le destinazioni di rendering Direct2D utilizzano questo spazio delle coordinate.

![illustrazione degli assi x e y di uno spazio delle coordinate a sinistra](images/coordinatespace.png)

Modificando i valori in una matrice di trasformazione, è possibile ruotare, ridimensionare, inclinare e spostare (tradurre) un oggetto. Se, ad esempio, si imposta OffsetX su 100 e OffsetY su 200, si sposta l'oggetto a destra 100 pixel e giù 200 pixel.

Per mostrare l'effetto dello spostamento dell'oggetto, è necessario applicare la trasformazione conversione per eseguire il rendering di destinazioni, pennelli o geometrie. L'applicazione di una trasformazione a destinazioni di rendering influiscono sull'intero schermo, mentre l'applicazione di una trasformazione a un pennello o a una geometria influiscono solo su tale pennello o geometria. Per creare una matrice di trasformazione, utilizzare la classe [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) .

## <a name="creating-transformation-matrices"></a>Creazione di matrici di trasformazione

Per la creazione di trasformazioni di rotazione, scalabilità, asimmetria e conversione, la classe [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) fornisce i metodi statici indicati nella tabella seguente. Nella colonna esempio della tabella sono inclusi i collegamenti alle procedure che illustrano come utilizzare ogni metodo di trasformazione.



| Metodo                                                                   | Descrizione                                                                                                     | Esempio                                            | Illustrazione                                                                                                                            |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**matrix3x2f:: Rotate**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)                          | Crea una trasformazione di rotazione con l'angolo e il punto centrale specificati.                                | [come ruotare un oggetto](how-to-rotate.md)       | ![illustrazione di un quadrato ruotato di 45 gradi in senso orario rispetto al centro del quadrato originale](images/rotate-ovw.png)                 |
| [**matrix3x2f:: scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f)) | Crea una trasformazione di scala con i fattori di scala e il punto centrale specificati.                           | [come ridimensionare un oggetto](how-to-scale.md)         | ![illustrazione di un quadrato con scala 130%](images/scale-ovw.png)                                                                           |
| [**matrix3x2f:: asimmetria**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)                              | Crea una trasformazione inclinazione con i valori dell'asse x e y e il punto centrale specificati.                 | [come inclinare un oggetto](how-to-skew.md)           | ![illustrazione di un quadrato inclinato di 30 gradi in senso antiorario dall'asse y](images/skew-ovw.png)                                     |
| [**matrix3x2f:: translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))                | Crea una trasformazione di conversione e specifica gli spostamenti nella direzione dell'asse x e dell'asse y. | [come tradurre un oggetto](how-to-translate.md) | ![illustrazione di un quadrato spostato di 20 unità lungo l'asse x positivo e 10 unità lungo l'asse y positivo](images/translation-ovw.png) |



 

## <a name="rendering-target-transforms"></a>Trasformazioni destinazione rendering

Una destinazione di rendering è una risorsa che eredita dall'interfaccia [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) . Consente di creare risorse per il disegno e l'esecuzione di operazioni di disegno effettive. Fornisce inoltre metodi per la trasformazione dello spazio delle coordinate. È possibile chiamare il metodo [**ID2D1RenderTarget:: setransform**](id2d1rendertarget-settransform.md) per applicare la trasformazione specificata alla destinazione di rendering. Tutte le operazioni di disegno successive si verificano nello spazio trasformato.

Per eseguire il rendering del contenuto, usare i metodi di disegno della destinazione di rendering. Prima di iniziare il disegno, chiamare il metodo [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) . Per completare il rendering del contenuto, chiamare il metodo [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Per un esempio, vedere [come applicare più trasformazioni a un oggetto](how-to-apply-multiple-transforms.md).

## <a name="brush-transforms"></a>Trasformazioni di pennelli

È possibile modificare la trasformazione sul pennello chiamando [**setransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)). Per questa trasformazione è possibile considerare il pennello come una grande porzione di carta e le diverse primitive di rendering (testo, geometria, rettangolo e così via) come stencil. Quando si modifica la trasformazione del pennello, è come se si stesse scorrendo la porzione di carta di grandi dimensioni sotto lo stencil, senza modificare la posizione dello stencil. È possibile usare questa tecnica per far dissolvere il testo da giallo a nero, nello spazio 3D.

Quando la trasformazione del pennello è la trasformazione identità, i pennelli vengono visualizzati nello stesso spazio delle coordinate della destinazione di rendering in cui vengono disegnati. La trasformazione pennello consente a un chiamante di modificare il mapping delle coordinate del pennello a questo spazio.

Lo spazio del pennello viene specificato in modo diverso in Direct2D rispetto a Windows Presentation Foundation (WPF). In Direct2D lo spazio del pennello non è relativo all'oggetto da disegnare, ma è il sistema di coordinate corrente della destinazione di rendering, trasformato dalla trasformazione del pennello, se presente. Per fare in modo che il pennello riempia un oggetto come è stato fatto in WPF, è necessario convertire l'origine dello spazio del pennello nell'angolo superiore sinistro del rettangolo di delimitazione dell'oggetto, quindi ridimensionare lo spazio del pennello in modo che la tessera di base riempia il rettangolo di delimitazione dell'oggetto.

Per ulteriori informazioni sulle trasformazioni del pennello, vedere [Cenni preliminari sui pennelli Direct2D](direct2d-brushes-overview.md).

## <a name="geometry-transforms"></a>Trasformazioni geometriche

Quando si ridimensionano, spostano, traducono o inclinano le geometrie, è possibile applicare direttamente una trasformazione a una geometria specifica, non a una trasformazione di destinazione di rendering che influirà sull'intero schermo. Una trasformazione di destinazione di rendering influiscono in genere sul tratto e sul riempimento di una geometria. Al contrario, una trasformazione Geometry influisca solo sul riempimento di una geometria, perché la trasformazione viene applicata a una geometria prima che venga tracciata.

> [!Note]  
> A partire da Windows 8, la trasformazione globale non influisce sul tratto se si imposta il tipo di tratto sul tipo di [**\_ \_ trasformazioni \_ \_ d2d1 Stroke**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type) o [**d2d1 \_ Stroke \_ \_ \_**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).

 

È possibile modificare la trasformazione su una geometria chiamando [**ID2D1Factory:: CreateTransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) per creare un oggetto [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) . Per altre informazioni sulle trasformazioni Geometry, vedere [Cenni preliminari sulle geometrie Direct2D](direct2d-geometries-overview.md).

## <a name="how-a-render-target-transform-affects-clips"></a>Effetti della trasformazione di una destinazione di rendering sulle clip

La trasformazione in una destinazione di rendering influiscono sulla modalità di calcolo del rettangolo di selezione di una clip allineata all'asse. Quando viene chiamato [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) , il parametro *clipRect* viene trasformato dalla trasformazione globale corrente impostata nella destinazione di rendering. Dopo che la trasformazione è stata applicata a *clipRect*, viene calcolato il rettangolo di delimitazione allineato all'asse per il *clipRect* . Per maggiore efficienza, il contenuto viene ritagliato a questo rettangolo di delimitazione allineato all'asse e non alla *clipRect* originale passata. I diagrammi seguenti illustrano come viene applicata una trasformazione di rotazione alla destinazione di rendering, al *clipRect* risultante e a un rettangolo di delimitazione allineato all'asse calcolato.

1.  Si supponga che il rettangolo nella figura seguente sia una destinazione di rendering allineata ai pixel dello schermo.

    ![illustrazione di un rettangolo (destinazione di rendering)](images/pushaxisalignedclip-step1-rendertarget.png)

2.  Applicare una trasformazione di rotazione alla destinazione di rendering. Nella figura seguente il rettangolo nero rappresenta la destinazione di rendering originale e il rettangolo tratteggiato rosso rappresenta la destinazione di rendering trasformata.

    ![illustrazione del rettangolo originale e di un rettangolo ruotato (destinazione di rendering trasformato)](images/pushaxisalignedclip-step2-transformed.png)

3.  Dopo la chiamata di [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) , la trasformazione di rotazione viene applicata a *clipRect*. Nella figura seguente il rettangolo blu rappresenta il *clipRect* trasformato.

    ![illustrazione di un rettangolo blu più piccolo (clipRect) all'interno del rettangolo ruotato (destinazione di rendering trasformato)](images/pushaxisalignedclip-step3-cliprecttransformed.png)

4.  Viene calcolato il rettangolo di delimitazione allineato all'asse. Nell'illustrazione seguente il rettangolo tratteggiato verde rappresenta il riquadro delimitatore. Tutto il contenuto viene ritagliato in questo rettangolo di delimitazione allineato all'asse.

    ![illustrazione di un riquadro delimitatore verde sul piccolo rettangolo blu (clipRect)](images/pushaxisalignedclip-step4-boundingbox.png)

## <a name="summary"></a>Riepilogo

Direct2D semplifica la trasformazione di oggetti bidimensionali con spazi di coordinate semplificati e classi correlate. Utilizzando vari tipi di trasformazioni, è possibile tradurre, ruotare, inclinare e ridimensionare gli oggetti per ottenere molti effetti visivi impressionanti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento Direct2D](reference.md)
</dt> </dl>

 

 