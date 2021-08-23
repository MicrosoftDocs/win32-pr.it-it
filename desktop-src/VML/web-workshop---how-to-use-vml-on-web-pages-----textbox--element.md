---
title: Uso dell'elemento Textbox
description: Uso dell'elemento Textbox
ms.assetid: e0022722-a504-47da-aa3f-62aa7fb4ac4d
keywords:
- Web workshop, elemento textbox
- progettazione di pagine Web, elemento textbox
- Vector Markup Language (VML), elemento textbox
- VML (Vector Markup Language),elemento textbox
- grafica vettoriale, elemento textbox
- elemento textbox
- Elementi VML, casella di testo
- Forme VML, elemento textbox
- Vector Markup Language (VML), collegamento di testo
- VML (Vector Markup Language), collegamento di testo
- grafica vettoriale, collegamento di testo
- forme VML, collegamento di testo
- collegamento di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a9b4cb0b9096777a017dafd7df1c738621a4d5681ac3228741b3fd30386ed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512627"
---
# <a name="using-the-textbox-element"></a>Uso dell'elemento Textbox

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

## <a name="examples"></a>Esempi:

Per associare testo a un rettangolo, è possibile digitare le righe seguenti `<BODY>` nell'area della pagina Web:


```HTML
<body>
<v:rect style='width:120pt;height:80pt;' fillcolor="red">
<v:textbox>
I'm attaching some text to this shape!!!
</v:textbox>
</v:rect>
</body>
```





Per associare un collegamento ipertestuale a un rettangolo arrotondato con riempimento sfumato, è possibile digitare le righe seguenti `<BODY>` nell'area della pagina Web:

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





Per altre informazioni su questo elemento, vedere la specifica [VML](https://www.w3.org/TR/NOTE-VML#-toc416858397) .

 

 