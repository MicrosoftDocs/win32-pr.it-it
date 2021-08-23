---
title: Attributo vml Margin-Left
description: Attributo vml Margin-Left
ms.assetid: 65488c47-06c2-4a8f-8d29-4837865465f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f403c19e617f8131886d3f4a862ff1ac0b878edbd2acf2fd0e27cb17b3406c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680822"
---
# <a name="vml-margin-left-attribute"></a>Attributo vml Margin-Left

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Specifica il bordo sinistro del rettangolo che contiene la forma rispetto all'ancoraggio della forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* style="margin-left: *expression* ">

**Sintassi dello script**

*element* .style.marginleft="*expression*"

*expression* = *elemento*.style.marginleft

**Osservazioni:**

**L'attributo Margin-Left** è simile all'attributo HTML **Margin-Left** standard usato con i fogli di stile.

Si noti che **marginleft** viene usato al posto **di margin-left per** lo scripting. Si noti anche che se **la posizione** è **assoluta,** il margine non verrà modificato.

Questa proprietà viene usata al posto di **Left** per le forme Microsoft Word e Microsoft Excel mobili in una posizione relativa a un punto di ancoraggio.

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

Il margine sinistro è impostato su 25 pixel.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-left:25px">
   </v:rect>
```



[Esempio di attributo Margin-Left](/previous-versions/visualstudio/design-tools/expression-studio-3/ee371308(v=expression.40)#examples). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 