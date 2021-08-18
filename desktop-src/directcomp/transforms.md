---
title: Trasformazioni (DirectComposition)
description: Questo argomento illustra il supporto di Microsoft DirectComposition per trasformazioni affine (lineari) bidimensionali (2D) e descrive i tipi di trasformazioni supportati da DirectComposition.
ms.assetid: a0f41cc6-e848-4831-8063-609e17d9b4c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c8cc34975ab8304300a1523269808775107f4ce0554432da8c3c04a01f25881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504811"
---
# <a name="transforms-directcomposition"></a>Trasformazioni (DirectComposition)

> [!NOTE]
> Per le app Windows 10, è consigliabile usare le API Windows.UI.Composition anziché DirectComposition. Per altre informazioni, vedi [Modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).

Questo argomento illustra il supporto di Microsoft DirectComposition per trasformazioni affine (lineari) bidimensionali (2D) e descrive i tipi di trasformazioni supportati da DirectComposition.

DirectComposition supporta anche trasformazioni prospettica 3D, ma poiché richiedono la creazione di una bitmap intermedia, DirectComposition le considera effetti anziché trasformazioni. Per informazioni sugli effetti di trasformazione prospettica 3D, vedere [Effetti.](effects.md)

Questo argomento include le sezioni seguenti:

