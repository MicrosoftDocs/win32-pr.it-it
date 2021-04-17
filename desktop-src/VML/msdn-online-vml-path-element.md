---
title: Elemento Path la
description: Elemento Path la
ms.assetid: c5b9f9e3-edee-45fa-9387-8f15e09983ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1de9440761479d6b3dc6cb10c96b00ea48626247
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299904"
---
# <a name="vml-path-element"></a>Elemento Path la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce un percorso per una forma.

Gli attributi seguenti modificano un'ombreggiatura.



| Attributo                                                        | Descrizione                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Arrowok](msdn-online-vml-arrowok-attribute.md)                 | Determina se le frecce verranno visualizzate.                                |
| [ConnectAngles](msdn-online-vml-connectangles-attribute.md)     | Specifica il modo in cui una curva si connetterà a un punto di connessione.                       |
| [ConnectLocs](msdn-online-vml-connectlocs-attribute.md)         | Definisce la posizione dei punti di connessione in un percorso.                            |
| [ConnectType](msdn-online-vml-connecttype-attribute.md)         | Definisce il tipo di punto di connessione utilizzato per il collegamento di forme ad altre forme. |
| [ExtrusionOK](msdn-online-vml-extrusionok-attribute.md)         | Determina se verrà visualizzata un'estrusione.                              |
| [FillOK](msdn-online-vml-fillok-attribute.md)                   | Determina se verrà visualizzato un riempimento.                                    |
| [GradientShapeOK](msdn-online-vml-gradientshapeok-attribute.md) | Determina se verrà visualizzata una forma sfumatura.                          |
| [ID](id-attribute--path--vml.md)                                | Definisce un identificatore univoco per un percorso.                                         |
| [Limousine](msdn-online-vml-limo-attribute.md)                       | Definisce un punto di estensione nel percorso.                                            |
| [ShadowOK](msdn-online-vml-shadowok-attribute.md)               | Determina se verrà visualizzata un'ombreggiatura.                                  |
| [StrokeOK](msdn-online-vml-strokeok-attribute.md)               | Determina se un tratto verrà visualizzato.                                  |
| [TextBoxRect](msdn-online-vml-textboxrect-attribute.md)         | Definisce una o più caselle di testo all'interno di una forma.                                   |
| [TextPathOK](msdn-online-vml-textpathok-attribute.md)           | Determina se verrà visualizzato un TextPath.                                |
| [V](msdn-online-vml-v-attribute.md)                             | Definisce i comandi che costituiscono un percorso.                                       |



 

**Osservazioni:**

Questo elemento deve essere definito all'interno di un elemento [Shape](shape-element--vml.md) .

Nel codice seguente viene illustrato come definire una forma con un percorso.


```HTML
   <v:shape strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="top:1;left:1;width:50;height:50">
   <v:path v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



Si noti che l'attributo [V](msdn-online-vml-v-attribute.md) di **path** sostituisce l'attributo [path](msdn-online-vml-path-attribute.md) di [Shape](shape-element--vml.md).

**esempi**

-   [Esempio di elemento figlio Path semplice](/previous-versions/bb229545(v=vs.85))
-   [Esempio di elemento figlio Path dinamico](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/path/x_path.md)

 

 