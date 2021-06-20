---
title: Raggruppamento di forme
description: Questo articolo descrive il raggruppamento di forme in VML, una funzionalità deprecata a Internet Explorer Windows 9.
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- Workshop Web, raggruppamento di forme
- progettazione di pagine Web, raggruppamento di forme
- Vector Markup Language (VML), raggruppamento di forme
- VML (Vector Markup Language),raggruppamento di forme
- grafica vettoriale, raggruppamento di forme
- forme VML, raggruppamento
- raggruppamento di forme
- Vector Markup Language (VML),elemento group
- VML (Vector Markup Language),elemento group
- grafica vettoriale, elemento group
- Elemento group
- elementi VML, gruppo
- Vector Markup Language (VML), spazio delle coordinate locale
- VML (Vector Markup Language),spazio delle coordinate locale
- grafica vettoriale, spazio delle coordinate locale
- spazio delle coordinate locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e0c3073f55d23c15734b5d5ddfa886e7291530
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407704"
---
# <a name="grouping-shapes"></a>Raggruppamento di forme

Questo argomento descrive VML, una funzionalità deprecata a Internet Explorer Windows 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Come si è appreso, è possibile disegnare facilmente singole forme usando VML. In questa sezione verranno illustrati i vantaggi del raggruppamento delle forme e verrà illustrato come raggruppare le forme.

Se si hanno molte forme che devono essere ridimensionate, spostate o ruotate insieme, può essere noioso impostare gli attributi singolarmente per ogni forma. Inoltre, è possibile aumentare il margine per gli errori. Sarebbe meglio raggruppare le forme e quindi impostare gli attributi per l'intero gruppo.

In VML è possibile usare l'elemento per raggruppare più forme in modo che possano `<group>` essere trasformate come un'unica unità. Ad esempio, come illustrato nella rappresentazione VML seguente, è possibile raggruppare facilmente due forme.


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



Quando le forme vengono raggruppate, usano lo [spazio delle coordinate locale](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) del gruppo. Di conseguenza, le forme all'interno di un gruppo possono essere ridimensionate e spostate insieme. Verranno visualizzati altri esempi nell'argomento Usare lo spazio delle coordinate locali.

All'interno di un gruppo è possibile avere tutte le forme o i gruppi desiderati. Quando un gruppo si trova all'interno di un altro gruppo, viene chiamato "gruppo annidato". Non esiste alcuna limitazione ai livelli di annidamento.

Ad esempio, le righe seguenti illustrano un gruppo annidato a 3 livelli. Shape3 e Shape4 sono in GroupC. Shape2 e GroupC sono in GroupB. Shape1 e GroupB sono in GroupA.


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



Per altre informazioni su questo elemento, vedere la [specifica VML](https://www.w3.org/TR/NOTE-VML#-toc416858388) .

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="summary"></a>Riepilogo

È possibile usare `<group>` l'elemento per raggruppare più forme in modo che possano essere trasformate come un'unica unità.

 

 