-   [Che cos'è una trasformazione DirectComposition 2D?](#what-is-a-directcomposition-2d-transform)
-   [Spazio delle coordinate 2D DirectComposition](#the-directcomposition-2d-coordinate-space)
-   [Supporto per trasformazioni 2D affine](#support-for-affine-2d-transforms)
-   [Trasformazioni matrix 2D](#matrix-2d-transforms)
-   [Trasforma gruppi](#transform-groups)
-   [Animazione Transform](#transform-animation)
-   [Argomenti correlati](#related-topics)

## <a name="what-is-a-directcomposition-2d-transform"></a>Che cos'è una trasformazione DirectComposition 2D?

Una trasformazione 2D consente di modificare la posizione, le dimensioni o la natura di un oggetto visivo in due dimensioni spostando l'oggetto visivo in un'altra posizione (traslazione), rendendolo più grande o più piccolo (ridimensionamento), ruotando (rotazione) o distorcendo la forma (inclinazione).

Una trasformazione 2D viene ottenuta tramite il mapping dei punti di un oggetto visivo da una posizione a un'altra all'interno dello stesso spazio delle coordinate o da uno spazio delle coordinate a un altro. Questo mapping è descritto da una tabella di valori denominata matrice di trasformazione, definita come raccolta di tre righe con tre colonne di valori a virgola mobile, come illustrato nella tabella seguente.

:::row:::
    :::column:::
        M11Default: 1.0<br/>
        M21Default: 0.0<br/>
        M31OffsetX: 0.0
    :::column-end:::
    :::column:::
        M12Default: 0.0<br/>
        M22Default: 1.0<br/>
        M32OffsetY: 0.0
    :::column-end:::
    :::column:::
        0,0<br/>
        0,0<br/>
        1.0
    :::column-end:::
:::row-end:::

La matrice di trasformazione per le trasformazioni 2D affine è una matrice 3 per 2 che omette la terza colonna dalla matrice di trasformazione precedente. Nella tabella seguente viene illustrato il layout di questa matrice.

:::row:::
    :::column:::
        M11Default: 1.0<br/>
        M21Default: 0.0<br/>
        M31OffsetX: 0.0
    :::column-end:::
    :::column:::
        M12Default: 0.0<br/>
        M22Default: 1.0<br/>
        M32OffsetY: 0.0
    :::column-end:::
:::row-end:::

> [!Note]  
> DirectComposition non esegue alcuna elaborazione speciale quando si applicano trasformazioni 2D a contenuto stereo. Ciò significa che il contenuto 3D potrebbe apparire distorto quando vi viene applicata una trasformazione 2D.

 

## <a name="the-directcomposition-2d-coordinate-space"></a>Spazio delle coordinate 2D DirectComposition

DirectComposition usa uno spazio delle coordinate 2D mancino; ciò significa che i valori positivi dell'asse x aumentano verso destra e i valori positivi dell'asse y aumentano verso il basso. Gli oggetti visivi vengono posizionati in relazione all'origine, ovvero il punto in cui si intersecano l'asse x e l'asse y (0, 0), come illustrato nella figura seguente.

![l'asse x e l'asse y di uno spazio delle coordinate a sinistra](images/coordinatespace.png)

Modificando i valori in una matrice di trasformazione 3 per 2, è possibile ruotare, ridimensionare, inclinare e traslare un oggetto in due dimensioni. Ad esempio, se si imposta OffsetX su 100 e OffsetY su 200, si sposta l'oggetto a destra di 100 pixel e verso il basso di 200 pixel.

## <a name="support-for-affine-2d-transforms"></a>Supporto per trasformazioni 2D affine

La tabella seguente descrive i tipi di trasformazioni 2D affine supportate da DirectComposition ed elenca le interfacce che è possibile usare per eseguire i vari tipi di trasformazioni.



| Trasformazione/interfaccia                                                                               | Descrizione                                                                                              | Illustrazione                                                                                                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Ruotare la nuova riga [**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)2D \[\]          | ruota un oggetto visivo in base all'angolo specificato intorno al punto centrale specificato.                                 | ![illustrazione di un quadrato ruotato di 45 gradi in senso orario intorno al centro del quadrato originale](images/rotate.png)               |
| Scala 2D [**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform) \[ newline\]             | Ridimensiona un oggetto visivo in base al fattore specificato in base al punto centrale specificato.                                 | ![illustrazione di un quadrato ridimensionato del 130%](images/scale.png)                                                                  |
| Skew 2D [**idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform) \[ newline\]                | inclina un oggetto visivo in base all'angolo specificato lungo l'asse x e l'asse y e intorno al punto centrale specificato. | ![illustrazione di un quadrato a inclinazione di 30 gradi in senso antiorario rispetto all'asse y](images/skew.png)                                   |
| Convert 2D [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) \[ newline\] | modificare la posizione di un oggetto visivo nella direzione dell'asse x e dell'asse y.                               | ![illustrazione di un quadrato spostato di 20 unità lungo l'asse x positivo e di 10 unità lungo l'asse y positivo](images/translate.png) |



 

## <a name="matrix-2d-transforms"></a>Trasformazioni matrix 2D

[**L'interfaccia IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) consente di definire la propria matrice di trasformazione 2D affine 3 per 2 e applicarla a un oggetto visivo. Questa interfaccia è utile se è necessario applicare un tipo di trasformazione 2D affine che non è disponibile tramite le altre interfacce di trasformazione DirectComposition. Per definire la matrice, compilare una struttura [**D2D \_ MATRIX \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) e passarla al [**metodo IDCompositionMatrixTransform::SetMatrix.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix)

## <a name="transform-groups"></a>Trasforma gruppi

È possibile usare i gruppi di trasformazioni per combinare più trasformazioni in un'unica trasformazione. Un gruppo di trasformazioni definisce una raccolta di oggetti transform le cui matrici vengono moltiplicate insieme nell'ordine in cui sono specificate nella raccolta. La matrice di trasformazione risultante viene quindi applicata all'oggetto visivo. Un gruppo di trasformazioni produce lo stesso risultato dell'applicazione separata di ogni trasformazione.

Tenere presente che l'ordine degli oggetti di trasformazione in un gruppo di trasformazioni è importante. Ad esempio, se un oggetto visivo viene prima ruotato, quindi ridimensionato e quindi convertito, il risultato è diverso da se l'oggetto visivo viene prima convertito, quindi ruotato e quindi ridimensionato. DirectComposition applica sempre le trasformazioni a un oggetto visivo nell'ordine in cui sono specificate nella raccolta.

Per creare un gruppo di trasformazioni, creare prima di tutto gli oggetti di trasformazione da includere nel gruppo e quindi passare una matrice di puntatori agli oggetti di trasformazione al [**metodo IDCompositionDevice::CreateTransformGroup.**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) Dopo aver creato un gruppo di trasformazioni, non è possibile aggiungere o rimuovere oggetti di trasformazione. Tuttavia, è possibile modificare le proprietà dei singoli oggetti transform nella raccolta e le modifiche verranno riflesse nella matrice di trasformazione risultante.

## <a name="transform-animation"></a>Animazione Transform

È possibile animare le proprietà di una trasformazione. Quando una proprietà viene animata, DirectComposition modifica il valore della proprietà nel tempo, anziché tutti contemporaneamente. Ciò è particolarmente utile quando si creano transizioni. Per altre informazioni, vedere [Animazione.](animation.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi a DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 
