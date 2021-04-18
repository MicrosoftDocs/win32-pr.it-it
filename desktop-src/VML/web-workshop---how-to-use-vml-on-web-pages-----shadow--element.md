---
title: Utilizzo dell'elemento Shadow
description: Utilizzo dell'elemento Shadow
ms.assetid: 905df226-6232-4e1c-8a9c-f4d4c50b13fa
keywords:
- Web Workshop, elemento Shadow
- progettazione di pagine Web, elemento Shadow
- Vector Markup Language (la), elemento Shadow
- LA (Vector Markup Language), elemento Shadow
- grafica vettoriale, elemento Shadow
- elemento Shadow
- Elementi la, ombreggiatura
- Forme la, elemento Shadow
- Vector Markup Language (la), disegno con effetti di ombreggiatura
- LA (Vector Markup Language), disegno con effetti di ombreggiatura
- grafica vettoriale, disegno con effetti di ombreggiatura
- LA forme, disegno con effetti ombreggiatura
- disegno con effetti di ombreggiatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe32651fbeab6b84b49a40bae05a08ba3d9c33a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399626"
---
# <a name="using-the-shadow-element"></a>Utilizzo dell'elemento Shadow

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

In questo argomento verrà illustrato come utilizzare il `<shadow>` sottoelemento per disegnare una forma con diversi effetti di ombreggiatura.

È possibile inserire il `<shadow>` sottoelemento all'interno `<shape>` di, `<shapetype>` o qualsiasi elemento della forma predefinito per disegnare una forma con un'ombreggiatura. È quindi possibile usare gli attributi di proprietà del `<shadow>` sottoelemento per personalizzare l'ombreggiatura.

Ad esempio, per creare una forma con un'ombreggiatura, come illustrato nell'immagine seguente, è possibile digitare le righe seguenti nell' `<BODY>` area della pagina Web:

![shape1.gif (887 byte)](images/shape1.gif)


```HTML
<v:oval style='width:120pt;height:80pt;' fillcolor="red">
<v:shadow on="t" type="perspective"
origin=".5,.5" offset="0,0"
matrix=",-92680f,,,,-95367431641e-17"/>
</v:oval>
```





-   `on="t"` e `type="perspective"` indicano di attivare l'ombreggiatura usando il tipo di prospettiva.
-   L' **origine** e l' **offset** indicano dove si desidera creare l'ombreggiatura.
-   `matrix="..."` Specifica la matrice di trasformazione della prospettiva.

Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858396) .

 

 