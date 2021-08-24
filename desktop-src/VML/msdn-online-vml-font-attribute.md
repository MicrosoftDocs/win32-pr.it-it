---
title: Attributo del tipo di carattere VML
description: Attributo del tipo di carattere VML
ms.assetid: 5a48fc54-e2dd-4b68-863c-3a83f9386108
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 074aa0672002dcbbac55d21ed27383d5a3fd6e3b9ccfe9125ad89c2c43ac71ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986661"
---
# <a name="vml-font-attribute"></a>Attributo del tipo di carattere VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Specifica un valore composto di attributi del tipo di carattere. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintassi dei tag**

<v: *element* style="font: *expression* ">

**Sintassi dello script**

*element* .style.font="*expression*"

*expression* = *elemento*.style.font

**Osservazioni:**

Definisce gli attributi di un tipo di carattere, tra cui famiglia, stile, peso, dimensioni e variante. L'ordine delle definizioni nella stringa è: **font-style,** **font-variant,** **font-weight,** **font-size,** **line-height** e **font-family.** I valori sono gli stessi degli attributi di stile HTML standard.

*Attributo standard VML*

**Esempio**

Il tipo di carattere del testo del percorso di testo è corsivo, maiuscoletto, grassetto, Arial a 36 punti.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic small-caps bold 36pt Arial"/>
   </v:line>
```



 

 