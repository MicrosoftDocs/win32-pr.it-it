---
title: Utilizzo dell'elemento formules
description: Utilizzo dell'elemento formules
ms.assetid: f5a381b4-4132-4b66-b41a-3cada26b41e2
keywords:
- Web Workshop, elemento formule
- progettazione di pagine Web, elemento formule
- Vector Markup Language (la), elemento formule
- LA (Vector Markup Language), elemento formule
- graphics vettoriale, elemento formule
- elemento formules
- Elementi la, formule
- Forme la, elemento formule
- Vector Markup Language (la), definizione dei percorsi per le forme
- LA (Vector Markup Language), definizione dei percorsi per le forme
- grafica vettoriale, definizione dei percorsi per le forme
- LA forme, definizione di percorsi
- definizione dei percorsi per le forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85ce4ebb6eea05895edf974e3ca86b1fa2ad923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046803"
---
# <a name="using-the-formulas-element"></a>Utilizzo dell'elemento formules

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

In questo argomento verrà illustrato come utilizzare il `<formulas>` sottoelemento per definire un percorso regolabile per una forma.

È possibile inserire il <formulas> sottoelemento all'interno `<shape>` o `<shapetype>` per definire formule che possono variare il percorso di una forma. All'interno del `<formulas>` sottoelemento, un sottoelemento **f** definisce una formula in modo che un valore venga valutato in base alla formula. Ad esempio, la formula `<v:f eqn="prod 10 4 5"/>` definisce un valore equivalente a "10 x 4/5".

È possibile inserire molti elementi secondari **f** all'interno `<formulas>` di un sottoelemento. Le formule possono fare riferimento ai valori definiti in precedenza in altre formule all'interno dello stesso `<formulas>` sottoelemento. Il valore definito nella prima formula può essere indicato come @0 , il valore definito nella seconda formula può essere definito come @1 e così via...

Inoltre, è possibile specificare l'attributo di proprietà **ADJ** dell' `<shape>` elemento, ad esempio ADJ = "100, 200, 150". All'interno dell' `<formulas>` elemento è quindi possibile fare riferimento a tali valori nell'elenco **ADJ** . Il primo valore (100) nell'elenco **ADJ** può essere definito come \# 0, il secondo valore (200) può essere definito come \# 1 e così via.

Ad esempio, per creare una faccia sorridente, è possibile digitare la rappresentazione la seguente:

![shape1.gif (735 byte)](images/shape1f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="17520"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





-   `adj="17520"` definisce un valore (= 17520). È possibile fare riferimento a questo valore come \# 0.
-   La prima formula, `<v:f eqn="sum 33030 0 #0"/>` , definisce il valore (= 33030 + 0- \# 0). È possibile fare riferimento a questo valore come @0 .
-   La seconda formula, `<v:f eqn="prod #0 4 3"/>` , definisce il valore (= \# 0 \* 4/3). È possibile fare riferimento a questo valore come @1 .
-   La terza formula, `<v:f eqn="prod @0 1 3"/>` , definisce il valore (= @0 \* 1/3). È possibile fare riferimento a questo valore come @2 .
-   La quarta formula, `<v:f eqn="sum @1 0 @2"/>` , definisce il valore (= @1 + 0 -@2 ). È possibile fare riferimento a questo valore come @3 .
-   All'interno dell' `<path>` elemento vengono utilizzati i valori definiti nelle prime ( @0 ) e le quattro @3 formule () per determinare il contorno della forma.

Se si modifica l'elenco **ADJ** , ad esempio `adj="20000"` , verranno modificati anche i valori delle formule che fanno riferimento all'elenco **ADJ** , che influisce sulla faccia sorridente come segue:

![shape2.gif (765 byte)](images/shape2f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="20000"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858392) .

 

 