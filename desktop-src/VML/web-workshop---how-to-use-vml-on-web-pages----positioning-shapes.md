---
title: Posizionamento di forme
description: Questo articolo descrive il posizionamento delle forme in VML, una funzionalità deprecata a Internet Explorer 9.
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- Web workshop, posizionamento di forme
- progettazione di pagine Web, posizionamento di forme
- Vector Markup Language (VML), posizionamento di forme
- VML (Vector Markup Language),posizionamento di forme
- grafica vettoriale, posizionamento di forme
- forme VML, posizionamento
- posizionamento di forme
- Vector Markup Language (VML), stile di posizione statica
- VML (Vector Markup Language),stile di posizione statica
- grafica vettoriale, stile di posizione statica
- stile di posizione statica
- Vector Markup Language (VML), stile di posizione relativa
- VML (Vector Markup Language),stile di posizione relativa
- grafica vettoriale, stile di posizione relativa
- stile di posizione relativa
- Vector Markup Language (VML), stile di posizione assoluta
- VML (Vector Markup Language),absolute position style
- grafica vettoriale, stile di posizione assoluta
- stile di posizione assoluta
- Vector Markup Language (VML),z-index position style
- VML (Vector Markup Language),z-index position style
- grafica vettoriale, stile di posizione z-index
- Stile di posizione z-index
- Vector Markup Language (VML), stile della posizione di rotazione
- VML (Vector Markup Language),stile della posizione di rotazione
- grafica vettoriale, stile di posizione di rotazione
- stile della posizione di rotazione
- Vector Markup Language (VML), stile di capovolgimento della posizione
- VML (Vector Markup Language),flip position style
- grafica vettoriale, stile posizione capovolgimento
- stile di posizione capovolgimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c96a8de891ed1bbd1b9bfee9eff52ede946247b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407714"
---
# <a name="positioning-shapes"></a>Posizionamento di forme

Questo argomento descrive VML, una funzionalità deprecata a Internet Explorer Windows 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Si è appreso come disegnare e colorare forme in una pagina Web usando VML. In questo argomento si userà VML per posizionare con precisione la grafica in una pagina Web.

