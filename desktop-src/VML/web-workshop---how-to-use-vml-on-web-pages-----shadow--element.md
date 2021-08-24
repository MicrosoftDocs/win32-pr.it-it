---
title: Uso dell'elemento Shadow
description: Uso dell'elemento Shadow
ms.assetid: 905df226-6232-4e1c-8a9c-f4d4c50b13fa
keywords:
- Workshop Web, elemento shadow
- progettazione di pagine Web, elemento shadow
- Vector Markup Language (VML),elemento shadow
- VML (Vector Markup Language),elemento shadow
- grafica vettoriale, elemento shadow
- shadow - elemento
- elementi VML, ombreggiatura
- Forme VML, elemento ombreggiatura
- Vector Markup Language (VML), disegno con effetti ombreggiatura
- VML (Vector Markup Language),disegno con effetti ombreggiatura
- grafica vettoriale, disegno con effetti ombreggiatura
- forme VML, disegno con effetti ombreggiatura
- disegno con effetti ombreggiatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83be3f59eacfb495a2c80d212bc99cfd3d43be10aa8144eb68d3defd8a029e41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512597"
---
# <a name="using-the-shadow-element"></a>Uso dell'elemento Shadow

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

In questo argomento verrà illustrato come usare il `<shadow>` sotto-elemento per disegnare una forma con vari effetti ombreggiati.

È possibile inserire il `<shadow>` sotto-elemento all'interno di , o qualsiasi elemento forma predefinito `<shape>` per disegnare una forma `<shapetype>` con un'ombreggiatura. È quindi possibile usare gli attributi della proprietà del `<shadow>` sotto-elemento per personalizzare l'ombreggiatura.

Ad esempio, per creare una forma con un'ombreggiatura, come illustrato nell'immagine seguente, è possibile digitare le righe seguenti `<BODY>` nell'area della pagina Web:

![shape1.gif (887 byte)](images/shape1.gif)


```HTML
<v:oval style='width:120pt;height:80pt;' fillcolor="red">
<v:shadow on="t" type="perspective"
origin=".5,.5" offset="0,0"
matrix=",-92680f,,,,-95367431641e-17"/>
</v:oval>
```





-   `on="t"` e `type="perspective"` indicano di attivare l'ombreggiatura usando il tipo di prospettiva.
-   **L'origine** e **l'offset** indicano dove disegnare l'ombreggiatura.
-   `matrix="..."` specifica la matrice di trasformazione prospettica.

Per altre informazioni su questo elemento, vedere la [specifica VML](https://www.w3.org/TR/NOTE-VML#-toc416858396) .

 

 