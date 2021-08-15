---
title: Attributo vml Font-Family
description: Attributo vml Font-Family
ms.assetid: 10586ae0-1480-4ffe-a690-ce8464e9bf41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1254be6f7264e0d8f77d5881a11b9c2ec5085a931a0cad713813c059c60e5e62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754739"
---
# <a name="vml-font-family-attribute"></a>Attributo vml Font-Family

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce la famiglia del tipo di carattere textpath. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Percorso di testo](msdn-online-vml-textpath-element.md)

**Sintassi dei tag**

<v: *element* style="font-family: *expression* ">

**Sintassi dello script**

*element* .style.fontfamily="*expression*"

*expression* = *elemento*.style.fontfamily

**Osservazioni:**

Definisce il nome del tipo di carattere. È possibile usare nomi specifici, ad esempio Arial, o tipi generici, ad esempio serif, sans-serif, cursive, sans o monospace. I valori sono gli stessi degli attributi di stile HTML standard.

*Attributo VML Standard*

**Esempio**

La famiglia di caratteri del testo è Arial.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 