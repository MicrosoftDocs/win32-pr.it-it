---
title: Attributo DoubleClickNotify di la
description: Attributo DoubleClickNotify di la
ms.assetid: 003a87f5-29c1-484e-ac15-2e4cb8e854ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16be329952cfff23957f961fb6d29198ad173898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337607"
---
# <a name="vml-doubleclicknotify-attribute"></a>Attributo DoubleClickNotify di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Invia un messaggio di evento quando si fa doppio clic su una forma. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* o:doubleclicknotify = " *Expression* " >

**Osservazioni:**

Il valore predefinito è **false**, che indica che l'evento non verrà generato.

*Attributo Microsoft Office Extensions*

**Esempio**

Quando si fa doppio clic, la forma attiverà un evento di doppio clic.


```HTML
   <v:rect id=myrect fillcolor="red" o:doubleclicknotify="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 