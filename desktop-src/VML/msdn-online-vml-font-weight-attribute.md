---
title: Attributo vml Font-Weight
description: Attributo vml Font-Weight
ms.assetid: d7b2b0c5-b5cf-4e7d-bbca-c554d12bf97e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14dd5edb3fed869390edeff514471359162ee39fd1d78796af3d2a260c96bdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754642"
---
# <a name="vml-font-weight-attribute"></a>Attributo vml Font-Weight

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce lo spessore delle lettere del tipo di carattere. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Percorso di testo](msdn-online-vml-textpath-element.md)

**Sintassi dei tag**

<v: *element* style="font-weight: *expression* ">

**Sintassi dello script**

*element* .style.fontweight="*expression*"

*expression* = *elemento*.style.fontweight

**Osservazioni:**

I valori sono gli stessi degli attributi di stile HTML standard. I possibili valori sono:



| Valore   | Descrizione                                                                 |
|---------|-----------------------------------------------------------------------------|
| normale  | Normale. Valore predefinito.                                                            |
| Grassetto    | Grassetto.                                                                       |
| bolder  | Più pesante del normale.                                                        |
| lighter | Più leggero del normale.                                                        |
| 100     | Almeno quanto il peso di 200.                                        |
| 200     | Almeno il grassetto come il peso 100 e almeno il peso di 300. |
| 300     | Almeno il grassetto come il peso 200 e almeno il peso 400. |
| 400     | Normale.                                                                     |
| 500     | Almeno il grassetto come il peso 400 e almeno la luce come il peso 600. |
| 600     | Almeno il grassetto come il peso 500 e almeno il peso 700. |
| 700     | Grassetto.                                                                       |
| 800     | Almeno il grassetto come il peso 700 e almeno la luce come il peso 900. |
| 900     | Almeno in grassetto come il peso di 800.                                         |



 

*Attributo VML Standard*

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



 

 