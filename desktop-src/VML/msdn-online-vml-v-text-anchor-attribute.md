---
title: LA V-text-anchor-attributo
description: LA V-text-anchor-attributo
ms.assetid: d6e2f60c-5cc7-4340-a9cd-b6c2b0b5b0be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 603f118a260c8ce9c271128fa642e9e2ae569806
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399376"
---
# <a name="vml-v-text-anchor-attribute"></a>LA V-text-anchor-attributo

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce l'ancoraggio verticale del testo in una casella di testo. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintassi Tag**

<v: *element* v-text-anchor = " *Expression* " >

**Osservazioni:**

I possibili valori sono:

-   **Top** (impostazione predefinita)
-   **intermedio**
-   **parte inferiore**
-   **in alto al centro**
-   **Centro centrale**
-   **in basso al centro**
-   **Top-Baseline**
-   **linea di base inferiore**
-   **Top-Center-Baseline**
-   **Bottom-Center-Baseline**

Il testo verrà ancorato a una posizione verticale nella casella di testo come indicato dal valore dell'attributo. L'allineamento di un ancoraggio del testo diventa evidente solo se [MSO-Fit-Text-to-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) è **false**. Questo attributo è diverso dall'attributo di stile **allineamento verticale** , che viene usato per i linguaggi ideogrammi.

Questo attributo viene utilizzato da Microsoft Office per archiviare i dati nei documenti Web, ma non viene eseguito il rendering in Microsoft Internet Explorer 5 o versione successiva.

*Attributo standard la*

**Esempio**

Il testo è allineato alla parte inferiore della casella di testo.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox style="v-text-anchor:bottom" id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 