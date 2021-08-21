---
title: Uso dell'elemento Shapetype
description: Uso dell'elemento Shapetype
ms.assetid: ad9e5c00-fbee-4bec-b4cd-075cf5a4d8c7
keywords:
- Workshop Web, elemento shapetype
- progettazione di pagine Web, elemento shapetype
- Vector Markup Language (VML), elemento shapetype
- VML (Vector Markup Language),elemento shapetype
- grafica vettoriale, elemento shapetype
- Elemento shapetype
- Elementi VML, shapetype
- Forme VML, elemento shapetype
- Vector Markup Language (VML), definizione di forme usate di frequente
- VML (Vector Markup Language), definizione di forme usate di frequente
- grafica vettoriale, definizione di forme usate di frequente
- definizione di forme usate di frequente
- Forme VML, definizione di forme usate di frequente
- Vector Markup Language (VML), creazione di istanze di copie di forme
- VML (Vector Markup Language), creazione di istanze di copie di forme
- grafica vettoriale, creazione di istanze di copie di forme
- creazione di istanze di copie di forme
- forme VML, creazione di istanze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d815d9f5f911e1a34d558496881ae606819d328a501c635ff463a84f2926ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512652"
---
# <a name="using-the-shapetype-element"></a>Uso dell'elemento Shapetype

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

In questo argomento verrà illustrato come usare l'elemento per definire forme usate di frequente e quindi creare un'istanza o creare forme dal `<shapetype>` tipo di forma.

Se si desidera disegnare molte forme con proprietà uguali o simili, sarebbe noioso se fosse necessario digitare ripetutamente gli stessi attributi di proprietà per ogni forma. VML fornisce `<shapetype>` l'elemento in modo che sia possibile definire un prototipo di una forma. È quindi possibile usare `<shape>` l'elemento per creare un'istanza di molte copie di forme dallo stesso tipo di forma.

È possibile seguire i tre passaggi per definire un tipo di forma e quindi creare un'istanza di una forma dal tipo di forma:

1.  Digitare un `<shapetype>` elemento e assegnargli un nome specificando l'attributo id.
2.  Descrivere il tipo di forma usando gli attributi o i sotto-elementi della proprietà.
3.  Creare un'istanza di una forma digitando un elemento e fare riferimento all'attributo type della `<shape>` forma all'attributo id del tipo di forma.

Ad esempio, digitare le righe seguenti per creare un tipo di forma denominato "MyShape":


```HTML
<v:shapetype id="MyShape" >
</v:shapetype>
```



Modificare quindi il tipo di forma impostando alcuni attributi di proprietà, ad esempio `fillcolor="red" strokecolor="blue"` . In caso contrario, è possibile usare sotto-elementi all'interno del tipo di forma, ad esempio , , (questi elementi secondari verranno trattati `<path>` `<fill>` negli argomenti `<stroke>` successivi).


```HTML
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue"...>
</v:shapetype>
```



Si crea quindi un'istanza di una forma dal tipo di forma "MyShape" specificando , come `type="#MyShape"` illustrato nella rappresentazione VML seguente. Questa forma eredita tutte le proprietà dal tipo di forma "MyShape" e viene visualizzata all'interno della casella contenitore con dimensioni di 100 per 80.


```HTML
<v:shape type="#MyShape" style='width:100;height:80'/>
```



È possibile creare un'istanza di un'altra forma dal tipo di forma "MyShape" specificando e sovrascrivendo alcune proprietà, ad esempio , come illustrato nella rappresentazione `type="#MyShape"` `fillcolor="maroon"` VML seguente. Questa forma eredita tutte le proprietà dal tipo di forma "MyShape", ad eccezione della proprietà fillcolor, e viene visualizzata all'interno della casella contenitore con dimensioni di 70 per 90.


```HTML
<v:shape type="#MyShape" fillcolor="maroon"
style='width:70; height:90'/>
```



Ecco la rappresentazione VML completa per l'esempio precedente:

![type1 \-1.gif (477 byte)](images/type1-1.gif)![type1 \-2.gif (471 byte)](images/type1-2.gif)


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





Come si è appreso, quando viene creata un'istanza di una forma da un tipo di forma, eredita tutti gli attributi della proprietà dal tipo di forma. È possibile sovrascrivere alcuni o tutti gli attributi ereditati ridefinendo gli attributi all'interno `<shape>` dell'elemento . Tenere presente che l'ereditarietà è di un solo livello. Ciò è dovuto al fatto che solo `<shape>` un elemento può fare riferimento a un elemento `<shapetype>` . Un `<shapetype>` elemento non può fare riferimento a un altro `<shapetype>` elemento.

Inoltre, un tipo di forma non appartiene ad alcun gruppo. Pertanto, `<shapetype>` l'elemento può essere visualizzato da solo o all'interno di un `<group>` elemento . È possibile avere molte forme all'interno di gruppi diversi che fanno riferimento allo stesso tipo di forma. Se un tipo di forma viene visualizzato all'interno di un gruppo, una forma che si trova in un altro gruppo può comunque fare riferimento a questo tipo di forma.

Nella rappresentazione VML seguente, ad esempio, Rect1 e Rect2 si trova in GroupA e Rect3 si trova in GroupB. Viene creata un'istanza di tutti e tre i rettangoli dal tipo di forma MyShape.


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



Per altre informazioni su questo elemento, vedere la [specifica VML](https://www.w3.org/TR/NOTE-VML#-toc416858387) .

 

 