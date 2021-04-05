---
title: Utilizzo dell'elemento Handles
description: Utilizzo dell'elemento Handles
ms.assetid: d748f74c-40e5-499a-bb61-94862eb3811c
keywords:
- Web Workshop, Handles-elemento
- progettazione di pagine Web, Handles-elemento
- Vector Markup Language (la), Handles-elemento
- LA (Vector Markup Language), Handles-elemento
- Vector graphics, Handles-elemento
- Handles-elemento
- Elementi la, handle
- Forme la, Handles-elemento
- Vector Markup Language (la), associazione di testo a forme
- LA (Vector Markup Language), associazione di testo a forme
- grafica vettoriale, associazione di testo a forme
- LA forme, associazione di testo
- associazione di testo a forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54c721d50f51c46cd4bf08393e85ad83307fc1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046802"
---
# <a name="using-the-handles-element"></a>Utilizzo dell'elemento Handles

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

In questo argomento verrà illustrato come utilizzare l' `<handles>` elemento per aggiungere testo a una forma.

È possibile inserire il `<handles>` sottoelemento all'interno `<shape>` o `<shapetype>` per definire gli elementi dell'interfaccia utente che possono variare i valori di **ADJ** sulla forma.

Ad esempio, come illustrato nella seguente rappresentazione la, è possibile specificare un handle di regolazione (casella gialla) che gli utenti possono semplicemente trascinare per regolare la forma.

Nota: gli handle sono disponibili quando questa forma la viene visualizzata nelle applicazioni Microsoft Office, in cui la forma è progettata per essere manipolabile.

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





Si noti che l'unica differenza tra la rappresentazione la precedente e quella seguente è il valore **ADJ** .

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





Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858393) .

 

 