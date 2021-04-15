---
title: Utilizzo dell'elemento TextBox
description: Utilizzo dell'elemento TextBox
ms.assetid: e0022722-a504-47da-aa3f-62aa7fb4ac4d
keywords:
- Web Workshop, elemento TextBox
- progettazione di pagine Web, elemento TextBox
- Vector Markup Language (la), elemento TextBox
- LA (Vector Markup Language), elemento TextBox
- Vector graphics, elemento TextBox
- elemento TextBox
- Elementi la, TextBox
- Forme la, elemento TextBox
- Vector Markup Language (la), associazione del testo
- LA (Vector Markup Language), associazione di testo
- grafica vettoriale, associazione di testo
- LA forme, associazione di testo
- Aggiunta di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5388a359ca8cf4e320f95d708b4cf7055287d424
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474123"
---
# <a name="using-the-textbox-element"></a>Utilizzo dell'elemento TextBox

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

## <a name="examples"></a>Esempi:

Per aggiungere testo a un rettangolo, è possibile digitare le righe seguenti nell' `<BODY>` area della pagina Web:


```HTML
<body>
<v:rect style='width:120pt;height:80pt;' fillcolor="red">
<v:textbox>
I'm attaching some text to this shape!!!
</v:textbox>
</v:rect>
</body>
```





Per allineare un collegamento ipertestuale a un rettangolo arrotondato con riempimento sfumato, è possibile digitare le righe seguenti nell' `<BODY>` area della pagina Web:

![textbox2.gif (1147 byte)](images/textbox2.gif)


```HTML
<body>
<v:roundrect style='width:80pt;height:30pt;' fillcolor="red">
<v:fill type="gradient" />
<v:textbox>
<a href="https://home.microsoft.com/"> Click here</a>
</v:textbox>
</v:roundrect>
</body>
```





Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858397) .

 

 