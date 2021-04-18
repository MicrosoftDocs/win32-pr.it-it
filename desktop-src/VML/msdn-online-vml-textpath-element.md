---
title: Elemento VML TextPath
description: Elemento VML TextPath
ms.assetid: dcc3b723-4c5c-4069-93c7-c41737292109
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08707ae79bf297e6094228b26ae118c57a03c736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299844"
---
# <a name="vml-textpath-element"></a>Elemento VML TextPath

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce un percorso di testo per una forma.

Gli attributi seguenti modificano un percorso di testo.



| Attributo                                                                    | Descrizione                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [FitPath](msdn-online-vml-fitpath-attribute.md)                             | Definisce se il testo corrisponde al percorso di una forma.                             |
| [FitShape](msdn-online-vml-fitshape-attribute.md)                           | Definisce se il testo soddisfa i limiti della forma.                            |
| [Famiglia di caratteri](msdn-online-vml-font-family-attribute.md)                     | Specifica la famiglia di caratteri del testo.                                             |
| [Dimensione carattere](msdn-online-vml-font-size-attribute.md)                         | Specifica la dimensione del tipo di carattere del testo.                                               |
| [Stile carattere](msdn-online-vml-font-style-attribute.md)                       | Specifica lo stile del tipo di carattere del testo.                                              |
| [Variant carattere](msdn-online-vml-font-variant-attribute.md)                   | Specifica il tipo di carattere Variant del testo.                                            |
| [Carattere-spessore](msdn-online-vml-font-weight-attribute.md)                     | Specifica lo spessore del carattere del testo.                                             |
| [Carattere](msdn-online-vml-font-attribute.md)                                   | Specifica il valore del carattere composto del testo.                                     |
| [MSO-testo-ombreggiatura](msdn-online-vml-mso-text-shadow-attribute.md)             | Definisce se un'ombreggiatura viene applicata al testo.                               |
| [Sì](on-attribute--textpath--vml.md)                                        | Definisce se il testo viene visualizzato.                                         |
| [Stringa](msdn-online-vml-string-attribute.md)                               | Definisce la stringa di testo.                                                       |
| [Decorazione di testo](msdn-online-vml-text-decoration-attribute.md)             | Definisce l'effetto di testo del testo.                                       |
| [Trim](msdn-online-vml-trim-attribute.md)                                   | Definisce se lo spazio aggiuntivo viene rimosso sopra e sotto il testo.               |
| [V-ruota-lettere](msdn-online-vml-v-rotate-letters-attribute.md)           | Determina se le lettere del testo vengono ruotate.                        |
| [V-same-Letter-Heights](msdn-online-vml-v-same-letter-heights-attribute.md) | Determina se tutte le lettere avranno la stessa altezza.                      |
| [V-text-align](msdn-online-vml-v-text-align-attribute.md)                   | Definisce l'allineamento del testo.                                             |
| [V-text-Kern](msdn-online-vml-v-text-kern-attribute.md)                     | Determina se la crenatura è attivata.                                       |
| [V-text-inverso](msdn-online-vml-v-text-reverse-attribute.md)               | Determina se l'ordine di layout delle righe è invertito.                       |
| [Modalità di spaziatura con testo V](msdn-online-vml-v-text-spacing-mode-attribute.md)     | Definisce la modalità per letterSpacing.                                            |
| [Spaziatura con testo](msdn-online-vml-v-text-spacing-attribute.md)               | Definisce la quantità di spaziatura per il testo.                                        |
| [XScale](msdn-online-vml-xscale-attribute.md)                               | Determina se verrà utilizzato un TextPath diretto al posto del percorso della forma. |



 

**Osservazioni:**

Questo elemento deve essere definito all'interno di un elemento [Shape](shape-element--vml.md) .

Oltre agli attributi di riempimento, stringa e stile normali, l'attributo [TextPathOK](msdn-online-vml-textpathok-attribute.md) di [path](msdn-online-vml-path-element.md) deve essere impostato su **true** e l'attributo [on](on-attribute--textpath--vml.md) di TextPath deve essere impostato su **true** per visualizzare il testo in un percorso di testo.

Di seguito è riportato il codice minimo necessario per visualizzare il testo in un percorso.


```HTML
   <v:line from="50 200" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



**esempi**

-   [Esempio di TextPath semplice](/previous-versions/bb264038(v=vs.85))
-   [Esempio di Typeface TextPath dinamico](/previous-versions/bb264042(v=vs.85))
-   [Esempio di curva TextPath dinamica](/previous-versions/bb264041(v=vs.85))

 

 