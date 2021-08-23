---
title: Uso dell'elemento Formulas
description: Uso dell'elemento Formulas
ms.assetid: f5a381b4-4132-4b66-b41a-3cada26b41e2
keywords:
- Workshop Web, elemento formulas
- progettazione di pagine Web, elemento formula
- Vector Markup Language (VML), elemento formulas
- VML (Vector Markup Language),elemento formulas
- grafica vettoriale,elemento formulas
- Elemento formulas
- elementi VML, formule
- Forme VML, elemento formula
- Vector Markup Language (VML), definizione di percorsi per le forme
- VML (Vector Markup Language), definizione dei percorsi per le forme
- grafica vettoriale, definizione di percorsi per le forme
- forme VML, definizione di tracciati
- definizione di percorsi per le forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23810ae6612e18132566c7d546db7f1f3a569871050b7919cbd8512f3d832808
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512802"
---
# <a name="using-the-formulas-element"></a>Uso dell'elemento Formulas

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

In questo argomento verrà illustrato come usare il `<formulas>` sotto-elemento per definire un tracciato modificabile per una forma.

È possibile inserire il <formulas> sotto-elemento all'interno di o per `<shape>` definire formule che possono variare il percorso di una `<shapetype>` forma. `<formulas>`All'interno del sotto-elemento, un sotto-elemento **f** definisce una formula in modo che un valore viene valutato in base a tale formula. Ad esempio, la formula `<v:f eqn="prod 10 4 5"/>` definisce un valore equivalente a "10 x 4/ 5".

È possibile inserire molti **sotto-elementi f** all'interno di un `<formulas>` sotto-elemento. Le formule possono fare riferimento ai valori definiti in precedenza in altre formule all'interno dello stesso `<formulas>` sotto-elemento. Il valore definito nella prima formula può essere definito come , il valore definito nella seconda formula può essere definito e @0 @1 così via.

È anche possibile specificare l'attributo della proprietà **adj** dell'elemento, ad esempio `<shape>` adj="100, 200, 150". `<formulas>`All'interno dell'elemento è quindi possibile fare riferimento a tali valori **nell'elenco adj.** Il primo valore (100) **nell'elenco adj** può essere indicato come 0, il secondo valore (200) può essere indicato come 1 e \# \# così via.

Ad esempio, per disegnare un viso sorridente, è possibile digitare la rappresentazione VML seguente:

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





-   `adj="17520"` definisce un valore (= 17520). È possibile fare riferimento a questo valore \# come 0.
-   La prima formula, `<v:f eqn="sum 33030 0 #0"/>` , definisce il valore (= 33030 + 0 - \# 0). È possibile fare riferimento a questo valore come @0 .
-   La seconda formula, `<v:f eqn="prod #0 4 3"/>` , definisce il valore (= \# 0 \* 4/3). È possibile fare riferimento a questo valore come @1 .
-   La terza formula, `<v:f eqn="prod @0 1 3"/>` , definisce il valore (= @0 \* 1/3). È possibile fare riferimento a questo valore come @2 .
-   La quarta formula, `<v:f eqn="sum @1 0 @2"/>` , definisce il valore (= + @1 -@2 0). È possibile fare riferimento a questo valore come @3 .
-   All'interno dell'elemento vengono usati i valori definiti nella prima formula ( ) e nella quarta formula ( ) per determinare la `<path>` @0 struttura della @3 forma.

Se si modifica **l'elenco adj,** ad esempio , verranno modificati anche i valori delle formule che fanno riferimento all'elenco `adj="20000"` **adj,** influenzando il viso sorridente come segue:

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





Per altre informazioni su questo elemento, vedere la [specifica VML](https://www.w3.org/TR/NOTE-VML#-toc416858392) .

 

 