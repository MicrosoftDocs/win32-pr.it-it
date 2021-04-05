---
title: Utilizzo dell'elemento background
description: Utilizzo dell'elemento background
ms.assetid: d11c1542-7f44-4ca7-9fb2-c8858fde3bc4
keywords:
- Web Workshop, elemento background
- progettazione di pagine Web, elemento background
- Vector Markup Language (la), elemento background
- LA (Vector Markup Language), elemento background
- Vector graphics, elemento background
- elemento background
- Elementi la, background
- Forme la, elemento background
- Vector Markup Language (la), personalizzazione degli sfondi
- LA (Vector Markup Language), personalizzazione degli sfondi
- grafica vettoriale, personalizzazione degli sfondi
- LA forme, personalizzazione degli sfondi
- personalizzazione degli sfondi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0108b91f199fbc3bff1c28ebdf016bfba11957
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872621"
---
# <a name="using-the-background-element"></a>Utilizzo dell'elemento background

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

In questo argomento verrà illustrato come è possibile personalizzare lo sfondo di una pagina Web utilizzando l' `<background>` elemento fornito in la.

Come si è appreso dall' [argomento `<fill>` use](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) , è possibile inserire il `<fill>` sottoelemento all'interno `<shape>` di, `<shapetype>` o qualsiasi elemento Shape predefinito per descrivere come riempire la forma.

Analogamente, è possibile inserire il `<fill>` sottoelemento all'interno dell' `<background>` elemento per descrivere come riempire lo sfondo di una pagina Web. È quindi possibile usare gli attributi di proprietà del `<fill>` sottoelemento per personalizzare l'effetto di riempimento, ad esempio [riempimento sfumato](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), [riempimento pattern](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)o [riempimento immagine](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).

Ad esempio, per creare uno sfondo con riempimento sfumato, è possibile digitare le righe seguenti nell' `<BODY>` area della pagina Web:


```HTML
<v:background fillcolor="red">
<v:fill type="gradient"/>
</v:background>
```





Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858389) .

 

 