---
title: Posizionamento di forme
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- Web Workshop, posizionamento delle forme
- progettazione di pagine Web, posizionamento di forme
- Vector Markup Language (la), posizionamento delle forme
- LA (Vector Markup Language), posizionamento delle forme
- grafica vettoriale, forme posizionamento
- Forme la, posizionamento
- posizionamento di forme
- Vector Markup Language (la), stile posizione statica
- LA (Vector Markup Language), stile posizione statica
- grafica vettoriale, stile posizione statica
- stile posizione statica
- Vector Markup Language (la), stile posizione relativa
- LA (Vector Markup Language), stile di posizione relativo
- grafica vettoriale, stile posizione relativa
- stile posizione relativa
- Vector Markup Language (la), stile di posizione assoluto
- LA (Vector Markup Language), stile di posizione assoluto
- grafica vettoriale, stile posizione assoluta
- stile posizione assoluta
- Vector Markup Language (la), stile posizione indice z
- LA (Vector Markup Language), stile posizione indice z
- grafica vettoriale, stile posizione indice z
- stile posizione indice z
- Vector Markup Language (la), stile posizione rotazione
- LA (Vector Markup Language), stile posizione rotazione
- grafica vettoriale, stile posizione rotazione
- stile posizione rotazione
- Vector Markup Language (la), Capovolgi stile posizione
- LA (Vector Markup Language), Capovolgi stile posizione
- grafica vettoriale, stile flip position
- Inverti stile posizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8e01d0c7962467b1894f0f4c2c6cd1f6b01509
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046901"
---
# <a name="positioning-shapes"></a>Posizionamento di forme

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Si è appreso come creare e colorare forme in una pagina Web usando la. In questo argomento verrà usato la per posizionare con precisione la grafica in una pagina Web.

