---
title: Attributo Font-Weight la
description: Attributo Font-Weight la
ms.assetid: d7b2b0c5-b5cf-4e7d-bbca-c554d12bf97e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70e4de8a1bb4132c75d4520dcacc661fbbc97eef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399238"
---
# <a name="vml-font-weight-attribute"></a>Attributo Font-Weight la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce lo spessore delle lettere del tipo di carattere. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintassi Tag**

<v: *elemento* Style = "font-weight: *Expression* " >

**Sintassi dello script**

*element* . Style. FontWeight = "*Expression*"

*espressione* = *element*. Style. FontWeight

**Osservazioni:**

I valori corrispondono agli attributi di stile HTML standard. I possibili valori sono:



| Valore   | Descrizione                                                                 |
|---------|-----------------------------------------------------------------------------|
| normale  | Normale. Valore predefinito.                                                            |
| Grassetto    | Grassetto.                                                                       |
| bolder  | Più pesante del normale.                                                        |
| lighter | Più chiaro del normale.                                                        |
| 100     | Almeno leggero come 200 peso.                                        |
| 200     | Almeno come grassetto come 100 e almeno come il peso 300. |
| 300     | Almeno come grassetto come 200 e almeno come il peso 400. |
| 400     | Normale.                                                                     |
| 500     | Almeno come grassetto come 400 e almeno come il peso 600. |
| 600     | Almeno come grassetto come 500 e almeno come il peso 700. |
| 700     | Grassetto.                                                                       |
| 800     | Almeno come grassetto come 700 e almeno come il peso 900. |
| 900     | Almeno in grassetto come 800 peso.                                         |



 

*Attributo standard la*

**Esempio**

Lo spessore del carattere è in grassetto.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal bold 36pt Arial"/>
   </v:line>
```



 

 