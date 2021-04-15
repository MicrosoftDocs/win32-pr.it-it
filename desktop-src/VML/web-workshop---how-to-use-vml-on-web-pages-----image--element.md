---
title: Utilizzo dell'elemento Image
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Web Workshop, elemento Image
- progettazione di pagine Web, elemento Image
- Vector Markup Language (la), elemento Image
- LA (Vector Markup Language), elemento Image
- Vector graphics, elemento Image
- Elemento image
- Elementi la, image
- Forme la, elemento Image
- Vector Markup Language (la), attributi della proprietà Crop
- LA (Vector Markup Language), attributi della proprietà Crop
- grafica vettoriale, attributi della proprietà Crop
- Forme la, attributi della proprietà Crop
- attributi della proprietà Crop
- Vector Markup Language (la), Acquisisci attributo proprietà
- LA (Vector Markup Language), Acquisisci attributo proprietà
- graphics vettoriale, Acquisisci attributo proprietà
- LA forme, Acquisisci attributo proprietà
- Acquisisci attributo proprietà
- Vector Markup Language (la), contrasto
- LA (Vector Markup Language), contrasto
- grafica vettoriale, contrasto
- Forme la, contrasto
- Vector Markup Language (la), attributo proprietà blacklevel
- LA (Vector Markup Language), attributo proprietà blacklevel
- grafica vettoriale, attributo proprietà blacklevel
- Forme la, attributo proprietà blacklevel
- attributo proprietà blacklevel
- Vector Markup Language (la), luminosità
- LA (Vector Markup Language), luminosità
- grafica vettoriale, luminosità
- Forme la, luminosità
- Vector Markup Language (la), attributo della proprietà di scala di grigi
- LA (Vector Markup Language), attributo della proprietà di scala di grigi
- grafica vettoriale, attributo Proprietà scala di grigi
- Forme la, attributo proprietà scale di grigi
- attributo della proprietà di scala di grigi
- Vector Markup Language (la), attributo di proprietà gamma
- LA (Vector Markup Language), attributo di proprietà gamma
- grafica vettoriale, attributo di proprietà gamma
- Forme la, attributo di proprietà gamma
- attributo della proprietà gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 820039ff76f3685eeea7a65e2bbc01578abbe581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517049"
---
# <a name="using-the-image-element"></a>Utilizzo dell'elemento Image

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Uso di `<image>`

In questo argomento verrà illustrato come utilizzare l' `<image>` elemento per visualizzare immagini con diversi effetti speciali.

Se si vuole visualizzare un'immagine che è stata caricata da un'origine esterna, in genere si usa l' `<img>` elemento fornito in HTML, quindi si posiziona l'attributo della proprietà **src** sul percorso del file di immagine.

