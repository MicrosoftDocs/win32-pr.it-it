---
title: Elemento TextBox VML
description: Elemento TextBox VML
ms.assetid: 3573256e-f241-4de7-8541-252c92109af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84b6ef160e975f00dd859e0f6db6f2821054a34815b3aef1ea19f520ad3d01a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597510"
---
# <a name="vml-textbox-element"></a>Elemento TextBox VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce una casella di testo per una forma.

Gli attributi seguenti modificano una casella di testo.



| Attributo                                                                    | Descrizione                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| [Direzione](msdn-online-vml-direction-attribute.md)                         | Definisce la direzione del testo.                         |
| [ID](id-attribute--textbox--vml.md)                                         | Definisce un identificatore univoco per la casella di testo.               |
| [Inserto](msdn-online-vml-inset-attribute.md)                                 | Specifica i valori del margine interno per il testo della casella di testo.            |
| [InsetMode](msdn-online-vml-insetmode-attribute.md)                         | Definisce il modo in cui un'applicazione consentirà valori inset personalizzati. |
| [Layout e Flow](msdn-online-vml-layout-flow-attribute.md)                     | Determina il flusso del testo nella casella di testo.            |
| [MSO-Direction-Alt](msdn-online-vml-mso-direction-alt-attribute.md)         | Definisce le direzioni alternative per il testo nelle caselle di testo.        |
| [MSO-Fit-Shape-To-Text](msdn-online-vml-mso-fit-shape-to-text-attribute.md) | Determina se una forma verrà adattata al testo.       |
| [MSO-Fit-Text-To-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) | Determina se il testo verrà adattato a una forma.       |
| [MSO-Layout-Flow-Alt](msdn-online-vml-mso-layout-flow-alt-attribute.md)     | Definisce il flusso di layout alternativo per il testo in una casella di testo.   |
| [MSO-Next-Textbox](msdn-online-vml-mso-next-textbox-attribute.md)           | Specifica la casella di testo successiva in una serie.                    |
| [MSO - Rotazione](msdn-online-vml-mso-rotate-attribute.md)                       | Determina se il testo ruota con una forma ruotata.      |
| [MsO-Text-Scale](msdn-online-vml-mso-text-scale-attribute.md)               | Definisce il fattore di ridimensionamento per l'adattamento del testo alle forme.     |
| [Singleclick](msdn-online-vml-singleclick-attribute.md)                     | Determina se il testo è selezionabile con un solo clic. |
| [Ancoraggio V-Text](msdn-online-vml-v-text-anchor-attribute.md)                 | Definisce l'ancoraggio verticale del testo in una casella di testo.       |



 

**Osservazioni:**

Questo elemento deve essere definito all'interno di un [elemento Shape.](shape-element--vml.md)

Di seguito è riportato il codice minimo necessario per produrre una casella di testo.


```HTML
   <v:oval strokecolor="red" fillcolor="yellow
   style="position:relative;top:50;left:50;width:75;height:50">
   <v:textbox>VML</v:textbox>
   </v:oval>
```



Si noti che il testo visualizzato nella casella di testo è racchiuso tra i tag TextBox. Il testo all'interno dei tag può essere modificato da tag HTML normali.

**Esempio**

-   [Esempio di TextBox semplice](/previous-versions/bb264075(v=vs.85))

 

 