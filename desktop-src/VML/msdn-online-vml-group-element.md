---
title: Elemento gruppo VML
description: Elemento gruppo VML
ms.assetid: 536c2380-2583-4fe8-a92e-c539de209a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd68bf24d217310bf52998779396b4e0b72aef02073c3ad6d2a0d6566d30fc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754598"
---
# <a name="vml-group-element"></a>Elemento gruppo VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Definisce un gruppo che può essere usato per raccogliere forme.

Questo elemento supporta gli stessi attributi di una forma, ad eccezione dei seguenti:

-   **Nascosto**
-   **type**
-   **Adj**
-   **path**
-   **spid**
-   **Opacità**
-   **chromakey**
-   **Accarezzò**
-   **strokecolor**
-   **strokeweight**
-   **Riempito**
-   **Fillcolor**
-   **Spt**
-   **ruleinitiator**
-   **ruleproxy**
-   **Connectortype**
-   **bwmode**
-   **bwpure**
-   **bwnormal**
-   **forcedash**
-   **oleicon**
-   **preferrelative**
-   **Ole**

Con Group è possibile usare solo i sottoelementi **seguenti.**

-   **Gruppo**
-   **Tipo di forma**
-   **Forma**
-   **Lock**

**Esempio**

Nell'esempio seguente viene illustrato come definire un gruppo.


```HTML
<!-- Include the VML behavior -->
<style>v\: * { behavior: url(#default#VML);display:inline-block }</style>

<!-- Declare the VML namespace -->
<xml:namespace ns="urn:schemas-microsoft-com:vml" prefix="v"/>

<v:group id="group1" style="left:10px;top:10px;width:50px;height:50px;"
  coordorigin="0,0" coordsize="6000,6000">

<v:shape id="_x0000_s2051"
  style='position:relative;left:234.75pt;top:208.875pt;width:235.25pt;height:128.875pt'
  coordsize="3765,2060"
  path="m1285,251l1126,469,580,1009,,1285,25,1412,93,1547,194,1673,1017,2026,2312,2060,3209,1756,3765,1388,3278,680,3059,319,2976,,1285,251,1285,251xe"
  fillcolor="#bcbcd6" stroked="f">
  <v:path arrowok="t"/>
 </v:shape>

 <v:shape id="_x0000_s2052" style='position:relative;left:314.625pt;
  top:140.5pt;width:104pt;height:102pt' coordsize="1663,1633"
  path="m0,1355l177,1498,353,1582,840,1633,1378,1498,1663,1295,1545,456,1260,10,1025,,656,260,253,874,,1355,,1355xe"
  fillcolor="#99ebff" stroked="f">
  <v:path arrowok="t"/>
 </v:shape>

</v:group>
```





 

 