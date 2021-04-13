---
title: Effetti (DirectComposition)
description: Questo argomento illustra le nozioni di base degli effetti Microsoft DirectComposition e descrive i tipi di effetti supportati da DirectComposition.
ms.assetid: 805B17D2-2F6B-4C25-8C6D-41FFA5DFC774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cfd1ca154dcbc7e55ca65cc34d04cfa7d73ccee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399203"
---
# <a name="effects-directcomposition"></a>Effetti (DirectComposition)

> [!NOTE]
> Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition. Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).

Questo argomento illustra le nozioni di base degli effetti Microsoft DirectComposition e descrive i tipi di effetti supportati da DirectComposition.

In questo argomento sono incluse le sezioni seguenti:

-   [Che cos'è un effetto DirectComposition?](#what-is-a-directcomposition-effect)
-   [Opacità](#opacity)
-   [effetti della trasformazione prospettiva 3D](#3d-perspective-transform-effects)
    -   [Spazio delle coordinate DirectComposition 3D](#the-directcomposition-3d-coordinate-space)
    -   [effetto trasformazione rotazione 3D](#3d-rotation-transform-effect)
    -   [effetto trasformazione scala 3D](#3d-scaling-transform-effect)
    -   [effetto trasformazione traduzione 3D](#3d-translation-transform-effect)
    -   [effetto trasformazione matrice 3D](#3d-matrix-transform-effect)
    -   [gruppo effetti trasformazione 3D](#3d-transform-effect-group)
-   [Oggetti Effect](#effect-objects)
-   [Argomenti correlati](#related-topics)

## <a name="what-is-a-directcomposition-effect"></a>Che cos'è un effetto DirectComposition?

Un *effetto* DirectComposition è un'operazione bitmap applicata durante la rasterizzazione di un oggetto visivo per modificare in qualche modo l'aspetto dell'oggetto visivo.

DirectComposition crea un effetto prendendo un sottoalbero visuale ed eseguendone il rendering in un'unica bitmap prima di applicare l'effetto. Ad esempio, per creare un effetto di trasformazione prospettiva 3D, DirectComposition produce un'immagine di un sottoalbero visivo e quindi trama l'immagine su un piano 3D trasformato in base alla matrice risultante dell'effetto di trasformazione 3D.

DirectComposition supporta i seguenti tipi di effetti.



| Tipo di effetto                                                   | Descrizione                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------|
| [Opacità](#opacity)                                           | Imposta l'opacità di un intero oggetto visivo.                                      |
| [trasformazione prospettiva 3D](#3d-perspective-transform-effects) | Applica un effetto di trasformazione prospettiva tridimensionale (3D) a un oggetto visivo. |



 

> [!Note]  
> DirectComposition non esegue alcuna elaborazione speciale quando applica effetti al contenuto stereo 3D. Ciò significa che il contenuto 3D potrebbe sembrare distorto quando viene applicato un effetto.

 

## <a name="opacity"></a>Opacità

L'effetto di opacità consente di impostare il fattore di opacità applicato a un intero oggetto visivo quando viene eseguito il rendering dell'oggetto visivo. Si differenzia da una maschera alfa in quanto lo stesso fattore di opacità viene applicato a tutti i pixel nell'oggetto visivo. L'opacità viene specificata come valore compreso tra 0 (completamente trasparente) e 1 (completamente opaco).

Il fattore di opacità viene applicato dagli oggetti visivi padre agli elementi figlio, ma gli effetti visibili delle impostazioni di opacità nidificata non sono indicati nel valore della proprietà dei singoli oggetti visivi figlio. Ad esempio, se un oggetto visivo radice ha un'opacità 50% (0,5) e uno degli elementi figlio ha un'opacità del 20% (0,2), l'opacità netta per tale elemento figlio viene sottoposta a rendering come 10% (0,1), ma il valore della proprietà di opacità del figlio sarà ancora 0,2.

## <a name="3d-perspective-transform-effects"></a>effetti della trasformazione prospettiva 3D

Questa sezione descrive lo spazio delle coordinate usato da DirectComposition per l'esecuzione di effetti della trasformazione prospettiva 3D. Vengono inoltre descritti i tipi di effetti della trasformazione prospettiva 3D supportati da DirectComposition.

-   [Spazio delle coordinate DirectComposition 3D](#the-directcomposition-3d-coordinate-space)
-   [effetto trasformazione rotazione 3D](#3d-rotation-transform-effect)
-   [effetto trasformazione scala 3D](#3d-scaling-transform-effect)
-   [effetto trasformazione traduzione 3D](#3d-translation-transform-effect)
-   [effetto trasformazione matrice 3D](#3d-matrix-transform-effect)
-   [gruppo effetti trasformazione 3D](#3d-transform-effect-group)

> [!Note]  
> In DirectComposition l'applicazione di effetti 3D a più livelli nella struttura ad albero visuale non funziona nello stesso modo in cui avviene con un motore 3D completo, ad esempio Microsoft Direct3D. Si consideri, ad esempio, un oggetto visivo padre con un singolo oggetto visivo figlio. Se l'oggetto visivo figlio viene ruotato in avanti nella direzione z (intorno all'asse y) di 90 gradi, il bordo del bordo visivo figlio verrà visualizzato nel Visualizzatore, quindi ci si aspetterebbe che l'oggetto visivo non sia visibile (perché una bitmap non ha profondità reale). Se l'oggetto visivo padre viene quindi ruotato all'indietro nella direzione della z negativa (intorno all'asse y) di 90 gradi, è possibile che l'oggetto visivo figlio diventi completamente visibile (poiché le trasformazioni si negano a vicenda). Tuttavia, in DirectComposition questo non è il caso. L'oggetto visivo figlio non sarà visibile perché è stato "flat" nella bitmap padre.

 

### <a name="the-directcomposition-3d-coordinate-space"></a>Spazio delle coordinate DirectComposition 3D

Lo spazio delle coordinate DirectComposition per gli effetti di trasformazione 3D individua l'origine (0, 0, 0) nell'angolo superiore sinistro della superficie bitmap, con i valori positivi dell'asse x che procedono verso destra, i valori positivi dell'asse y che procedono verso il basso e i valori positivi dell'asse z che procedono verso l'esterno dall'origine verso il visualizzatore. Questa illustrazione mostra lo spazio delle coordinate 3D di DirectComposition.

![spazio delle coordinate 3D directcompostion](images/3d-coordinate-space.png)

### <a name="3d-rotation-transform-effect"></a>effetto trasformazione rotazione 3D

Un effetto di trasformazione rotazione 3D ruota un oggetto visivo in tre dimensioni in base all'angolo specificato rispetto a un vettore asse di rotazione \[ x, y, z \] situato al punto centrale specificato (x, y, z). L'angolo è specificato in gradi. Il vettore dell'asse di rotazione predefinito è \[ 0, 0,-1 \] e il punto centrale predefinito è (0, 0, 0).

Usare il metodo [**IDCompositionDevice:: CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d) per creare un oggetto Transform di rotazione 3D. Il metodo recupera un'interfaccia [**IDCompositionRotateTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform3d) che è possibile usare per impostare le proprietà dell'oggetto.

### <a name="3d-scaling-transform-effect"></a>effetto trasformazione scala 3D

Un effetto di trasformazione di scala 3D rende un oggetto visivo più grande o più piccolo. Ridimensiona un oggetto visivo nella \[ direzione x, y, z del \] punto centrale (x, y, z). Il punto centrale predefinito è (0, 0, 0).

Usare il metodo [**IDCompositionDevice:: CreateScaleTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform3d) per creare un oggetto Transform di ridimensionamento 3D. Il metodo recupera un'interfaccia [**IDCompositionScaleTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform3d) che è possibile usare per impostare le proprietà dell'oggetto.

### <a name="3d-translation-transform-effect"></a>effetto trasformazione traduzione 3D

Un effetto di trasformazione della traduzione 3D modifica la posizione di un oggetto visivo nella \[ direzione x, y, z \] .

Usare il metodo [**IDCompositionDevice:: CreateTranslateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform3d) per creare un oggetto Transform di conversione 3D. Il metodo recupera un'interfaccia [**IDCompositionTranslateTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform3d) che è possibile usare per impostare le proprietà dell'oggetto.

### <a name="3d-matrix-transform-effect"></a>effetto trasformazione matrice 3D

L'interfaccia [**IDCompositionMatrixTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) consente di definire una matrice di trasformazione 4 per 4 e di applicarla a un oggetto visivo. Questa interfaccia è utile se è necessario applicare un tipo di effetto di trasformazione prospettiva 3D che non è disponibile tramite le altre interfacce di effetto trasformazione 3D di DirectComposition. Per definire la matrice, compilare una struttura [**D3DMATRIX**](/windows/desktop/direct3d10/d3d10-d3dmatrix) e passarla al metodo [**IDCompositionMatrixTransform3D:: sematrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) . In alternativa, è possibile impostare ogni elemento della matrice usando il metodo [**IDCompositionMatrixTransform3D:: Sematrixelement**](/previous-versions/windows/desktop/legacy/hh437429(v=vs.85)) .

### <a name="3d-transform-effect-group"></a>gruppo effetti trasformazione 3D

[**IDCompositionDevice:: CreateTransform3DGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransform3dgroup) crea una raccolta di effetti della trasformazione 3D che è possibile applicare a un oggetto visivo come gruppo. La matrice può includere qualsiasi numero di oggetti Transform e può includere trasformazioni di matrice, rotazione, scalabilità e conversione. La raccolta di oggetti trasformazione 3D genera una trasformazione il cui valore è la moltiplicazione di matrici delle singole matrici di trasformazione nella raccolta.

L'ordine delle singole trasformazioni nel gruppo è importante. Se, ad esempio, si esegue prima la rotazione, quindi si esegue la scalabilità e si traduce, si ottiene un risultato diverso da quello in cui si esegue la prima conversione, quindi si ruota e quindi si ridimensiona. DirectComposition rispetta l'ordine in cui si specificano le trasformazioni 3D in un gruppo trasforma 3D nello stesso modo in cui avviene per le trasformazioni 2D. Inoltre, le trasformazioni della prospettiva 3D generano una bidimensionale della struttura ad albero visuale dopo l'applicazione di tutte le trasformazioni 3D nell'oggetto visivo corrente. Questa operazione viene eseguita per assicurarsi che la scena risulti più vicina al più possibile il 3D.

## <a name="effect-objects"></a>Oggetti Effect

Per applicare un effetto a un oggetto visivo, è necessario innanzitutto creare e impostare le proprietà di un oggetto Effect che rappresenta il tipo di effetto che si desidera produrre nell'oggetto visivo. Quindi, è necessario applicare l'oggetto Effect alla proprietà Effect dell'oggetto visivo.

Per creare un oggetto Effect, usare uno dei seguenti metodi di interfaccia [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) per creare un oggetto Effect per il tipo di effetto desiderato. I metodi seguenti creano oggetti Effect:

-   [**CreateMatrixTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-creatematrixtransform3d)
-   [**CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d)
-   [**CreateScaleTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform3d)
-   [**CreateTranslateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform3d)

Ognuno dei metodi precedenti recupera un'interfaccia che è possibile usare per impostare le proprietà dell'oggetto effetto appena creato. Usare i metodi di interfaccia per impostare le proprietà necessarie per produrre l'effetto visivo desiderato.

La maggior parte delle proprietà di un oggetto Effect può essere animata. Per animare una particolare proprietà, creare un oggetto animazione e applicarlo alla proprietà che si desidera animare; in caso contrario, impostare la proprietà su un valore statico che produce l'effetto desiderato. Per ulteriori informazioni sull'animazione delle proprietà, vedere [Animation](animation.md).

Per applicare un oggetto Effect a Visual, chiamare il metodo [**IDCompositionVisual:: seeffect**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) . Quando si applica un effetto a un oggetto visivo, l'effetto viene applicato all'intero sottoalbero visuale radice in corrispondenza dell'oggetto visivo. Se, ad esempio, si imposta l'opacità di un oggetto visivo su 50 percent, l'opacità di tutti gli oggetti visivi figlio nel sottoalbero visuale verrà ridotta del 50%. È possibile applicare lo stesso oggetto Effect a uno o più oggetti visivi. Se si modificano le proprietà di un oggetto effetto dopo averlo applicato agli oggetti visivi, tutti gli oggetti visivi vengono ricomposti per riflettere la modifica.

Utilizzando un oggetto gruppo di effetti, è possibile applicare contemporaneamente più effetti a un oggetto visivo. Chiamare prima [**IDCompositionDevice:: CreateEffectGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createeffectgroup) per creare l'oggetto gruppo di effetti, quindi aggiungere effetti al gruppo usando l'interfaccia [**IDCompositionEffectGroup**](/windows/win32/api/dcomp/nn-dcomp-idcompositioneffectgroup) dell'oggetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 