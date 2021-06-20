---
title: Uso dell'elemento Image
description: Questo articolo descrive l'uso dell'elemento Image in VML, una funzionalità deprecata a Internet Explorer 9 di Windows.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Web workshop, elemento image
- progettazione di pagine Web, elemento image
- Vector Markup Language (VML), elemento image
- VML (Vector Markup Language),elemento image
- grafica vettoriale, elemento image
- Elemento image
- elementi VML, immagine
- Forme VML, elemento image
- Vector Markup Language (VML), attributi delle proprietà crop
- VML (Vector Markup Language),attributi delle proprietà crop
- grafica vettoriale, attributi delle proprietà di ritaglio
- Forme VML, attributi delle proprietà di ritaglio
- Attributi delle proprietà di ritaglio
- Vector Markup Language (VML), ottenere l'attributo della proprietà
- VML (Vector Markup Language),ottenere l'attributo della proprietà
- grafica vettoriale, attributo della proprietà gain
- Forme VML,ottenere l'attributo della proprietà
- Attributo della proprietà gain
- Vector Markup Language (VML), contrasto
- VML (Vector Markup Language),contrasto
- grafica vettoriale, contrasto
- Forme VML,contrasto
- Vector Markup Language (VML), attributo della proprietà blacklevel
- VML (Vector Markup Language),attributo della proprietà blacklevel
- vector graphics,blacklevel - attributo della proprietà
- Forme VML, attributo della proprietà blacklevel
- Attributo della proprietà blacklevel
- Vector Markup Language (VML), luminosità
- VML (Vector Markup Language),luminosità
- grafica vettoriale, luminosità
- Forme VML, luminosità
- Vector Markup Language (VML), attributo della proprietà grayscale
- VML (Vector Markup Language),attributo della proprietà grayscale
- grafica vettoriale, attributo della proprietà grayscale
- Forme VML, attributo della proprietà grayscale
- Attributo della proprietà grayscale
- Vector Markup Language (VML), attributo della proprietà gamma
- VML (Vector Markup Language),attributo della proprietà gamma
- grafica vettoriale, attributo della proprietà gamma
- Forme VML, attributo della proprietà gamma
- Attributo della proprietà gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572acef76afc42e02f476ca1825ef2541f596380
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407804"
---
# <a name="using-the-image-element"></a>Uso dell'elemento Image

Questo argomento descrive VML, una funzionalità deprecata a Internet Explorer 9 di Windows. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Uso di `<image>`

In questo argomento verrà illustrato come usare l'elemento `<image>` per visualizzare immagini con vari effetti speciali.

Se si desidera visualizzare un'immagine caricata da un'origine esterna, in genere si usa l'elemento fornito in HTML e quindi si punta l'attributo della proprietà src al percorso del file di `<img>` immagine. 

