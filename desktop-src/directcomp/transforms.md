---
title: Trasformazioni (DirectComposition)
description: In questo argomento viene illustrato il supporto di Microsoft DirectComposition per le trasformazioni affini (lineari) bidimensionali (2D) e vengono descritti i tipi di trasformazioni supportati da DirectComposition.
ms.assetid: a0f41cc6-e848-4831-8063-609e17d9b4c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27a1fec5774d208f240e6d2f1c8b7df09d25c486
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104555293"
---
# <a name="transforms-directcomposition"></a>Trasformazioni (DirectComposition)

> [!NOTE]
> Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition. Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).

In questo argomento viene illustrato il supporto di Microsoft DirectComposition per le trasformazioni affini (lineari) bidimensionali (2D) e vengono descritti i tipi di trasformazioni supportati da DirectComposition.

DirectComposition supporta anche le trasformazioni della prospettiva 3D, ma poiché richiedono la creazione di una bitmap intermedia, DirectComposition considera gli effetti anziché le trasformazioni. Per informazioni sugli effetti della trasformazione prospettiva 3D, vedere [effetti](effects.md).

Questo argomento include le sezioni seguenti:

-   [Che cos'è una trasformazione 2D DirectComposition?](#what-is-a-directcomposition-2d-transform)
-   [Spazio delle coordinate 2D DirectComposition](#the-directcomposition-2d-coordinate-space)
-   [Supporto per le trasformazioni 2D affini](#support-for-affine-2d-transforms)
-   [Trasformazioni 2D matrice](#matrix-2d-transforms)
-   [Gruppi di trasformazione](#transform-groups)
-   [Trasforma animazione](#transform-animation)
-   [Argomenti correlati](#related-topics)

## <a name="what-is-a-directcomposition-2d-transform"></a>Che cos'è una trasformazione 2D DirectComposition?

Una trasformazione 2D consente di modificare la posizione, le dimensioni o la natura di un oggetto visivo in due dimensioni spostando l'oggetto visivo in un altro percorso (conversione), rendendolo più grande o più piccolo (ridimensionamento), trasformandolo (rotazione) o distorsione della forma (inclinazione).

Una trasformazione 2D viene eseguita eseguendo il mapping dei punti di un oggetto visivo da una posizione a un'altra nello stesso spazio delle coordinate o da uno spazio delle coordinate a un altro. Questo mapping è descritto da una tabella di valori denominata matrice di trasformazione, definita come una raccolta di tre righe con tre colonne di valori a virgola mobile, come illustrato nella tabella seguente.



|                 |                 |     |
|-----------------|-----------------|-----|
| M11Default: 1,0 | M12Default: 0,0 | 0,0 |
| M21Default: 0,0 | M22Default: 1,0 | 0,0 |
| M31OffsetX: 0,0 | M32OffsetY: 0,0 | 1.0 |



 

La matrice di trasformazione per le trasformazioni 2D affini è una matrice 3 per 2 che omette la terza colonna dalla matrice di trasformazione precedente. Nella tabella seguente viene illustrato il layout di questa matrice.



|                 |                 |
|-----------------|-----------------|
| M11Default: 1,0 | M12Default: 0,0 |
| M21Default: 0,0 | M22Default: 1,0 |
| M31OffsetX: 0,0 | M32OffsetY: 0,0 |



 

> [!Note]  
> DirectComposition non esegue alcuna elaborazione speciale quando si applicano trasformazioni 2D al contenuto stereo. Ciò significa che il contenuto 3D potrebbe sembrare distorto quando viene applicata una trasformazione 2D.

 

## <a name="the-directcomposition-2d-coordinate-space"></a>Spazio delle coordinate 2D DirectComposition

DirectComposition utilizza uno spazio delle coordinate 2D a sinistra; ovvero, i valori positivi dell'asse x aumentano a destra e i valori positivi dell'asse y aumentano verso il basso. Gli oggetti visivi sono posizionati in relazione all'origine, ovvero il punto in cui l'asse x e l'asse y si intersecano (0,0), come illustrato nella figura seguente.

![asse x e asse y di uno spazio delle coordinate a sinistra](images/coordinatespace.png)

Modificando i valori in una matrice di trasformazione 3 per 2, è possibile ruotare, ridimensionare, inclinare e tradurre un oggetto in due dimensioni. Se, ad esempio, si imposta OffsetX su 100 e OffsetY su 200, si sposta l'oggetto a destra 100 pixel e giù 200 pixel.

## <a name="support-for-affine-2d-transforms"></a>Supporto per le trasformazioni 2D affini

La tabella seguente descrive i tipi di trasformazioni 2D affini supportate da DirectComposition ed elenca le interfacce che è possibile usare per eseguire i vari tipi di trasformazioni.



| Trasformazione/interfaccia                                                                               | Descrizione                                                                                              | Illustrazione                                                                                                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Ruotare la[](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform) \[ nuova riga idcompositionrotatetransform 2D\]          | ruotare un oggetto visivo in base all'angolo specificato intorno al punto centrale specificato.                                 | ![illustrazione di un quadrato ruotato di 45 gradi in senso orario rispetto al centro del quadrato originale](images/rotate.png)               |
| Ridimensiona la[](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform) \[ nuova riga idcompositionscaletransform 2D\]             | Ridimensiona un oggetto visivo in base al fattore specificato sul punto centrale specificato.                                 | ![illustrazione di un quadrato con scala 130%](images/scale.png)                                                                  |
| Nuova riga [**Idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)2D \[\]                | inclina un oggetto visivo in base all'angolo specificato lungo l'asse x e l'asse y e intorno al punto centrale specificato. | ![illustrazione di un quadrato inclinato di 30 gradi in senso antiorario dall'asse y](images/skew.png)                                   |
| Tradurre la[](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) \[ nuova riga idcompositiontranslatetransform 2D\] | modificare la posizione di un oggetto visivo nella direzione dell'asse x e dell'asse y.                               | ![illustrazione di un quadrato spostato di 20 unità lungo l'asse x positivo e 10 unità lungo l'asse y positivo](images/translate.png) |



 

## <a name="matrix-2d-transforms"></a>Trasformazioni 2D matrice

L'interfaccia [**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) consente di definire una matrice di trasformazione 2D affine con 3 per 2 e applicarla a un oggetto visivo. Questa interfaccia è utile se è necessario applicare un tipo di trasformazione 2D affine che non è disponibile tramite le altre interfacce di trasformazione DirectComposition. Per definire la matrice, compilare una struttura [**D2D \_ Matrix \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) e passarla al metodo [**IDCompositionMatrixTransform:: sematrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) .

## <a name="transform-groups"></a>Gruppi di trasformazione

È possibile utilizzare i gruppi di trasformazione per combinare più trasformazioni in una sola. Un gruppo di trasformazione definisce una raccolta di oggetti Transform le cui matrici vengono moltiplicate insieme nell'ordine in cui sono specificate nella raccolta. La matrice di trasformazione risultante viene quindi applicata all'oggetto visivo. Un gruppo di trasformazione produce lo stesso risultato dell'applicazione di ogni trasformazione separatamente.

Tenere presente che l'ordine degli oggetti Transform in un gruppo di trasformazione è importante. Se, ad esempio, un oggetto visivo viene prima ruotato, quindi ridimensionato e quindi convertito, il risultato è diverso da quello in cui l'oggetto visivo viene prima tradotto, quindi ruotato e quindi ridimensionato. DirectComposition applica sempre le trasformazioni a un oggetto visivo nell'ordine in cui sono specificate nella raccolta.

Per creare un gruppo di trasformazione, creare prima di tutto gli oggetti Transform da includere nel gruppo, quindi passare una matrice di puntatori all'oggetto Transform al metodo [**IDCompositionDevice:: CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) . Dopo aver creato un gruppo di trasformazione, non è possibile aggiungere o rimuovere oggetti Transform. Tuttavia, è possibile modificare le proprietà dei singoli oggetti Transform nella raccolta e le modifiche verranno riflesse nella matrice di trasformazione risultante.

## <a name="transform-animation"></a>Trasforma animazione

Le proprietà di una trasformazione possono essere animate. Quando una proprietà viene animata, DirectComposition modifica il valore della proprietà nel tempo invece che in una sola volta. Questa operazione è particolarmente utile quando si creano transizioni. Per altre informazioni, vedere [Animation](animation.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 
