---
title: Attributo VML V-Text-Align
description: Attributo VML V-Text-Align
ms.assetid: ca2cbbf6-ddbb-4f2b-942c-3fe0033bd649
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54bf8ec2e781b04e7ababc0b30ea3996e569e5cf9066a4bac072806fd7329eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117939130"
---
# <a name="vml-v-text-align-attribute"></a>Attributo VML V-Text-Align

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce l'allineamento del testo. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Percorso di testo](msdn-online-vml-textpath-element.md)

**Sintassi dei tag**

<v: *element* style="v-text-align: *expression* ">

**Sintassi dello script**

*element* .style.v-text-align="*expression*"

*expression* = *elemento*.style.v-text-align

**Osservazioni:**

I possibili valori sono:

-   **left** (impostazione predefinita)
-   **va bene**
-   **Centro**
-   **Giustificare**
-   **lettera-giustificazione**
-   **giustificazione estesa**

*Attributo VML Standard*

**Esempio**

Il testo verrà adattato al percorso, ma lo spazio aggiuntivo verrà inserito tra ogni lettera.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-align:letter-justify;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 