---
title: Forme di raggruppamento
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- Workshop Web, forme di raggruppamento
- progettazione di pagine Web, raggruppamento di forme
- Vector Markup Language (la), forme di raggruppamento
- LA (Vector Markup Language), forme di raggruppamento
- grafica vettoriale, forme raggruppamento
- LA forme, raggruppamento
- forme di raggruppamento
- Vector Markup Language (la), elemento Group
- LA (Vector Markup Language), elemento Group
- grafica vettoriale, elemento Group
- Elemento group
- Elementi la, gruppo
- Vector Markup Language (la), spazio delle coordinate locale
- LA (Vector Markup Language), spazio delle coordinate locale
- grafica vettoriale, spazio delle coordinate locale
- spazio delle coordinate locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59eed282094e2d24d2d27e338b93731eaaa1eec0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047262"
---
# <a name="grouping-shapes"></a>Forme di raggruppamento

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Come si è appreso, è possibile creare facilmente singole forme usando la. In questa sezione vengono illustrati i vantaggi derivanti dal raggruppamento di forme e come raggruppare le forme.

Se erano presenti molte forme che dovevano essere ridimensionate, spostate o ruotate insieme, sarebbe noioso impostare gli attributi singolarmente per ogni forma. Inoltre, è possibile aumentare il margine per gli errori. Sarebbe opportuno raggruppare le forme, quindi impostare gli attributi per l'intero gruppo.

In la è possibile usare l' `<group>` elemento per raggruppare molte forme in modo che possano essere trasformate come un'unica unità. Ad esempio, come illustrato nella seguente rappresentazione la, è possibile raggruppare facilmente due forme.


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



Quando le forme vengono raggruppate, utilizzano lo [spazio delle coordinate locale](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) del gruppo. Pertanto, le forme all'interno di un gruppo possono essere ridimensionate e spostate insieme. Per altri esempi, vedere l'argomento usare lo spazio delle coordinate locali.

All'interno di un gruppo, è possibile avere tutte le forme o i gruppi desiderati. Quando un gruppo si trova all'interno di un altro gruppo, viene definito "gruppo annidato". Non esiste alcuna limitazione per i livelli di annidamento.

Ad esempio, le righe seguenti illustrano un gruppo annidato a 3 livelli. Shape3 e Shape4 sono in GroupC. Shape2 e GroupC sono in GroupB. Shape1 e GroupB si trovano nel gruppo a.


```HTML
<body>
   <v:group id="GroupA"...>
      <v:shape id="Shape1"...></v:shape>
      <v:group id="GroupB"...>
         <v:shape id="Shape2"...></v:shape>
         <v:group id="GroupC"...>
            <v:shape id="Shape3"...></v:shape>
            <v:shape id="Shape4"...></v:shape>
         </v:group>
      </v:group>
   </v:group>
</body>
```



Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858388) .

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="summary"></a>Riepilogo

È possibile utilizzare l' `<group>` elemento per raggruppare molte forme in modo che possano essere trasformate come un'unica unità.

 

 