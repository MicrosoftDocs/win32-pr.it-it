---
title: La MSO-attributo in modalità wrap
description: La MSO-attributo in modalità wrap
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5657192fcf9da72ff99dc25cff7930b6d2d9b6b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338094"
---
# <a name="vml-mso-wrap-mode-attribute"></a>La MSO-attributo in modalità wrap

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la modalità di wrapping per il testo. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *elemento* Style = "MSO-Wrap-Mode: *Expression* " >

**Osservazioni:**

I possibili valori sono:



| Valore          | Descrizione                          |
|----------------|--------------------------------------|
| square         | Esegue il wrapping del testo intorno alla forma in un quadrato. |
| una stretta          | Il testo viene incapsulato vicino alla forma.  |
| in alto e in basso | Il testo passa dall'alto verso il basso.       |
| -        | Il testo viene visualizzato attraverso la forma.     |
| Nessuno           | Il testo non viene incapsulato.                   |



 

Usato da Microsoft PowerPoint per il salvataggio nel codice HTML per indicare se il ritorno a capo automatico all'interno di una forma è on (**Square**) o off (**nessuno**).

*Attributo Microsoft Office Extensions*

**Esempio**

Il codice seguente indica che WordWrap all'interno di una forma AutoShape è attivato in PowerPoint.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 