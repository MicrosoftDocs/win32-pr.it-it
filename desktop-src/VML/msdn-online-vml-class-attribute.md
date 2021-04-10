---
title: Attributo della classe la
description: Attributo della classe la
ms.assetid: 4030b8b7-fcc9-4153-8004-81935a347a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94bdc723ba9be335afc43023ab89b88834c55474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963247"
---
# <a name="vml-class-attribute"></a>Attributo della classe la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Fa riferimento a una definizione di uno stile CSS. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* class = " *Expression* " >

**Sintassi dello script**

*element* . NomeClasse = "*Expression*"

*espressione* = *element*. NomeClasse

**Osservazioni:**

L'attributo della **classe** è simile all'attributo della **classe** HTML standard usato con i fogli di stile CSS.

Si noti che **NomeClasse** viene usato al posto della **classe** per lo scripting. Si noti inoltre che, per gli script, è possibile leggere solo **NomeClasse** ; Se si modifica il valore di **NomeClasse** , il rendering della forma non viene modificato.

*Attributo standard la*

**Vedere anche**

[Con forme](shape-element--vml.md)

**Esempio**

Viene creata una classe per **Width** con lo stile


```HTML
   .narrowstyle {width:50;height:100}
```



Viene quindi fatto riferimento alla larghezza includendo lo stile. Si noti che la larghezza andheight non è definita nell'attributo **Style** , ma verrà definita dallo stile.


```HTML
   <v:shape id="rect01" class="narrowstyle"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



Si noti che la **classe** si applica solo agli attributi di tipo CSS.

 

 