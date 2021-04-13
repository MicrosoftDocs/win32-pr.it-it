---
title: Utilizzo dell'elemento TipoForma
description: Utilizzo dell'elemento TipoForma
ms.assetid: ad9e5c00-fbee-4bec-b4cd-075cf5a4d8c7
keywords:
- Web Workshop, elemento TipoForma
- progettazione di pagine Web, elemento TipoForma
- Vector Markup Language (la), elemento TipoForma
- LA (Vector Markup Language), elemento TipoForma
- grafica vettoriale, elemento TipoForma
- elemento TipoForma
- Elementi la, TipoForma
- Forme la, elemento TipoForma
- Vector Markup Language (la), definizione di forme usate di frequente
- LA (Vector Markup Language), definizione di forme usate di frequente
- grafica vettoriale, definizione di forme usate di frequente
- definizione di forme usate di frequente
- LA forme, definizione di uso frequente
- Vector Markup Language (la), creazione di un'istanza di copie di forme
- LA (Vector Markup Language), creazione di un'istanza di copie di forme
- grafica vettoriale, creazione di istanze di copie di forme
- creazione di istanze di copie di forme
- LA forme, creazione di istanze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfa7ec47dde492231e8bcd54f68e4637454613b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474014"
---
# <a name="using-the-shapetype-element"></a>Utilizzo dell'elemento TipoForma

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

In questo argomento verrà illustrato come usare l' `<shapetype>` elemento per definire le forme usate di frequente e quindi creare un'istanza o creare forme da TipoForma.

Se si desidera disegnare molte forme con proprietà identiche o simili, è noioso se è necessario digitare ripetutamente gli stessi attributi di proprietà per ogni forma. LA fornisce l' `<shapetype>` elemento in modo che sia possibile definire un prototipo di una forma. È quindi possibile usare l' `<shape>` elemento per creare un'istanza di molte copie di forme dallo stesso TipoForma.

È possibile seguire i tre passaggi per definire un TipoForma e quindi creare un'istanza di una forma da TipoForma:

1.  Digitare un `<shapetype>` elemento e assegnargli un nome specificando l'attributo ID.
2.  Descrivere TipoForma usando i relativi attributi o sottoelementi della proprietà.
3.  Creare un'istanza di una forma digitando un `<shape>` elemento e fare riferimento all'attributo Type della forma all'attributo ID di TipoForma.

Si digitano, ad esempio, le righe seguenti per creare un TipoForma denominato "forme":


```HTML
<v:shapetype id="MyShape" >
</v:shapetype>
```



Modificare quindi il TipoForma impostando alcuni attributi delle proprietà, ad esempio `fillcolor="red" strokecolor="blue"` . In alternativa, è possibile usare sottoelementi all'interno di TipoForma, ad esempio, `<path>` `<fill>` , `<stroke>` (si parlerà di tali sottoelementi negli argomenti successivi).


```HTML
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue"...>
</v:shapetype>
```



Quindi, si crea un'istanza di una forma da TipoForma "forme" specificando `type="#MyShape"` , come illustrato nella seguente rappresentazione la. Questa forma eredita tutte le proprietà da TipoForma "forma" e viene visualizzata all'interno della casella che lo contiene a una dimensione di 100 per 80.


```HTML
<v:shape type="#MyShape" style='width:100;height:80'/>
```



È possibile creare un'istanza di un'altra forma da TipoForma "forme" specificando `type="#MyShape"` e sovrascrivendo alcune proprietà, ad esempio `fillcolor="maroon"` , come illustrato nella rappresentazione la seguente. Questa forma eredita tutte le proprietà da TipoForma "Shape" ad eccezione della proprietà FillColor e viene visualizzata all'interno della casella che lo contiene a una dimensione di 70 per 90.


```HTML
<v:shape type="#MyShape" fillcolor="maroon"
style='width:70; height:90'/>
```



Di seguito è illustrata la rappresentazione la completa per l'esempio precedente:

![\-1.gif tipo1 (477 byte)](images/type1-1.gif)![\-2.gif tipo1 (471 byte)](images/type1-2.gif)


```HTML
<body>
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue" coordsize="21600,21600"
path="m10860,2187c10451,1746,9529,1018,9015,730,7865,152,6685,,5415,,4175,
152,2995,575,1967,1305,1150,2187,575,3222,242,4220,,5410,242,6560,575,7597l10860,
21600,20995,7597c21480,6560,21600,5410,21480,4220,21115,3222,20420,2187,19632,
1305,18575,575,17425,152,16275,,15005,,13735,152,12705,730,12176,1018,11254,1746,
10860,2187xe">
</v:shapetype>
<v:shape type="#MyShape" style='width:100;height:80;'/>
<v:shape type="#MyShape" style='width:70;height:90;' fillcolor="maroon"/>
</body>
```





Come appreso, quando viene creata un'istanza di una forma da un TipoForma, eredita tutti gli attributi della proprietà da TipoForma. È possibile sovrascrivere alcuni o tutti gli attributi ereditati ridefinendo gli attributi all'interno dell' `<shape>` elemento. Tenere presente che l'ereditarietà è un solo livello. Questo perché solo un `<shape>` elemento può fare riferimento a un `<shapetype>` elemento. Un `<shapetype>` elemento non può fare riferimento A un altro `<shapetype>` elemento.

Inoltre, un TipoForma non appartiene ad alcun gruppo. Pertanto, l' `<shapetype>` elemento può essere visualizzato da solo o all'interno di un `<group>` elemento. È possibile disporre di molte forme all'interno di gruppi diversi che fanno riferimento allo stesso TipoForma. Se un TipoForma viene visualizzato all'interno di un gruppo, una forma che vive in un altro gruppo può comunque fare riferimento a questo TipoForma.

Nella rappresentazione la seguente, ad esempio, Rect1 e rect2 sono in GroupA e Rect3 è in GroupB. Viene creata un'istanza di tutti e tre i rettangoli da forma TipoForma.


```HTML
<body>
...
<v:shapetype id="MyShape" fillcolor="blue" strokecolor="red"...>
</v:shapetype>

<v:group id="GroupA"...>
<v:shape id="Rect1" type="#MyShape" .../>
<v:shape id="Rect2" type="#MyShape" strokecolor="black".../>
</v:group>

<v:group id="GroupB"...>
<v:shape id="Rect3" type="#MyShape" fillcolor="green".../>
</v:group>
...
</body>
```



Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858387) .

 

 