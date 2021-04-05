---
title: Elemento TextBox la
description: Elemento TextBox la
ms.assetid: 3573256e-f241-4de7-8541-252c92109af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a46ce8b6636b79099b7f7423fd8f746602a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727567"
---
# <a name="vml-textbox-element"></a>Elemento TextBox la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce una casella di testo per una forma.

Gli attributi seguenti modificano una casella di testo.



| Attributo                                                                    | Descrizione                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| [Direzione](msdn-online-vml-direction-attribute.md)                         | Definisce la direzione del testo.                         |
| [ID](id-attribute--textbox--vml.md)                                         | Definisce un identificatore univoco per la casella di testo.               |
| [Inserto](msdn-online-vml-inset-attribute.md)                                 | Specifica i valori del margine interno per il testo della casella di testo.            |
| [InsetMode](msdn-online-vml-insetmode-attribute.md)                         | Definisce il modo in cui un'applicazione consentirà valori di incasso personalizzati. |
| [Layout-flusso](msdn-online-vml-layout-flow-attribute.md)                     | Determina il flusso del testo nella casella di testo.            |
| [MSO-direzione-Alt](msdn-online-vml-mso-direction-alt-attribute.md)         | Definisce direzioni alternative per il testo nelle caselle di testo.        |
| [MSO-Fit-Shape-to-text](msdn-online-vml-mso-fit-shape-to-text-attribute.md) | Determina se una forma si estenderà per adattarla al testo.       |
| [MSO-Fit-Text-to-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) | Determina se il testo si estenderà per adattarsi a una forma.       |
| [MSO-layout-Flow-Alt](msdn-online-vml-mso-layout-flow-alt-attribute.md)     | Definisce il flusso di layout alternativo per il testo in una casella di testo.   |
| [MSO-Next-TextBox](msdn-online-vml-mso-next-textbox-attribute.md)           | Specifica la casella di testo successiva in una serie.                    |
| [MSO-ruota](msdn-online-vml-mso-rotate-attribute.md)                       | Determina se il testo ruota con una forma ruotata.      |
| [MSO-scalabilità testuale](msdn-online-vml-mso-text-scale-attribute.md)               | Definisce il fattore di scala per l'inserimento di testo in forme.     |
| [SingleClick](msdn-online-vml-singleclick-attribute.md)                     | Determina se il testo è selezionabile con un solo clic. |
| [V-text-anchor](msdn-online-vml-v-text-anchor-attribute.md)                 | Definisce l'ancoraggio verticale del testo in una casella di testo.       |



 

**Osservazioni:**

Questo elemento deve essere definito all'interno di un elemento [Shape](shape-element--vml.md) .

Di seguito è riportato il codice minimo necessario per generare una casella di testo.


```HTML
   <v:oval strokecolor="red" fillcolor="yellow
   style="position:relative;top:50;left:50;width:75;height:50">
   <v:textbox>VML</v:textbox>
   </v:oval>
```



Si noti che il testo visualizzato nella casella di testo è racchiuso tra i tag TextBox. Il testo all'interno dei tag può essere modificato da tag HTML normali.

**Esempio**

-   [Esempio di casella di testo semplice](/previous-versions/bb264075(v=vs.85))

 

 