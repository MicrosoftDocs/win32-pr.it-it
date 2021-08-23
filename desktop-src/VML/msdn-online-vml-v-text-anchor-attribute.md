---
title: Attributo V-Text-Anchor VML
description: Attributo V-Text-Anchor VML
ms.assetid: d6e2f60c-5cc7-4340-a9cd-b6c2b0b5b0be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7c4b355aa4e56e3b0320200a092a66aa1f504b16be02f697e1335cd295627c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057699"
---
# <a name="vml-v-text-anchor-attribute"></a>Attributo V-Text-Anchor VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce l'ancoraggio verticale del testo in una casella di testo. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintassi dei tag**

<v: *element* v-text-anchor=" *expression* ">

**Osservazioni:**

I possibili valori sono:

-   **top** (impostazione predefinita)
-   **Mezzo**
-   **Fondoschiena**
-   **in alto al centro**
-   **middle-center**
-   **in basso al centro**
-   **top-baseline**
-   **linea di base inferiore**
-   **top-center-baseline**
-   **bottom-center-baseline**

Il testo verrà ancorato a una posizione verticale nella casella di testo, come indicato dal valore dell'attributo . L'allineamento di un ancoraggio di testo diventa evidente solo se [MSO-Fit-Text-To-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) è **False.** Questo attributo è diverso **dall'attributo Vertical-Align** Style, usato per le lingue ideografiche.

Questo attributo viene usato dai Microsoft Office per archiviare i dati nei documenti Web, ma non viene eseguito il rendering in Microsoft Internet Explorer 5 o versione successiva.

*Attributo VML Standard*

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



 

 