---
title: Uso dell'elemento Handles
description: Uso dell'elemento Handles
ms.assetid: d748f74c-40e5-499a-bb61-94862eb3811c
keywords:
- Web workshop, elemento handles
- progettazione di pagine Web,gestisce l'elemento
- Vector Markup Language (VML), gestisce l'elemento
- VML (Vector Markup Language),gestisce l'elemento
- grafica vettoriale,gestisce l'elemento
- Elemento handles
- elementi VML,handle
- Forme VML,gestisce l'elemento
- Vector Markup Language (VML), collegamento di testo alle forme
- VML (Vector Markup Language), collegamento di testo alle forme
- grafica vettoriale, collegamento di testo alle forme
- forme VML, collegamento di testo
- collegamento di testo alle forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d504024a3d5c42caf8af116a08e5bd8787905991f14c4181fe3a75b10f4814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057210"
---
# <a name="using-the-handles-element"></a>Uso dell'elemento Handles

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

In questo argomento verrà illustrato come usare `<handles>` l'elemento per associare testo a una forma.

È possibile inserire il sotto-elemento all'interno o per definire elementi dell'interfaccia utente che possono variare i `<handles>` `<shape>` valori `<shapetype>` **adj** sulla forma.

Ad esempio, come illustrato nella rappresentazione VML seguente, è possibile fornire un quadratino di regolazione (casella gialla) che gli utenti possono semplicemente trascinare per regolare la forma.

Nota: i punti di manipolazione sono disponibili quando questa forma VML viene visualizzata Microsoft Office applicazioni, in cui la forma deve essere manipulable.

![shape1.gif (564 byte)](images/shape1h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="16200,5400"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





Si noti che l'unica differenza tra la rappresentazione VML precedente e quella seguente è il **valore adj.**

![shape2.gif (1361 byte)](images/shape2h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="11304,6600"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





Per altre informazioni su questo elemento, vedere la specifica [VML](https://www.w3.org/TR/NOTE-VML#-toc416858393) .

 

 