In alternativa, è possibile usare `<image>` l'elemento fornito in VML. Quando si usa l'elemento , è possibile creare un solo file di immagine e quindi visualizzare l'immagine in modo diverso modificando gli attributi `<image>` delle proprietà `<image>` dell'elemento. Inoltre, l'elemento fornisce diversi effetti speciali che non è possibile eseguire semplicemente usando l'elemento HTML, ad esempio il ritaglio, il `<image>` `<img>` [](#crop) [contrasto,](#contrast) [](#brightness)la luminosità, la [gamma](#gamma)e la scala di [grigi.](#grayscale)

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="crop"></a>Raccolto

È possibile usare gli attributi delle proprietà **cropbottom**, **croptop**, **cropleft** e **cropright** dell'elemento per visualizzare immagini diverse ritagliate dallo `<image>` stesso file di immagine.

Il valore di questi attributi di ritaglio rappresenta la percentuale di taglio dal bordo dell'immagine. Il valore può essere qualsiasi numero compreso tra 0 e 1. Per impostazione predefinita, il valore è impostato su 0, a indicare che non viene ritagliato dal bordo. Il valore 0,1 indica un ritaglio del 10% dal bordo, Il valore 0,15 indica un ritaglio del 15% dal bordo e così via.

Ad esempio, per visualizzare cinque immagini tutte ritagliate dallo stesso file di immagine, è possibile usare l'elemento e specificare valori di ritaglio diversi, come illustrato nella rappresentazione `<image>` VML seguente:

![image1.jpg (5770 byte)](images/image1.jpg)![image1 \-2.jpg (1969 byte)](images/image1-2.jpg)![image1 \-3.jpg (1148 byte)](images/image1-3.jpg)![image1 \-4.jpg (1686 byte)](images/image1-4.jpg)![image1 \-5.jpg (1364 byte)](images/image1-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:85pt;height:64pt' src="image1.jpg"
cropbottom="0.2" cropright="0.15"/>
<v:image style='width:50pt;height:44pt' src="image1.jpg"
cropbottom="0.45" cropleft="0.5"/>
<v:image style='width:80pt;height:56pt' src="image1.jpg"
croptop="0.3" cropright="0.2"/>
<v:image style='width:70pt;height:48pt' src="image1.jpg"
croptop="0.4" cropleft="0.3"/>
```





La prima immagine, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , non ha alcun valore di ritaglio. Di conseguenza, il 100% dell'immagine originale viene visualizzato con dimensioni di 100 punti per 80 punti.

La seconda immagine, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , ha alcuni valori di ritaglio. `cropbottom="0.2"` indica che il 20% dell'immagine verrà ritagliato dal basso; `cropright="0.15"` indica che il 15% dell'immagine verrà ritagliato dal bordo destro. L'immagine rimanente viene quindi visualizzata con una dimensione di 85 punti per 64 punti.

Analogamente, la terza, la quarta e la quinta immagine hanno alcuni valori di ritaglio. L'immagine originale viene ritagliata in base ai valori di ritaglio e quindi visualizzata in base al valore di larghezza e altezza.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="contrast"></a>elevato

È possibile usare **l'attributo della** proprietà gain dell'elemento per visualizzare diverse immagini con impostazioni `<image>` di contrasto diverse.

Il valore **dell'attributo della proprietà gain** può essere qualsiasi numero. Per impostazione predefinita, il valore è 1, che indica l'uso dello stesso contrasto dell'immagine originale. Il valore 0 indica nessun contrasto. Maggiore è il numero, maggiore è il contrasto.

Ad esempio, per visualizzare cinque immagini con impostazioni di contrasto diverse, è possibile usare l'elemento e impostare un valore diverso per l'attributo della proprietà gain, come illustrato nella rappresentazione `<image>` VML seguente: 

![image1.jpg (5770 byte)](images/image1.jpg)![image2 \-2.jpg (270 byte)](images/image2-2.jpg)![image2 \-3.jpg (1919 byte)](images/image2-3.jpg)![image2 \-4.jpg (3143 byte)](images/image2-4.jpg)![image2 \-5.jpg (1724 byte)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





Quando **l'attributo della** proprietà gain è impostato su 0, l'intera immagine diventa grigia perché non è presente alcun contrasto. Il contrasto è più evidente quando **l'attributo della** proprietà gain è impostato su 3 rispetto a quando è impostato su 0,5. Il contrasto viene invertito quando **l'attributo della** proprietà gain è impostato su un valore negativo, ad esempio -0,4.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="brightness"></a>luminosità

È possibile usare **l'attributo della proprietà blacklevel** dell'elemento `<image>` per visualizzare varie immagini con impostazioni di luminosità diverse.

Il valore **dell'attributo della proprietà blacklevel** può essere qualsiasi valore compreso tra 0 e 1. Per impostazione predefinita, il valore è 0, a indicare che il livello di luminosità nell'immagine originale viene mantenuto. Il valore 1 indica il livello massimo di luminosità.

Ad esempio, per visualizzare cinque immagini con impostazioni di luminosità diverse, è possibile usare l'elemento e impostare un valore diverso per l'attributo della proprietà blacklevel, come illustrato nella rappresentazione `<image>` VML seguente: 

![image1.jpg (5770 byte)](images/image1.jpg)![image3 \-2.jpg (2579 byte)](images/image3-2.jpg)![image3 \-3.jpg (2330 byte)](images/image3-3.jpg)![image3 \-4.jpg (2727 byte)](images/image3-4.jpg)![image3 \-5.jpg (2435 byte)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="grayscale"></a>scala di grigi

È possibile usare **l'attributo della proprietà grayscale** dell'elemento `<image>` per visualizzare immagini con o senza gradazioni di grigio.

Il valore **dell'attributo della proprietà grayscale** può essere true o false. Per impostazione predefinita, il valore è impostato su false in modo che l'immagine verrà visualizzata a colori. Se il valore è impostato su true, l'immagine verrà visualizzata in scala di grigi.

Ad esempio, come illustrato nell'immagine seguente, la prima immagine usa l'impostazione predefinita (false) dell'attributo della scala di grigi ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ). Di conseguenza, l'immagine viene visualizzata a colori.

La seconda immagine imposta l'attributo della scala di grigi su true ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ). Di conseguenza, l'immagine viene visualizzata in scala di grigi, come illustrato nella rappresentazione VML seguente:

![image1.jpg (5770 byte)](images/image1.jpg)![image4 \-2.jpg (2138 byte)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="gamma"></a>gamma

È possibile usare **l'attributo della** proprietà gamma dell'elemento per visualizzare immagini con impostazioni `<image>` gamma diverse.

Il valore dell'attributo della proprietà gamma può essere qualsiasi valore compreso tra 0 e 1. Per impostazione predefinita, il valore è impostato su 1.

Ad esempio, per visualizzare tre immagini con impostazioni gamma diverse, è possibile usare l'elemento e impostare un valore diverso dell'attributo della proprietà gamma, come illustrato nella rappresentazione `<image>` VML seguente: 

![image5 \-1.jpg (2714 byte)](images/image5-1.jpg)![image5 \-2.jpg (2729 byte)](images/image5-2.jpg)![image5 \-3.jpg (2726 byte)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





Per altre informazioni su questo elemento, vedere la [specifica VML](https://www.w3.org/TR/NOTE-VML#-toc416858408) .

 

 