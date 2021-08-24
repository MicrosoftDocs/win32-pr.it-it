---
title: Attributo type (Shape)(VML)
description: Attributo type (Shape)(VML)
ms.assetid: 41f0d1d3-3a2c-47cf-b2ec-d983b14aea87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b20f663f8a403acca03ff8ab516a86dc91f7dd8d478eadedaa6be8b919ad48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513151"
---
# <a name="type-attribute-shapevml"></a>Attributo type (Shape)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce un riferimento all'ID di un [elemento ShapeType.](msdn-online-vml-shapetype-element.md) Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

``` syntax
<v:
          element 
          type=" expression ">
```

**Sintassi dello script**

``` syntax
element 
          .type="#expression"
```

``` syntax
expression=element .type
```

**Osservazioni:**

Se **l'attributo Type** fa riferimento all'ID di un **elemento ShapeType,** i riempimenti, i percorsi e i tratti di **ShapeType** vengono usati come modelli per creare la forma. I valori derivati da **ShapeType** possono essere sostituiti da singoli valori di forma.

Se usato nei tag, il valore stringa deve iniziare con un simbolo di simbolo di \# numero ( ).

**Attributo standard VML**

**Esempio**

Viene creata una forma **ShapeType** con "mytype" come ID.


```HTML
   <v:shapetype id="mytype"
   fillcolor="red" strokecolor="blue"
   coordorigin="0 0" coordsize="200 200">
   <v:path v="m 0,0 l 0,200, 200,200, 200,0 x e"/>
   </v:shapetype>
```



Quindi, se si crea una forma usando i **valori ShapeType,** la forma avrà gli attributi di **ShapeType "mytype".** cio, "shape01" avrà un riempimento rosso con un tratto blu.


```HTML
   <v:shape id="shape01" type="#mytype"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



È possibile eseguire l'override dei valori ereditati, ad esempio modificando il colore in verde.


```HTML
   <v:shape id="shape02" type="#mytype"
   fillcolor="green"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



[Esempio di attributo Type](/previous-versions/bb264099(v=vs.85)). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 