---
title: Elemento percorso VML
description: Elemento percorso VML
ms.assetid: c5b9f9e3-edee-45fa-9387-8f15e09983ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb46ce43d2dc9ad80aeb21340dceacde80feba99d9debdf66920b662eeaf3a9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119308181"
---
# <a name="vml-path-element"></a>Elemento percorso VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce un percorso per una forma.

Gli attributi seguenti modificano un'ombreggiatura.



| Attributo                                                        | Descrizione                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Freccia](msdn-online-vml-arrowok-attribute.md)                 | Determina se verranno visualizzate le frecce.                                |
| [ConnectAngles](msdn-online-vml-connectangles-attribute.md)     | Specifica la modalità di connessione di una curva a un punto di connessione.                       |
| [ConnectLocs](msdn-online-vml-connectlocs-attribute.md)         | Definisce la posizione dei punti di connessione in un percorso.                            |
| [ConnectType](msdn-online-vml-connecttype-attribute.md)         | Definisce il tipo di punto di connessione utilizzato per associare forme ad altre forme. |
| [EstrusioneOK](msdn-online-vml-extrusionok-attribute.md)         | Determina se verrà visualizzata un'estrusione.                              |
| [FillOK](msdn-online-vml-fillok-attribute.md)                   | Determina se verrà visualizzato un riempimento.                                    |
| [GradientShapeOK](msdn-online-vml-gradientshapeok-attribute.md) | Determina se verrà visualizzata una forma sfumato.                          |
| [ID](id-attribute--path--vml.md)                                | Definisce un identificatore univoco per un percorso.                                         |
| [Limousine](msdn-online-vml-limo-attribute.md)                       | Definisce un punto di estensione sul percorso.                                            |
| [ShadowOK](msdn-online-vml-shadowok-attribute.md)               | Determina se verrà visualizzata un'ombreggiatura.                                  |
| [StrokeOK](msdn-online-vml-strokeok-attribute.md)               | Determina se verrà visualizzato un tratto.                                  |
| [TextBoxRect](msdn-online-vml-textboxrect-attribute.md)         | Definisce una o più caselle di testo all'interno di una forma.                                   |
| [TextPathOK](msdn-online-vml-textpathok-attribute.md)           | Determina se verrà visualizzato un percorso di testo.                                |
| [V](msdn-online-vml-v-attribute.md)                             | Definisce i comandi che costituiscono un percorso.                                       |



 

**Osservazioni:**

Questo elemento deve essere definito all'interno di un [elemento Shape.](shape-element--vml.md)

Il codice seguente illustra come definire una forma con un percorso.


```HTML
   <v:shape strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="top:1;left:1;width:50;height:50">
   <v:path v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



Si noti che [l'attributo V](msdn-online-vml-v-attribute.md) **di Path** sostituisce [l'attributo Path](msdn-online-vml-path-attribute.md) di [Shape](shape-element--vml.md).

**esempi**

-   [Esempio di elemento figlio Simple Path](/previous-versions/bb229545(v=vs.85))
-   [Esempio di elemento figlio Dynamic Path](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/path/x_path.md)

 

 