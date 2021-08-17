---
title: Attributo vml Font-Size
description: Attributo vml Font-Size
ms.assetid: 49394cd5-3009-424a-97d3-28c85d874bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 401d66668b0a86b92e453ac2e4a8a9adb96411131cc90f7bf14bd22be67e6775
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346578"
---
# <a name="vml-font-size-attribute"></a>Attributo vml Font-Size

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce le dimensioni del tipo di carattere. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Percorso di testo](msdn-online-vml-textpath-element.md)

**Sintassi dei tag**

<v: *element* style="font-size: *expression* ">

**Sintassi dello script**

*element* .style.fontsize="*expression*"

*expression* = *elemento*.style.fontsize

**Osservazioni:**

La dimensione del carattere è definita in punti. I valori sono gli stessi degli attributi di stile HTML standard.

*Attributo VML Standard*

**Esempio**

La dimensione del carattere è di 36 punti.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 