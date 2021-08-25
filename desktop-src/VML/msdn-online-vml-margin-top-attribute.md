---
title: Attributo vml Margin-Top
description: Attributo vml Margin-Top
ms.assetid: bce0c575-918a-45ea-a068-cfb6f4a16b1a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e42d86ba6e0fe05c2b0dff1f6d8bdabba0100fffee97d489fd59360cb8e13bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346397"
---
# <a name="vml-margin-top-attribute"></a>Attributo vml Margin-Top

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Specifica il bordo superiore del rettangolo che contiene la forma rispetto all'ancoraggio della forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* margin-top=" *expression* ">

**Sintassi dello script**

*element* .margin-top="*expression*"

*expression* = *elemento*.margin-top

**Osservazioni:**

**L'attributo Margin-Top** è simile all'attributo HTML **Margin-Top** standard usato con i fogli di stile.

Si noti che **margintop** viene usato al posto di **margin-top per** lo scripting. Si noti anche che se **la posizione** è **assoluta,** il margine non verrà modificato.

Questa proprietà viene usata al posto di **Top** per le forme Microsoft Word e Microsoft Excel mobili in una posizione relativa a un punto di ancoraggio.

I possibili valori sono:



| Valore      | Descrizione                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Posizione predefinita di un elemento nel flusso della pagina.                                                                                                                                           |
| units      | Valore predefinito. Numero con un identificatore di unità assoluto (cm, mm, in, pt, pc o px) o un designatore di unità relative (em o ex). Se non viene specificata alcuna unità, vengono utilizzati i pixel (px). Il valore predefinito è 0. |
| percentuale | Valore espresso come percentuale dell'altezza dell'oggetto padre.                                                                                                                                    |



 

*Attributo VML Standard*

**Vedere anche**

[Unità](msdn-online-vml-units.md)

**Esempio**

Il margine superiore è impostato su 25 pixel.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-top:25px">
   </v:rect>
```



[Esempio di attributo Margin-Top](/previous-versions/bb264087(v=vs.85)). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 