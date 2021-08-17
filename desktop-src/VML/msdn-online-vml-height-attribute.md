---
title: Attributo altezza VML
description: Attributo altezza VML
ms.assetid: 5667ddc5-c840-40d8-894e-58396f56e0fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49218b83834d0d276d458656376d1806089be00a2158f271e38a4ee8da8099c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136994"
---
# <a name="vml-height-attribute"></a>Attributo altezza VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Specifica l'altezza della forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* style="height: *expression* ">

**Sintassi dello script**

*element* .style.height="*expression*"

*expression* = *elemento*.style.height

**Osservazioni:**

**L'attributo Height** è simile all'attributo **HTML Height** standard per gli stili.

Le unità possono essere mappate all'elemento padre o possono essere in unità assolute.

I possibili valori sono:



| Valore      | Descrizione                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Posizione predefinita di un elemento nel flusso della pagina.                                                                                                          |
| units      | Numero con un designatore di unità assolute (cm, mm, in, pt, pc o px) o un designatore di unità relative (em o ex). Se non viene specificata alcuna unità, vengono utilizzati i pixel (px). |
| percentuale | Valore espresso come percentuale dell'altezza dell'oggetto padre.                                                                                                   |



 

*Attributo standard VML*

**Vedere anche**

[Unità](msdn-online-vml-units.md)

**Esempio**

L'altezza della forma è impostata su 30.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:30">
   </v:rect>
```



[Esempio di attributo Height](/previous-versions/bb229671(v=vs.85)). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 