In alternativa, è possibile usare l' `<image>` elemento fornito in la. Quando si usa l' `<image>` elemento, è possibile creare un solo file di immagine e quindi visualizzare l'immagine in modo diverso modificando gli attributi delle proprietà dell' `<image>` elemento. Inoltre, l' `<image>` elemento fornisce diversi effetti speciali che non è possibile eseguire utilizzando semplicemente l' `<img>` elemento HTML, ad esempio [ritaglio](#crop), [contrasto](#contrast), [luminosità](#brightness), [gamma](#gamma)e [scala di grigi](#grayscale).

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="crop"></a>raccolto

È possibile usare gli attributi di proprietà **CropBottom**, **CropTop**, **CropLeft** e **CropRight** dell' `<image>` elemento per visualizzare immagini diverse ritagliate dallo stesso file di immagine.

Il valore di questi attributi di ritaglio rappresenta il taglio percentuale dal bordo dell'immagine. Il valore può essere qualsiasi numero compreso tra 0 e 1. Per impostazione predefinita, il valore è impostato su 0, che indica nessun ritaglio dal bordo. Il valore 0,1 indica un ritaglio del 10% dal bordo, il valore 0,15 indica un ritaglio del 15% dal bordo e così via.

Per visualizzare, ad esempio, cinque immagini ritagliate dallo stesso file di immagine, è possibile usare l' `<image>` elemento e specificare valori di ritaglio diversi, come illustrato nella rappresentazione la seguente:

![image1.jpg (5770 byte)](images/image1.jpg)![\-2.jpg image1 (1969 byte)](images/image1-2.jpg)![\-3.jpg image1 (1148 byte)](images/image1-3.jpg)![\-4.jpg image1 (1686 byte)](images/image1-4.jpg)![\-5.jpg image1 (1364 byte)](images/image1-5.jpg)


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





La prima immagine, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , non ha alcun valore di ritaglio. Pertanto, il 100% dell'immagine originale viene visualizzato con una dimensione di 100 punti per 80 punti.

La seconda immagine, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , presenta alcuni valori di ritaglio. `cropbottom="0.2"` indica che il 20% dell'immagine verrà ritagliato dalla parte inferiore; `cropright="0.15"` indica che il 15% dell'immagine verrà ritagliato dal bordo destro. L'immagine rimanente viene quindi visualizzata con una dimensione di 85 punti per 64 punti.

Analogamente, le immagini terzo, quarto e quinto hanno alcuni valori di ritaglio. L'immagine originale viene ritagliata in base ai valori di ritaglio e viene quindi visualizzata in base al valore della larghezza e dell'altezza.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="contrast"></a>elevato

È possibile usare l'attributo della proprietà **Gain** dell' `<image>` elemento per visualizzare varie immagini con diverse impostazioni di contrasto.

Il valore dell'attributo della proprietà **Gain** può essere qualsiasi numero. Per impostazione predefinita, il valore è 1, che indica l'uso dello stesso contrasto dell'immagine originale. Il valore 0 indica nessun contrasto. Maggiore è il numero, maggiore è il contrasto.

Ad esempio, per visualizzare cinque immagini con impostazioni di contrasto diverse, è possibile usare l' `<image>` elemento e impostare un valore diverso per l'attributo **Gain** Property, come illustrato nella rappresentazione la seguente:

![image1.jpg (5770 byte)](images/image1.jpg)![\-2.jpg Image2 (270 byte)](images/image2-2.jpg)![\-3.jpg Image2 (1919 byte)](images/image2-3.jpg)![\-4.jpg Image2 (3143 byte)](images/image2-4.jpg)![\-5.jpg Image2 (1724 byte)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





Quando l'attributo **Gain** Property è impostato su 0, l'intera immagine diventa grigio perché non esiste alcun contrasto. Il contrasto è più evidente quando l'attributo della proprietà **Gain** è impostato su 3 rispetto a quando è impostato su 0,5. Il contrasto viene invertito quando l'attributo della proprietà **Gain** è impostato su un valore negativo, ad esempio-0,4.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="brightness"></a>luminosità

È possibile usare l'attributo della proprietà **blacklevel** dell' `<image>` elemento per visualizzare varie immagini con impostazioni di luminosità diverse.

Il valore dell'attributo della proprietà **blacklevel** può essere qualsiasi valore compreso tra 0 e 1. Per impostazione predefinita, il valore è 0, che indica che il livello di luminosità nell'immagine originale viene mantenuto. Il valore 1 indica il livello massimo di luminosità.

Ad esempio, per visualizzare cinque immagini con impostazioni di luminosità diverse, è possibile usare l' `<image>` elemento e impostare un valore diverso per l'attributo della proprietà **blacklevel** , come illustrato nella rappresentazione la seguente:

![image1.jpg (5770 byte)](images/image1.jpg)![\-2.jpg image3 (2579 byte)](images/image3-2.jpg)![\-3.jpg image3 (2330 byte)](images/image3-3.jpg)![\-4.jpg image3 (2727 byte)](images/image3-4.jpg)![\-5.jpg image3 (2435 byte)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="grayscale"></a>scala di grigi

È possibile usare l'attributo della proprietà **scala di grigi** dell' `<image>` elemento per visualizzare immagini con o senza scala di grigi.

Il valore dell'attributo della proprietà **scala di grigi** può essere true o false. Per impostazione predefinita, il valore è impostato su false in modo che l'immagine venga visualizzata in colore. Se il valore è impostato su true, l'immagine verrà visualizzata in scala di grigi.

Come illustrato nell'immagine seguente, ad esempio, la prima immagine usa l'impostazione predefinita (false) dell'attributo di scala di grigi ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ). Pertanto, l'immagine viene visualizzata in colore.

La seconda immagine imposta l'attributo scala di grigi su true ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ). Pertanto, l'immagine viene visualizzata in scala di grigi, come illustrato nella rappresentazione la seguente:

![image1.jpg (5770 byte)](images/image1.jpg)![\-2.jpg image4 (2138 byte)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="gamma"></a>gamma

È possibile usare l'attributo di proprietà **gamma** dell' `<image>` elemento per visualizzare immagini con impostazioni gamma diverse.

Il valore dell'attributo della proprietà gamma può essere qualsiasi valore compreso tra 0 e 1. Per impostazione predefinita, il valore è impostato su 1.

Per visualizzare, ad esempio, tre immagini con impostazioni gamma diverse, è possibile usare l' `<image>` elemento e impostare un valore diverso dell'attributo della proprietà **gamma** , come illustrato nella rappresentazione la seguente:

![\-1.jpg image5 (2714 byte)](images/image5-1.jpg)![\-2.jpg image5 (2729 byte)](images/image5-2.jpg)![\-3.jpg image5 (2726 byte)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858408) .

 

 