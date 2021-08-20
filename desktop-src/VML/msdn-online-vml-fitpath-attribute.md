---
title: Attributo VmL FitPath
description: Attributo VmL FitPath
ms.assetid: f15775ed-f7b7-45d9-83ed-e307daf7451b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8863fb4d8a382ac9ccddaf7cc55fe5e8ceeff221dc1f816e340fa0a78cf9d7b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124784"
---
# <a name="vml-fitpath-attribute"></a>Attributo VmL FitPath

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce se il testo si adatta al percorso di una forma. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintassi dei tag**

<v: *elemento* fitpath=" *espressione* ">

**Sintassi dello script**

*element* .fitpath="*expression*"

*expression* = *elemento*.fitpath

**Osservazioni:**

Se **True,** ridimensiona il testo per riempire il percorso su cui si trova. Il valore predefinito è **False**.

*Attributo standard VML*

**Esempio**

Il testo si adatterà al percorso.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitpath="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 