VML usa la stessa sintassi definita nelle sezioni Box Model (Modello [box)](https://www.w3.org/TR/PR-CSS2/box.mdl) e [Visual Rendering Model](https://www.w3.org/TR/PR-CSS2/visuren.mdl) (Modello di rendering visivo) di [CSS2](https://www.w3.org/TR/PR-CSS2/) per posizionare le forme in una pagina Web. È possibile usare [static](#static), [relative](#relative)o [absolute](#absolute) per determinare dove si trova il punto di base in una pagina Web. È quindi possibile usare  gli **attributi** di stile superiore e sinistro per specificare l'offset dal punto di base in cui verrà posizionata la casella contenitore per la forma.

È anche possibile usare [z-index](#z-index) per specificare l'ordine z delle forme in una pagina Web.

VmL offre inoltre la [rotazione](#rotation) e il [capovolgimento](#flip) per ruotare o capovolgere le forme.

In questo argomento

-   [static](#static)
-   [relative](#relative)
-   [absolute](#absolute)
-   [z-index](#z-index)
-   [Rotazione](#rotation)
-   [flip](#flip)
-   [Summary](#summary)

## <a name="static"></a>static

Lo stile di posizione predefinito è statico, che indica ai browser di posizionare la forma in corrispondenza del  punto  corrente (il punto di base) nel flusso di testo e ignorare le impostazioni negli attributi di stile superiore e sinistro.

Nella rappresentazione VML seguente, ad esempio, l'ovale rosso viene posizionato immediatamente dopo il testo "Beginning of the shape:", come illustrato nell'immagine seguente:

![shape1 \-ps.gif (2123 byte)](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="relative"></a>relative

L'impostazione dell'attributo di stile della posizione su "relative" consente di posizionare la casella contenitore con un offset dal punto corrente (il punto di base) nel flusso di testo. L'offset è determinato dalle impostazioni negli attributi di stile **superiore** **e** sinistro. Tenere presente che la casella contenitore posizionata come relativa occupa spazio nel flusso di testo.

Nella rappresentazione VML seguente, ad esempio, l'ovale rosso viene posizionato 20 punti da sinistra e 10 punti dall'alto rispetto al punto corrente nel flusso di testo, come illustrato nell'immagine seguente:

![shape3.gif (2048 byte)](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="absolute"></a>assoluto

L'impostazione dell'attributo di stile della posizione su "absolute" consente di posizionare la casella contenitore a una distanza esatta dall'angolo superiore sinistro (il punto di base) dell'elemento padre (l'elemento posizionato che contiene la forma). Tenere presente che la casella contenitore posizionata come assoluta non richiede spazio nel flusso di testo.

Nella rappresentazione VML seguente, ad esempio, l'ovale rosso è contenuto all'interno dell'elemento (l'intera pagina Web). Pertanto, il punto di base si trova nell'angolo superiore sinistro della `<body>` pagina Web. La casella contenitore per l'ovale è posizionata esattamente a 20 punti da sinistra e a 10 punti dall'alto, rispetto all'angolo superiore sinistro della pagina Web, come illustrato nell'immagine seguente:

![shape2.gif (2006 byte)](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="z-index"></a>indice z

È possibile posizionare una forma che si sovrappone a un'altra forma. In genere, il grafico elencato per ultimo nel codice HTML viene visualizzato nella parte superiore.

In VML è possibile controllare l'ordine z usando **l'attributo di stile z-index.** Il valore di questo attributo può essere zero, un numero intero positivo o un numero intero negativo. L'elemento grafico con un valore z-index maggiore viene visualizzato sopra l'elemento grafico con un valore z-index più piccolo. Quando entrambi gli elementi grafici hanno lo stesso valore z-index, l'elemento grafico elencato per ultimo nel codice HTML viene visualizzato nella parte superiore.

Nella rappresentazione VML seguente, ad esempio, l'ovale rosso viene visualizzato sopra il rettangolo blu. Questo perché il valore z-index dell'ovale rosso è maggiore del valore z-index del rettangolo blu.

![shape4.gif (572 byte)](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





Se si modifica l'indice z, come illustrato nella rappresentazione VML seguente, l'ovale rosso si sposterà dietro il rettangolo blu.

![shape5.gif (469 byte)](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





Se si specifica un numero intero negativo, è possibile usare z-index per posizionare la grafica dietro il normale flusso di testo, come illustrato nella rappresentazione VML seguente.

![shape6.gif (2125 byte)](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="rotation"></a>Rotazione

È possibile usare **l'attributo di** stile di rotazione per specificare quanti gradi si vuole che una forma accerti il relativo asse. Un valore positivo indica una rotazione in senso orario; un valore negativo indica una rotazione in senso antiorario.

Ad esempio, se si specifica **style**='... rotation:90', è possibile ruotare la forma di 90 gradi in senso orario.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="flip"></a>flip

È possibile usare **l'attributo dello** stile di capovolgimento per capovolgere una forma sul relativo asse x o y in base alla tabella seguente:



| Valore | Descrizione                                                  |
|-------|--------------------------------------------------------------|
| x     | Capovolgere la forma ruotata intorno all'asse y (inverti x ordinate) |
| y     | Capovolgere la forma ruotata intorno all'asse x (inverte ordinate y) |



 

Sia x che y possono essere specificati nella proprietà flip.

Ad esempio, se si digita **style**='... flip:x y', la forma verrà capovolta sia sull'asse x che sull'asse y.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="summary"></a>Riepilogo

In base a quanto appreso, è possibile posizionare con precisione una forma in una pagina Web seguendo questa procedura:

1.  Decidere dove si vuole che la forma venga visualizzata in una pagina Web e le dimensioni della forma.
2.  Specificare **style**='position:relative (or relative)' per determinare il punto di base.
3.  Usare **left** e **top** per specificare l'offset dal punto di base.
4.  Usare **larghezza** e **altezza** per specificare le dimensioni della casella contenitore per la forma.
5.  Usare **z-index** per specificare l'ordine z della forma.

 

 