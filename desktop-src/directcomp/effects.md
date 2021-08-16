---
title: Effetti (DirectComposition)
description: Questo argomento illustra le nozioni di base degli effetti di Microsoft DirectComposition e descrive i tipi di effetti supportati da DirectComposition.
ms.assetid: 805B17D2-2F6B-4C25-8C6D-41FFA5DFC774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c5119367a35725a85efe20b8ba4d0f9f9887ff91b4d9618e2215bedfbfef67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117905052"
---
# <a name="effects-directcomposition"></a>Effetti (DirectComposition)

> [!NOTE]
> Per le app Windows 10, è consigliabile usare le API Windows.UI.Composition anziché DirectComposition. Per altre informazioni, vedi [Modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).

Questo argomento illustra le nozioni di base degli effetti di Microsoft DirectComposition e descrive i tipi di effetti supportati da DirectComposition.

In questo argomento sono incluse le sezioni seguenti:

-   [Che cos'è un effetto DirectComposition?](#what-is-a-directcomposition-effect)
-   [Opacità](#opacity)
-   [Effetti di trasformazione della prospettiva 3D](#3d-perspective-transform-effects)
    -   [Spazio delle coordinate 3D DirectComposition](#the-directcomposition-3d-coordinate-space)
    -   [Effetto di trasformazione rotazione 3D](#3d-rotation-transform-effect)
    -   [Effetto di trasformazione ridimensionamento 3D](#3d-scaling-transform-effect)
    -   [Effetto di trasformazione traslazione 3D](#3d-translation-transform-effect)
    -   [Effetto di trasformazione matrice 3D](#3d-matrix-transform-effect)
    -   [Gruppo di effetti di trasformazione 3D](#3d-transform-effect-group)
-   [Oggetti Effetto](#effect-objects)
-   [Argomenti correlati](#related-topics)

## <a name="what-is-a-directcomposition-effect"></a>Che cos'è un effetto DirectComposition?

Un effetto DirectComposition *è* un'operazione bitmap che viene applicata durante la rasterizzazione di un oggetto visivo per modificare in qualche modo l'aspetto dell'oggetto visivo.

DirectComposition crea un effetto prendendo un sottoalbero visivo e ne esegue il rendering in una singola bitmap prima di applicare l'effetto. Ad esempio, per creare un effetto di trasformazione prospettica 3D, DirectComposition produce un'immagine di un sottoal albero visivo e quindi trame dell'immagine in un piano 3D trasformato in base alla matrice risultante dell'effetto di trasformazione 3D.

DirectComposition supporta i tipi di effetti seguenti.



| Tipo di effetto                                                   | Descrizione                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------|
| [Opacità](#opacity)                                           | Imposta l'opacità di un intero oggetto visivo.                                      |
| [Trasformazione della prospettiva 3D](#3d-perspective-transform-effects) | Applica un effetto di trasformazione prospettica tridimensionale (3D) a un oggetto visivo. |



 

> [!Note]  
> DirectComposition non esegue alcuna elaborazione speciale quando si applicano effetti al contenuto stereo 3D. Ciò significa che il contenuto 3D potrebbe apparire distorto quando vi viene applicato un effetto.

 

## <a name="opacity"></a>Opacità

L'effetto di opacità consente di impostare il fattore di opacità applicato a un intero oggetto visivo quando viene eseguito il rendering dell'oggetto visivo. Differisce da una maschera alfa perché lo stesso fattore di opacità viene applicato a tutti i pixel nell'oggetto visivo. L'opacità viene specificata come valore compreso tra 0 (completamente trasparente) e 1 (completamente opaco).

Il fattore di opacità viene applicato dagli oggetti visivi padre a figlio, ma gli effetti visibili delle impostazioni di opacità annidata non sono indicati nel valore della proprietà dei singoli oggetti visivi figlio. Ad esempio, se un oggetto visivo radice ha un'opacità del 50% (0,5) e uno dei relativi elementi figlio ha un'opacità del 20% (0,2), viene eseguito il rendering dell'opacità di rete per tale elemento figlio come 10% (0,1), ma il valore della proprietà Opacity dell'elemento figlio sarà comunque 0,2.

## <a name="3d-perspective-transform-effects"></a>Effetti di trasformazione della prospettiva 3D

Questa sezione descrive lo spazio delle coordinate utilizzato da DirectComposition per l'esecuzione di effetti di trasformazione prospettica 3D. Descrive anche i tipi di effetti di trasformazione prospettica 3D supportati da DirectComposition.

-   [Spazio delle coordinate 3D DirectComposition](#the-directcomposition-3d-coordinate-space)
-   [Effetto di trasformazione rotazione 3D](#3d-rotation-transform-effect)
-   [Effetto di trasformazione ridimensionamento 3D](#3d-scaling-transform-effect)
-   [Effetto di trasformazione traslazione 3D](#3d-translation-transform-effect)
-   [Effetto di trasformazione matrice 3D](#3d-matrix-transform-effect)
-   [Gruppo di effetti di trasformazione 3D](#3d-transform-effect-group)

> [!Note]  
> In DirectComposition l'applicazione di effetti 3D a più livelli nella struttura ad albero visuale non funziona allo stesso modo di un motore 3D completo, ad esempio Microsoft Direct3D. Si consideri ad esempio un oggetto visivo padre con un singolo oggetto visivo figlio. Se l'oggetto visivo figlio viene ruotato in avanti nella direzione z (intorno all'asse y) di 90 gradi, il bordo del bordo dell'oggetto visivo figlio si trova di fronte al visualizzatore e quindi ci si aspetterebbe che l'oggetto visivo non sia visibile (perché una bitmap non ha una profondità reale). Se l'oggetto visivo padre viene quindi ruotato all'indietro nella direzione z negativa (intorno all'asse y) di 90 gradi, è possibile che l'oggetto visivo figlio diventi completamente visibile (poiché le trasformazioni si negano a vicenda). Tuttavia, in DirectComposition questo non è il caso. L'oggetto visivo figlio non sarà visibile perché è stato "appiattito" nella bitmap padre.

 

### <a name="the-directcomposition-3d-coordinate-space"></a>Spazio delle coordinate 3D DirectComposition

Lo spazio delle coordinate DirectComposition per gli effetti di trasformazione 3D individua l'origine (0,0,0) nell'angolo superiore sinistro della superficie bitmap, con i valori positivi dell'asse x che procede verso destra, i valori positivi dell'asse y che procede verso il basso e i valori positivi dell'asse z che procede verso l'esterno dell'origine verso il visualizzatore. Questa illustrazione mostra lo spazio delle coordinate 3D di DirectComposition.

![directcompostion 3d coordinate space](images/3d-coordinate-space.png)

### <a name="3d-rotation-transform-effect"></a>Effetto di trasformazione rotazione 3D

Un effetto di trasformazione rotazione 3D ruota un oggetto visivo in tre dimensioni in base all'angolo specificato intorno a un vettore dell'asse di rotazione x,y,z situato nel punto \[ \] centrale specificato (x,y,z). L'angolo è specificato in gradi. Il vettore dell'asse di rotazione predefinito \[ è 0,0,-1 e il punto centrale predefinito \] è (0,0,0).

Usare il [**metodo IDCompositionDevice::CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d) per creare un oggetto di trasformazione di rotazione 3D. Il metodo recupera [**un'interfaccia IDCompositionRotateTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform3d) che è possibile usare per impostare le proprietà dell'oggetto.

### <a name="3d-scaling-transform-effect"></a>Effetto di trasformazione ridimensionamento 3D

Un effetto di trasformazione di ridimensionamento 3D rende un oggetto visivo più grande o più piccolo. Ridimensiona un oggetto visivo nella direzione \[ x,y,z verso il punto \] centrale (x,y,z). Il punto centrale predefinito è (0,0,0).

Usare il [**metodo IDCompositionDevice::CreateScaleTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform3d) per creare un oggetto di trasformazione di ridimensionamento 3D. Il metodo recupera [**un'interfaccia IDCompositionScaleTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform3d) che è possibile usare per impostare le proprietà dell'oggetto.

### <a name="3d-translation-transform-effect"></a>Effetto di trasformazione traslazione 3D

Un effetto di trasformazione traslazione 3D modifica la posizione di un oggetto visivo nella \[ direzione x,y,z. \]

Usare il [**metodo IDCompositionDevice::CreateTranslateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform3d) per creare un oggetto trasformazione traslazione 3D. Il metodo recupera [**un'interfaccia IDCompositionTranslateTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform3d) che è possibile usare per impostare le proprietà dell'oggetto.

### <a name="3d-matrix-transform-effect"></a>Effetto di trasformazione matrice 3D

[**L'interfaccia IDCompositionMatrixTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) consente di definire una matrice di trasformazione 4 per 4 e applicarla a un oggetto visivo. Questa interfaccia è utile se è necessario applicare un tipo di effetto di trasformazione prospettiva 3D che non è disponibile tramite le altre interfacce di effetto di trasformazione 3D DirectComposition. Per definire la matrice, compilare una struttura [**D3DMATRIX**](/windows/desktop/direct3d10/d3d10-d3dmatrix) e passarla al [**metodo IDCompositionMatrixTransform3D::SetMatrix.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) In alternativa, è possibile impostare ogni elemento della matrice usando il [**metodo IDCompositionMatrixTransform3D::SetMatrixElement.**](/previous-versions/windows/desktop/legacy/hh437429(v=vs.85))

### <a name="3d-transform-effect-group"></a>Gruppo di effetti di trasformazione 3D

[**IDCompositionDevice::CreateTransform3DGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransform3dgroup) crea una raccolta di effetti di trasformazione 3D che è possibile applicare a un oggetto visivo come gruppo. La matrice può includere qualsiasi numero di oggetti transform e può includere trasformazioni di matrice, rotazione, ridimensionamento e traslazione. La raccolta di oggetti di trasformazione 3D comporta una trasformazione il cui valore è la moltiplicazione di matrici delle singole matrici di trasformazione nella raccolta.

L'ordine delle singole trasformazioni nel gruppo è importante. Ad esempio, se prima si ruota, quindi si ridimensiona, quindi si trasla, si ottiene un risultato diverso da quello che si ottiene traslando, quindi ruotando e quindi ridimensionando. DirectComposition rispetta l'ordine in cui si specificano le trasformazioni 3D all'interno di un gruppo 3D di trasformazione allo stesso modo delle trasformazioni 2D. Inoltre, le trasformazioni della prospettiva 3D comportano l'appiattimento della struttura ad albero visuale dopo l'applicazione di tutte le trasformazioni 3D nell'oggetto visivo corrente. Questa operazione viene eseguita per garantire che la scena sia il più vicino possibile al 3D.

## <a name="effect-objects"></a>Oggetti Effetto

Per applicare un effetto a un oggetto visivo, è prima necessario creare e impostare le proprietà di un oggetto effetto che rappresenta il tipo di effetto che si vuole produrre sull'oggetto visivo. È quindi necessario applicare l'oggetto effetto alla proprietà Effect dell'oggetto visivo.

Per creare un oggetto effetto, usare uno dei metodi di interfaccia [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) seguenti per creare un oggetto effetto per il tipo di effetto desiderato. I metodi seguenti creano oggetti effetto:

-   [**CreateMatrixTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-creatematrixtransform3d)
-   [**CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d)
-   [**CreateScaleTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform3d)
-   [**CreateTranslateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform3d)

Ognuno dei metodi precedenti recupera un'interfaccia che è possibile usare per impostare le proprietà dell'oggetto effetto appena creato. Usare i metodi di interfaccia per impostare le proprietà in base alle esigenze per produrre l'effetto visivo desiderato.

La maggior parte delle proprietà di un oggetto effetto può essere animata. Per animare una determinata proprietà, creare un oggetto animazione e applicarlo alla proprietà a cui si vuole aggiungere un'animazione. In caso contrario, impostare la proprietà su un valore statico che produce l'effetto desiderato. Per altre informazioni sull'animazione delle proprietà, vedere [Animazione.](animation.md)

Per applicare un oggetto effetto all'oggetto visivo, chiamare il [**metodo IDCompositionVisual::SetEffect.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) Quando si applica un effetto a un oggetto visivo, l'effetto viene applicato all'intero sottoalbero visivo radice di tale oggetto visivo. Ad esempio, se si imposta l'opacità di un oggetto visivo sul 50%, l'opacità di tutti gli oggetti visivi figlio nel sottoalbero visivo verrà ridotta del 50%. È possibile applicare lo stesso oggetto effetto a uno o più oggetti visivi. Se si modificano le proprietà di un oggetto effetto dopo l'applicazione agli oggetti visivi, tutti gli oggetti visivi vengono ri-composti per riflettere la modifica.

Usando un oggetto gruppo di effetti, è possibile applicare contemporaneamente più effetti a un oggetto visivo. Chiamare prima [**IDCompositionDevice::CreateEffectGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createeffectgroup) per creare l'oggetto gruppo di effetti e quindi aggiungere effetti al gruppo usando [**l'interfaccia IDCompositionEffectGroup**](/windows/win32/api/dcomp/nn-dcomp-idcompositioneffectgroup) dell'oggetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi a DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 