LA utilizza la stessa sintassi definita nelle sezioni [modello di riquadro](https://www.w3.org/TR/PR-CSS2/box.mdl) e [modello di rendering visivo](https://www.w3.org/TR/PR-CSS2/visuren.mdl) di [CSS2](https://www.w3.org/TR/PR-CSS2/) per posizionare le forme in una pagina Web. È possibile usare [static](#static), [relativa](#relative)o [Absolute](#absolute) per determinare la posizione in cui si trova il punto di base in una pagina Web. È quindi possibile usare gli attributi di stile **superiore** e **sinistro** per specificare l'offset dal punto di base in cui verrà posizionata la casella contenitore per la forma.

È inoltre possibile utilizzare [z-index](#z-index) per specificare l'ordine z delle forme in una pagina Web.

Inoltre, la fornisce [rotazione](#rotation) e [Capovolgi](#flip) per ruotare o capovolgere le forme.

In questo argomento

-   [static](#static)
-   [relative](#relative)
-   [absolute](#absolute)
-   [indice z](#z-index)
-   [rotazione](#rotation)
-   [flip](#flip)
-   [Summary](#summary)

## <a name="static"></a>static

Lo stile di posizione predefinito è statico, che indica ai browser di posizionare la forma in corrispondenza del punto corrente, ovvero il punto di base, nel flusso di testo e ignorare le impostazioni negli attributi di stile **superiore** e **sinistro** .

Nella rappresentazione la seguente, ad esempio, il rosso ovale viene posizionato immediatamente dopo il testo "inizio della forma:", come illustrato nell'immagine seguente:

![\-ps.gif Shape1 (2123 byte)](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="relative"></a>relative

L'impostazione dell'attributo di stile position su "relativa" consente di posizionare la casella contenitore con un offset dal punto corrente (il punto di base) nel flusso di testo. L'offset è determinato dalle impostazioni negli attributi di stile **superiore** e **sinistro** . Tenere presente che la casella contenitore che è posizionata come relativa occupa spazio nel flusso di testo.

Nella rappresentazione la seguente, ad esempio, il rosso ovale è posizionato a 20 punti da sinistra e 10 punti dalla parte superiore rispetto al punto corrente nel flusso di testo, come illustrato nell'immagine seguente:

![shape3.gif (2048 byte)](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="absolute"></a>assoluto

Impostando l'attributo di stile position su "Absolute" è possibile posizionare la casella contenente una distanza esatta dall'angolo superiore sinistro (il punto di base) del relativo elemento padre, ovvero l'elemento posizionato che contiene la forma. Tenere presente che la casella contenitore che è posizionata come assoluta non occupi spazio nel flusso di testo.

Nella rappresentazione la seguente, ad esempio, il rosso ovale è contenuto all'interno dell' `<body>` elemento (l'intera pagina Web); Pertanto, il punto di base si trova nell'angolo superiore sinistro della pagina Web. La casella contenitore per l'ovale è posizionata esattamente a 20 punti da sinistra e 10 punti dalla parte superiore rispetto all'angolo superiore sinistro della pagina Web, come illustrato nell'immagine seguente:

![shape2.gif (2006 byte)](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="z-index"></a>indice z

È possibile posizionare una forma che si sovrappone a un'altra forma. In genere, il grafico elencato per ultimo nel codice HTML viene visualizzato nella parte superiore.

In la è possibile controllare l'ordine z usando l'attributo di stile **z-index** . Il valore di questo attributo può essere zero, un numero intero positivo o un numero intero negativo. Il grafico con un valore di indice z più grande viene visualizzato sopra l'elemento grafico con un valore di indice z inferiore. Quando entrambi i grafici hanno lo stesso valore di indice z, il grafico elencato per ultimo nel codice HTML viene visualizzato nella parte superiore.

Nella rappresentazione la seguente, ad esempio, il rosso ovale viene visualizzato sopra il rettangolo blu. Questo è dovuto al fatto che il valore dell'indice z dell'ovale rosso è maggiore del valore dell'indice z del rettangolo blu.

![shape4.gif (572 byte)](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





Se si modifica l'indice z, come illustrato nella seguente rappresentazione la, il rosso ovale si sposta dietro il rettangolo blu.

![shape5.gif (469 byte)](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





Se si specifica un numero intero negativo, è possibile usare z-index per posizionare la grafica dietro il normale flusso di testo, come illustrato nella rappresentazione la seguente.

![shape6.gif (2125 byte)](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="rotation"></a>rotazione

È possibile utilizzare l'attributo di stile **Rotation** per specificare il numero di gradi per cui si desidera che una forma accenda l'asse. Un valore positivo indica una rotazione in senso orario; un valore negativo indica una rotazione in senso antiorario.

Ad esempio, se si specifica **Style**='... Rotation: 90', è possibile ruotare la forma 90 gradi in senso orario.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="flip"></a>flip

È possibile utilizzare l'attributo **Flip** Style per capovolgere una forma sull'asse x o y in base alla tabella seguente:



| Valore | Descrizione                                                  |
|-------|--------------------------------------------------------------|
| x     | Capovolgere la forma ruotata sull'asse y (Inverti le coordinate x) |
| y     | Capovolgere la forma ruotata sull'asse x (coordinate y invertite) |



 

Nella proprietà Flip è possibile specificare sia x che y.

Ad esempio, se si digita **Style**='... Flip: x y. la forma viene invertita sia sull'asse x che su quello y.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="summary"></a>Riepilogo

In base a quanto appreso, è possibile posizionare con precisione una forma in una pagina Web attenendosi alla seguente procedura:

1.  Decidere dove si desidera che la forma venga visualizzata in una pagina Web e la dimensione della forma.
2.  Specificare **Style**=' position: relativa (o relativa)' per determinare il punto di base.
3.  Utilizzare **Left** e **Top** per specificare l'offset dal punto di base.
4.  Usare **Width** e **Height** per specificare la dimensione della casella contenitore per la forma.
5.  Utilizzare **z-index** per specificare l'ordine z della forma.

 

 