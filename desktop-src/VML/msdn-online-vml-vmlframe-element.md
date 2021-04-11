---
title: Elemento VML VMLFrame
description: Elemento VML VMLFrame
ms.assetid: a1582223-d6e2-42d1-95bb-97f6f1d453d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f53371afb0c2790ff6dd666f0121b30b586c51b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117858"
---
# <a name="vml-vmlframe-element"></a>Elemento VML VMLFrame

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce un frame per una forma esterna.

Gli attributi seguenti modificano un frame.



| Attributo                                     | Descrizione                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------|
| [Clip](msdn-online-vml-clip-attribute.md)    | Determina se l'immagine verrà ritagliata.                         |
| [ID](id-attribute--vmlframe--vml.md)         | Definisce un identificatore univoco per il frame.                            |
| [Origine](origin-attribute--vmlframe--vml.md) | Specifica l'origine del frame.                                    |
| [Dimensioni](size-attribute--vmlframe.md)          | Specifica le dimensioni del frame.                                      |
| [Src](src-attribute--vmlframe--vml.md)       | Specifica l'origine dei dati che verranno visualizzati nel frame. |
| [Style](msdn-online-vml-style-attribute.md)  | Definisce gli stili CSS normali che possono essere usati per posizionare il frame. |



 

**Osservazioni:**

I dati di origine da visualizzare nel frame possono essere contenuti nella stessa pagina Web o far parte di un'altra pagina. Tramite lo scripting, l'origine può essere modificata dinamicamente e le caratteristiche di visualizzazione possono essere modificate.

Gli oggetti all'interno della **VMLFrame** sono "scalabilità zoom". Ovvero, vengono ridimensionati come i metafile, in cui i pesi delle righe, gli offset di ombreggiatura e l'area di testo vengono ridimensionati proporzionalmente. Si tratta di un gruppo diverso da quello in cui le dimensioni e la posizione dell'oggetto vengono ridimensionate in modo proporzionale, ma la riga, l'ombreggiatura e così via.

Di seguito è riportato il codice minimo necessario per caricare un'immagine in un frame.


```HTML
   <v:vmlframe
     style="top:1;left:1;width:50;height:50">
     src="external.vml#rect01"/>
   </v:vmlframe>
```



Se il file è esterno, deve essere un file XML. Il codice seguente è il codice minimo necessario per specificare un file di origine esterno che deve contenere una forma identificabile. Questo esempio contiene una forma immagine che consente di visualizzare una bitmap.


```HTML
   <xml xmlns:v = "urn:schemas-microsoft-com:vml">
   <v:image id="rect01"
     style="height:100;width:100;top:50;left:50">
     src="kids.jpg">
   </v:rect>
   </xml>
```



> [!Note]  
> Nelle versioni non definitive di la, questo elemento è stato chiamato **VMLCanvas** .

 

**esempi**

-   [Esempio di VMLFrame semplice](/previous-versions/bb263920(v=vs.85))
-   [Esempio di VMLFrame dinamico](/previous-versions/bb263902(v=vs.85))

 

 