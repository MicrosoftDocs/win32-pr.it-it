---
title: Attributo VML V-Text-Spacing-Mode
description: Attributo VML V-Text-Spacing-Mode
ms.assetid: 2c20e9d7-cb6a-4da7-af7a-9a7b1baa8e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a42137e8c8ec401548c4e0b027a50f34813fc7b45b04c4568011617906ac8e1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057659"
---
# <a name="vml-v-text-spacing-mode-attribute"></a>Attributo VML V-Text-Spacing-Mode

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce la modalità per la combinazione di lettere. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintassi dei tag**

<v: *element* style="v-text-spacing-mode: *expression* ">

**Sintassi dello script**

*element* .style.v-text-spacing-mode="*expression*"

*expression* = *element*.style.v-text-spacing-mode

**Osservazioni:**

I valori includono

-   **tightening** (impostazione predefinita)
-   **Monitoraggio**

Questo attributo determina se lo spazio verrà rimosso tra ogni lettera (stringing) o aggiunto tra ogni lettera (rilevamento). La quantità di modifiche di spaziatura tra lettere è definita [dall'attributo V-Text-Spacing.](msdn-online-vml-v-text-spacing-attribute.md)

*Attributo standard VML*

**Esempio**

La combinazione di lettere tra ogni lettera viene aumentata di 200 unità.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tracking;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 