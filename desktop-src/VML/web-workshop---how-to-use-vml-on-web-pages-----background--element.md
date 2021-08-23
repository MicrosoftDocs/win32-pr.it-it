---
title: Uso dell'elemento Background
description: Uso dell'elemento Background
ms.assetid: d11c1542-7f44-4ca7-9fb2-c8858fde3bc4
keywords:
- Web workshop, elemento background
- progettazione di pagine Web, elemento background
- Vector Markup Language (VML), elemento background
- VML (Vector Markup Language),elemento background
- grafica vettoriale, elemento di sfondo
- elemento background
- elementi VML, sfondo
- Forme VML, elemento di sfondo
- Vector Markup Language (VML), personalizzazione degli sfondi
- VML (Vector Markup Language),personalizzazione degli sfondi
- grafica vettoriale, personalizzazione degli sfondi
- forme VML, personalizzazione degli sfondi
- personalizzazione degli sfondi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb4a694aa5458a0eae01fcbf577f72da8b8f54b7efda506423565aee362ce2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512781"
---
# <a name="using-the-background-element"></a>Uso dell'elemento Background

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

In questo argomento verrà illustrato come personalizzare lo sfondo di una pagina Web usando `<background>` l'elemento fornito in VML.

Come si è appreso [ `<fill>` ](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) dall'argomento Usare, è possibile inserire il sotto-elemento all'interno di , o qualsiasi elemento forma predefinito per descrivere come riempire `<fill>` la `<shape>` `<shapetype>` forma.

Analogamente, è possibile inserire il sotto-elemento all'interno dell'elemento per descrivere come riempire lo `<fill>` sfondo di una pagina `<background>` Web. È quindi possibile usare gli attributi della proprietà del sotto-elemento per personalizzare l'effetto di riempimento, ad esempio il riempimento sfumato, il riempimento a motivi `<fill>` o il riempimento [immagine.](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) [](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) [](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)

Ad esempio, per disegnare uno sfondo con sfumatura, è possibile digitare le righe seguenti `<BODY>` nell'area della pagina Web:


```HTML
<v:background fillcolor="red">
<v:fill type="gradient"/>
</v:background>
```





Per altre informazioni su questo elemento, vedere la specifica [VML](https://www.w3.org/TR/NOTE-VML#-toc416858389) .

 

 