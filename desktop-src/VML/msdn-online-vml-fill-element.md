---
title: Elemento VML Fill
description: Elemento VML Fill
ms.assetid: ea790017-5aaa-4e75-8fc7-77fc94fd1d1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc7205baa9db0eaa7d84d4022057f81804ea790
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963435"
---
# <a name="vml-fill-element"></a>Elemento VML Fill

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce un riempimento per una forma.

Gli attributi seguenti modificano un riempimento.



| Attributo                                                          | Descrizione                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [AlignShape](msdn-online-vml-alignshape-attribute.md)             | Determina se un'immagine viene allineata a una forma.   |
| [AltHRef](althref-attribute--fill--vml.md)                        | Specifica un riferimento alternativo per un'immagine.         |
| [Angle](angle-attribute--fill--vml.md)                            | Definisce l'angolo di un riempimento sfumato.                  |
| [Aspetto](msdn-online-vml-aspect-attribute.md)                     | Specifica il modo in cui l'aspetto dell'immagine di riempimento verrà mantenuto. |
| [Colore](color-attribute--fill--vml.md)                            | Definisce il colore di un riempimento.                           |
| [Color2](color2-attribute--fill--vml.md)                          | Definisce il secondo colore per un riempimento.                   |
| [Colori](msdn-online-vml-colors-attribute.md)                     | Definisce più colori per un riempimento sfumato.           |
| [DetectMouseClick](detectmouseclick-attribute--fill--vml.md)      | Determina se viene rilevato un clic del mouse.          |
| [Lo stato attivo](msdn-online-vml-focus-attribute.md)                       | Definisce il centro di un riempimento sfumato lineare.          |
| [FocusPosition](msdn-online-vml-focusposition-attribute.md)       | Definisce il centro di un riempimento con sfumatura radiale.          |
| [FocusSize](msdn-online-vml-focussize-attribute.md)               | Definisce le dimensioni dello stato attivo per un riempimento radiale.              |
| [HRef](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | Definisce un URL per il file di immagine originale.              |
| [ID](id-attribute--fill--vml.md)                                  | Definisce un identificatore univoco per il riempimento.              |
| [Metodo](msdn-online-vml-method-attribute.md)                     | Definisce il metodo utilizzato per generare un riempimento sfumato.   |
| [Sì](on-attribute--fill--vml.md)                                  | Determina se deve essere visualizzata la finestra di riempimento.          |
| [Opacità](opacity-attribute--fill--vml.md)                        | Definisce la trasparenza di un riempimento.                    |
| [Opacity2](msdn-online-vml-opacity2-attribute.md)                 | Definisce la trasparenza del secondo colore di riempimento.     |
| [Origine](origin-attribute--fill--vml.md)                          | Definisce il centro di un'immagine.                        |
| [Position](position-attribute--fill--vml.md)                      | Definisce la posizione di un'immagine.                      |
| [Dimensioni](size-attribute--fill--vml.md)                              | Definisce le dimensioni di un'immagine.                          |
| [Src](src-attribute--fill--vml.md)                                | Definisce l'immagine da caricare per un riempimento.                  |
| [Title](title-attribute--fill--vml.md)                            | Definisce il titolo di un riempimento.                           |
| [Tipo](type-attribute--fill--vml.md)                              | Definisce il tipo di riempimento.                              |



 

**Osservazioni:**

Questo elemento deve essere definito all'interno di un elemento [Shape](shape-element--vml.md) .

Il codice seguente mostra un riempimento sfumato semplice per una forma.


```HTML
   <v:shape
   style="position:relative;top:1;left:1;width:400;height:400"
   path = "m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type=gradient color="blue" color2="yellow"/>
   </v:shape>
```



**esempi**

-   [Riempimento sfumato semplice](/previous-versions/bb229620(v=vs.85))
-   [Esempio di riempimento dinamico](/previous-versions/bb229621(v=vs.85))

 

 