---
title: Superficie di composizione
description: Questo argomento descrive i tipi di superfici supportate da Microsoft DirectComposition.
ms.assetid: E19B4F0E-1CFA-4E93-BB6A-BFB701BC72CA
keywords:
- superficie di composizione
- Superficie logica DirectComposition
- Superficie virtuale DirectComposition
- aggiornamento di una superficie logica
- superficie logica, aggiornamento
- taglio di una superficie virtuale
- superficie virtuale, taglio
- Taglia superficie virtuale
- ridimensionamento di una superficie virtuale
- Surace virtuale, ridimensionamento
- Ridimensiona superficie virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4bd30bfbd1de91444b7076184db597cd7a8c82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046921"
---
# <a name="composition-surface"></a>Superficie di composizione

> [!NOTE]
> Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition. Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).

Questo argomento descrive i tipi di superfici supportate da Microsoft DirectComposition.

-   [Superficie logica DirectComposition](#directcomposition-logical-surface)
    -   [Aggiornamento di una superficie logica](#updating-a-logical-surface)
    -   [Sospensione degli aggiornamenti in una superficie logica](#suspending-updates-to-a-logical-surface)
    -   [Ripresa degli aggiornamenti in una superficie logica](#resuming-updates-to-a-logical-surface)
    -   [Fine degli aggiornamenti a una superficie logica](#suspending-updates-to-a-logical-surface)
    -   [Esempio di utilizzo di una superficie logica](#example-of-using-a-logical-surface)
-   [Superficie virtuale DirectComposition](#directcomposition-virtual-surface)
    -   [Ridimensionamento di una superficie virtuale](#resizing-a-virtual-surface)
    -   [Taglio di una superficie virtuale](#trimming-a-virtual-surface)
-   [Argomenti correlati](#related-topics)

## <a name="directcomposition-logical-surface"></a>Superficie logica DirectComposition

DirectComposition espone l'oggetto [**IDCompositionSurface**](/windows/win32/api/dcomp/nn-dcomp-idcompositionsurface) per rappresentare una superficie di composizione logica. DirectComposition espone le API che è possibile usare per creare, aggiornare ed eliminare queste superfici logiche. Ogni superficie può essere associata a uno o più oggetti visivi. Un'applicazione è responsabile della gestione della durata delle superfici logiche.

### <a name="updating-a-logical-surface"></a>Aggiornamento di una superficie logica

Un'applicazione può aggiornare una superficie logica chiamando [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) e specificando la dimensione e l'offset del rettangolo sulla superficie logica che l'app vuole aggiornare. DirectComposition alloca un rettangolo con le dimensioni specificate, quindi restituisce la superficie e l'offset corrispondente che l'applicazione deve creare o aggiornare. I limiti del rettangolo di aggiornamento sono associati alle dimensioni della superficie. Il rettangolo di aggiornamento per una superficie di pixel 40 per 100, ad esempio, può essere fino a (0, 0, 40100). Inoltre, l'area aggiornabile viene applicata da un rettangolo Guard. Poiché può essere presente un solo rettangolo Guard alla volta, è possibile aggiornare una sola superficie logica alla volta. **BeginDraw** restituisce un codice di errore se [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) o [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) non è stato chiamato dopo una chiamata precedente a **BeginDraw**. Un'applicazione può aggiungere una chiamata di cui è stato eseguito il commit a **BeginDraw** a un batch, ma non diventa effettiva fino a quando non viene chiamato e sottoposta a commit **EndDraw** .

### <a name="suspending-updates-to-a-logical-surface"></a>Sospensione degli aggiornamenti in una superficie logica

Un'applicazione che deve aggiornare diverse superfici può chiamare [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) sull'aggiornamento corrente e quindi chiamare [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) per avviare un nuovo aggiornamento. Microsoft DirectComposition consente più aggiornamenti, ma solo uno può essere attivo alla volta. Ciò significa che è necessario chiamare **SuspendDraw** o [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) su una superficie prima di chiamare **BeginDraw** su quello successivo. A differenza di **EndDraw**, un batch di cui è stato eseguito il commit può contenere una superficie che si trova in uno stato **SuspendDraw** , ma tali aggiornamenti non vengono visualizzati sullo schermo finché non viene chiamato **EndDraw** .

### <a name="resuming-updates-to-a-logical-surface"></a>Ripresa degli aggiornamenti in una superficie logica

Un'applicazione può riprendere un aggiornamento a una superficie che si trova in uno stato [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) chiamando [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw). Questo metodo può essere chiamato solo su una superficie sospesa.

### <a name="ending-updates-to-a-logical-surface"></a>Fine degli aggiornamenti a una superficie logica

La chiamata a [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) e [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) è l'unico modo per visualizzare le modifiche dell'aggiornamento bitmap sullo schermo. Ogni chiamata a **EndDraw** deve avere una chiamata corrispondente a [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) per rimuovere il rettangolo Guard. La superficie logica mantiene tutti gli aggiornamenti fino a quando non viene chiamato il **commit** . È inoltre possibile chiamare **EndDraw** su una superficie che si trova nello stato [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) perché **EndDraw** è un resume/end implicito. Dopo aver chiamato **EndDraw**, il contenuto aggiornato viene presentato allo schermo e rimosso in modo che la memoria per l'aggiornamento possa essere riutilizzata per un aggiornamento successivo.

### <a name="example-of-using-a-logical-surface"></a>Esempio di utilizzo di una superficie logica

Nell'esempio seguente vengono descritti i passaggi necessari per un'applicazione se è stata creata una struttura ad albero visuale costituita da due oggetti visivi e quindi è necessario aggiornare aree specifiche delle due superfici logiche associate agli oggetti visivi:

1.  Creare un dispositivo DirectComposition.
2.  Creare la struttura ad albero visuale costituita da un nodo radice e dagli oggetti visivi 1 e 2.
3.  Creare le superfici logiche 1 e 2.
4.  Chiamare il [**contenuto**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) per associare una superficie logica agli oggetti visivi 1 e 2.
5.  Chiamare [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) su un rettangolo secondario della superficie logica 1.
6.  Aggiornare la superficie in corrispondenza dell'offset restituito da DirectComposition.
7.  Passaggi facoltativi:
    1.  Chiamare [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) sulla superficie logica 1.
    2.  Chiamare [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) su Sub-Rect della superficie logica 2.
    3.  Aggiornare la superficie in corrispondenza dell'offset restituito da DirectComposition.
    4.  Chiamare [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) sulla superficie logica 2.
    5.  Chiamare [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) sulla superficie logica 1.
8.  Aggiornare la superficie in corrispondenza dell'offset restituito da DirectComposition.
9.  Chiamare [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) sulla superficie logica 1.
10. Chiamare [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit).

## <a name="directcomposition-virtual-surface"></a>Superficie virtuale DirectComposition

DirectComposition espone l'interfaccia [**IDCompositionVirtualSurface**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvirtualsurface) per rappresentare una superficie virtuale, ovvero una raccolta di superfici logiche (riquadri) disposti in una griglia fissa con riquadri di dimensioni fisse. L'applicazione specifica la dimensione della trama virtuale al momento della creazione. La dimensione stabilisce i limiti per la superficie virtuale. La superficie può essere associata a uno o più oggetti visivi.

Quando una superficie virtuale viene inizializzata, non è supportata dalle allocazioni effettive. In altre parole, non tiene alcun bit. DirectComposition alloca i riquadri, ovvero gli oggetti superficie di composizione, dopo che l'applicazione inizia ad aggiornare la superficie. L'applicazione aggiorna la superficie virtuale chiamando [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) e specificando l'area di interesse rispetto alle coordinate della superficie virtuale. Quindi, DirectComposition alloca i riquadri necessari per conservare l'aggiornamento e restituisce la superficie di composizione e l'offset da aggiornare.

Come per le superfici logiche, è possibile chiamare [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) e [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) su una superficie virtuale. DirectComposition espone inoltre i metodi che è possibile usare per ridimensionare e tagliare una superficie virtuale esistente.

### <a name="resizing-a-virtual-surface"></a>Ridimensionamento di una superficie virtuale

Il metodo [**Resize**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-resize) modifica i limiti della superficie virtuale, ovvero tutti i nuovi aggiornamenti o allocazioni devono rientrare nei limiti impostati dalle nuove dimensioni. Un'applicazione usa **Resize** per indicare a DirectComposition che una determinata area della superficie virtuale non è più necessaria e può essere recuperata. Se **Resize** compatta la superficie virtuale, l'applicazione non potrà più aggiornare le aree esterne ai nuovi limiti.

Nell'illustrazione seguente viene mostrata una superficie virtuale 3 per 3 ridimensionata a 2 per 2. L'area rossa rappresenta i riquadri eliminati come parte dell'operazione di ridimensionamento e la memoria viene recuperata da DirectComposition. Dopo il ridimensionamento, l'applicazione non può apportare aggiornamenti all'area rossa senza ridimensionare nuovamente la superficie virtuale.

![ridimensionamento di una superficie virtuale ](images/resize-virtual-surface.png)

L'operazione di ridimensionamento ha effetto immediato. DirectComposition non attende che l'applicazione chiami [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) per apportare aggiornamenti di ridimensionamento. Si supponga, ad esempio, che un'applicazione effettua la seguente sequenza di chiamate.


```
pVirtualSurface->Resize(0, 0);
pVirtualSurface->Resize(INT_MAX, INT_MAX);
pDevice->Commit();
```



In questo esempio, l'applicazione perde tutto il contenuto al primo ridimensionamento. Il secondo ridimensionamento non ha alcun effetto anche se è stato chiamato prima del [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit). In questo caso non viene visualizzato nulla sullo schermo.

### <a name="trimming-a-virtual-surface"></a>Taglio di una superficie virtuale

Il metodo [**Trim**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim) identifica l'area della superficie virtuale necessaria per l'applicazione. Non ridimensiona i limiti della superficie virtuale, ma indica a DirectComposition quali superfici logiche è attualmente necessario allocare.

Nella figura seguente il quadrato verde è il viewport dell'applicazione. L'applicazione esegue inizialmente il rendering dei primi sei riquadri (blu) della superficie virtuale (grigio chiaro) presenti nel viewport. Quando la pagina rappresentata dalla superficie virtuale scorre, l'applicazione deve eseguire il rendering degli ultimi sei riquadri. L'applicazione chiama [**Trim**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim) per indicare che l'area definita dagli ultimi sei riquadri è la posizione in cui si trova il contenuto e il resto non è necessario al momento. DirectComposition può quindi scegliere di riciclare le superfici logiche che originariamente rappresentavano i primi sei riquadri (grigio scuro).

![taglio di una superficie virtuale](images/trim-virtual-surface.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 