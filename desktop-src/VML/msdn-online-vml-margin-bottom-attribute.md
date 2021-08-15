---
title: Attributo Margin-Bottom VML
description: Attributo Margin-Bottom VML
ms.assetid: c1101430-f4fc-4fa5-8e02-7cee126c2c1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 551cf9cba00901e07998f2de38465cba1cb45bb8f563c04d1adf25f75d1852bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057819"
---
# <a name="vml-margin-bottom-attribute"></a>Attributo Margin-Bottom VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Specifica il bordo inferiore del rettangolo contenente la forma rispetto all'ancoraggio della forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* margin-bottom=" *expression* ">

**Sintassi dello script**

*element* .marginbottom="*expression*"

*expression* = *elemento*.marginbottom

**Osservazioni:**

**L'attributo Margin-Bottom** è simile all'attributo **Margin-Bottom** HTML standard usato con i fogli di stile.

Si noti **che marginbottom** viene usato invece **di margin-bottom per** lo scripting. Si noti anche che **se la posizione** è **assoluta,** il margine non verrà modificato.

I possibili valori sono:



| Valore      | Descrizione                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Posizione predefinita di un elemento nel flusso della pagina.                                                                                                                                           |
| units      | Valore predefinito. Numero con un designatore di unità assolute (cm, mm, in, pt, pc o px) o un designatore di unità relative (em o ex). Se non viene specificata alcuna unità, vengono utilizzati i pixel (px). Il valore predefinito è 0. |
| percentuale | Valore espresso come percentuale dell'altezza dell'oggetto padre.                                                                                                                                    |



 

*Attributo standard VML*

**Vedere anche**

[Unità](msdn-online-vml-units.md)

**Esempio**

Il margine inferiore è impostato su 25 pixel.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-bottom:25px">
   </v:rect>
```



[Esempio di attributo Margin-Bottom](/previous-versions/bb229675(v=vs.85)). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 