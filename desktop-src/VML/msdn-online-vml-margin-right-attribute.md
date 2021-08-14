---
title: Attributo Margin-Right VML
description: Attributo Margin-Right VML
ms.assetid: 7b635bea-df3f-4a24-aa22-cfca95575599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5569f4f89cbe5320cfc348f2e2929b986736412f4cb864a62dd4584bde43a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346459"
---
# <a name="vml-margin-right-attribute"></a>Attributo Margin-Right VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Specifica il bordo destro del rettangolo contenente la forma rispetto all'ancoraggio della forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* style="margin-right: *expression* ">

**Sintassi dello script**

*element* .style.marginright="*expression*"

*expression* = *elemento*.style.marginright

**Osservazioni:**

**L'attributo Margin-Right** è simile all'attributo **Margin-Right** HTML standard usato con i fogli di stile.

Si noti che **marginright** viene usato anziché **margin-right per** lo scripting. Si noti anche che **se la posizione** è **assoluta,** il margine non verrà modificato.

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

Il margine destro è impostato su 25 pixel.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-right:25px">
   </v:rect>
```



[Esempio di attributo Margin-Right](/previous-versions/bb229677(v=vs.85)). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 